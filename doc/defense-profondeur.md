# Stratégie de Défense en Profondeur

## Vue d'ensemble

La défense en profondeur est une approche de sécurité qui implémente plusieurs couches de protection pour sécuriser l'application. Chaque couche contribue à la sécurité globale, même si une couche est compromise. Cette stratégie est particulièrement importante pour le projet Farfadet Joueur, qui gère des données d'événements et d'utilisateurs.

## Couches de Protection

### 1. Couche Frontend (React)

#### Validation des Données
- Utilisation de Zod pour la validation des formulaires
- Sanitisation des entrées utilisateur
- Protection contre les attaques XSS
- Validation côté client avant l'envoi des données

#### Gestion des Sessions
- Stockage sécurisé des tokens JWT
- Gestion des sessions avec expiration
- Protection contre le vol de session

### 2. Couche API (Fastify)

#### Middleware de Sécurité
```typescript
// middlewares/security.ts
import helmet from '@fastify/helmet'
import cors from '@fastify/cors'

export const securityMiddleware = {
  // Configuration Helmet pour les en-têtes de sécurité
  helmet: {
    contentSecurityPolicy: {
      directives: {
        defaultSrc: ["'self'"],
        scriptSrc: ["'self'", "'unsafe-inline'"],
        styleSrc: ["'self'", "'unsafe-inline'"],
        imgSrc: ["'self'", "data:", "https:"],
      }
    },
    crossOriginEmbedderPolicy: false,
    crossOriginResourcePolicy: { policy: "cross-origin" }
  },
  
  // Configuration CORS
  cors: {
    origin: process.env.FRONTEND_URL,
    methods: ['GET', 'POST', 'PUT', 'DELETE'],
    credentials: true
  }
}
```

#### Validation des Requêtes
- Validation des DTOs avec Zod
- Sanitisation des paramètres d'URL
- Protection contre les injections SQL

### 3. Couche Base de Données

#### Sécurité des Requêtes
- Utilisation de TypeORM pour la protection contre les injections SQL
- Paramétrage des requêtes
- Validation des types de données

#### Gestion des Connexions
- Pool de connexions limité
- Timeout des connexions inactives
- Gestion des erreurs de connexion

### 4. Couche Infrastructure

#### Configuration du Serveur
- HTTPS obligatoire
- Limitation des requêtes (rate limiting)
- Protection contre les attaques DDoS

#### Monitoring et Logging
- Journalisation des événements de sécurité
- Détection des tentatives d'intrusion
- Alertes en cas de comportement suspect

## Implémentation

### 1. Configuration de Base

```typescript
// config/security.ts
export const securityConfig = {
  // Configuration générale
  rateLimit: {
    max: 100,
    timeWindow: '1 minute'
  },
  
  // Configuration JWT
  jwt: {
    secret: process.env.JWT_SECRET,
    expiresIn: '24h',
    refreshToken: {
      expiresIn: '7d'
    }
  },
  
  // Configuration des sessions
  session: {
    cookie: {
      secure: true,
      httpOnly: true,
      sameSite: 'strict'
    }
  }
}
```

### 2. Middleware de Protection

```typescript
// middlewares/protection.ts
import { FastifyPluginAsync } from 'fastify'
import { securityConfig } from '../config/security'

export const protectionMiddleware: FastifyPluginAsync = async (fastify) => {
  // Rate limiting
  await fastify.register(import('@fastify/rate-limit'), {
    max: securityConfig.rateLimit.max,
    timeWindow: securityConfig.rateLimit.timeWindow
  })

  // Protection contre les attaques XSS
  fastify.addHook('onRequest', async (request, reply) => {
    // Sanitisation des entrées
    if (request.body) {
      request.body = sanitizeInput(request.body)
    }
  })
}
```

### Validation des Données avec Zod

Zod est une bibliothèque de validation de schéma qui permet de :
- Valider les données entrantes
- Garantir la sécurité des types
- Prévenir les injections et les attaques par manipulation de données

Exemple d'utilisation de Zod pour la validation des événements :

```typescript
import { z } from 'zod';

// Schéma de validation pour un événement
const EventSchema = z.object({
  title: z.string()
    .min(3, "Le titre doit contenir au moins 3 caractères")
    .max(100, "Le titre ne doit pas dépasser 100 caractères"),
  description: z.string()
    .min(10, "La description doit contenir au moins 10 caractères")
    .max(1000, "La description ne doit pas dépasser 1000 caractères"),
  date: z.date()
    .min(new Date(), "La date doit être dans le futur"),
  location: z.string()
    .min(5, "Le lieu doit contenir au moins 5 caractères"),
  type: z.enum(['birthday', 'convention', 'tournament', 'home', 'venue']),
  startTime: z.string().optional(),
  endTime: z.string().optional(),
  imageUrl: z.string().url().optional(),
  maxParticipants: z.number().int().positive().optional()
});

// Utilisation dans une route Fastify
app.post('/api/events', async (request, reply) => {
  try {
    // Validation des données entrantes
    const validatedData = EventSchema.parse(request.body);
    
    // Si la validation réussit, les données sont sûres
    const event = await createEvent(validatedData);
    
    return reply.send(event);
  } catch (error) {
    if (error instanceof z.ZodError) {
      // Gestion des erreurs de validation
      return reply.status(400).send({
        error: "Données invalides",
        details: error.errors
      });
    }
    throw error;
  }
});
```

### Middleware de Sécurité

```typescript
import fastify from 'fastify';
import helmet from '@fastify/helmet';
import cors from '@fastify/cors';
import rateLimit from '@fastify/rate-limit';

const app = fastify();

// Configuration des en-têtes de sécurité
app.register(helmet, {
  contentSecurityPolicy: {
    directives: {
      defaultSrc: ["'self'"],
      imgSrc: ["'self'", "data:", "https:"],
      scriptSrc: ["'self'"],
      styleSrc: ["'self'", "'unsafe-inline'"],
    },
  },
});

// Configuration CORS
app.register(cors, {
  origin: process.env.ALLOWED_ORIGINS?.split(',') || ['http://localhost:3000'],
  methods: ['GET', 'POST', 'PUT', 'DELETE'],
  credentials: true,
});

// Rate limiting
app.register(rateLimit, {
  max: 100,
  timeWindow: '1 minute',
});
```

### Protection contre les Injections SQL

```typescript
import { Pool } from 'pg';

const pool = new Pool({
  connectionString: process.env.DATABASE_URL,
});

// Requête sécurisée avec des paramètres
async function getEventById(id: string) {
  const query = 'SELECT * FROM events WHERE id = $1';
  const values = [id];
  
  const result = await pool.query(query, values);
  return result.rows[0];
}

// Requête sécurisée pour la création d'événement
async function createEvent(event: Event) {
  const query = `
    INSERT INTO events (title, description, date, location, type, start_time, end_time, image_url)
    VALUES ($1, $2, $3, $4, $5, $6, $7, $8)
    RETURNING *
  `;
  
  const values = [
    event.title,
    event.description,
    event.date,
    event.location,
    event.type,
    event.startTime,
    event.endTime,
    event.imageUrl
  ];
  
  const result = await pool.query(query, values);
  return result.rows[0];
}
```

## Bonnes Pratiques

1. **Validation des Données**
   - Toujours valider les entrées utilisateur
   - Utiliser des schémas de validation stricts
   - Rejeter les données invalides

2. **Gestion des Sessions**
   - Utiliser des tokens JWT avec expiration
   - Implémenter le refresh token
   - Stocker les tokens de manière sécurisée

3. **Protection des Routes**
   - Authentification pour les routes sensibles
   - Vérification des permissions
   - Rate limiting sur les routes critiques

4. **Monitoring**
   - Journalisation des événements de sécurité
   - Surveillance des tentatives d'intrusion
   - Alertes en temps réel

## Tests de Sécurité

1. **Tests Automatisés**
   - Tests de pénétration automatisés
   - Tests de vulnérabilités
   - Tests de validation des entrées

2. **Audits de Sécurité**
   - Revue de code de sécurité
   - Tests de configuration
   - Vérification des dépendances

## Maintenance

1. **Mises à jour**
   - Mise à jour régulière des dépendances
   - Correction des vulnérabilités
   - Adaptation aux nouvelles menaces

2. **Documentation**
   - Mise à jour des procédures de sécurité
   - Documentation des incidents
   - Formation de l'équipe 