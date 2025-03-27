# Politique de Moindre Privilège

## Vue d'ensemble

La politique de moindre privilège consiste à accorder aux utilisateurs et aux processus uniquement les permissions nécessaires pour accomplir leurs tâches spécifiques. Cette approche est essentielle pour la sécurité du projet Farfadet Joueur.

## Implémentation

### 1. Gestion des Rôles et Permissions

#### Définition des Rôles
```typescript
// types/roles.ts
export enum UserRole {
  VISITOR = 'VISITOR',
  USER = 'USER',
  MODERATOR = 'MODERATOR',
  ADMIN = 'ADMIN'
}

export interface Permission {
  resource: string;
  actions: ('read' | 'write' | 'delete')[];
}

export const RolePermissions: Record<UserRole, Permission[]> = {
  [UserRole.VISITOR]: [
    { resource: 'events', actions: ['read'] },
    { resource: 'categories', actions: ['read'] }
  ],
  [UserRole.USER]: [
    { resource: 'events', actions: ['read', 'write'] },
    { resource: 'categories', actions: ['read'] },
    { resource: 'profile', actions: ['read', 'write'] }
  ],
  [UserRole.MODERATOR]: [
    { resource: 'events', actions: ['read', 'write', 'delete'] },
    { resource: 'categories', actions: ['read', 'write'] },
    { resource: 'users', actions: ['read'] }
  ],
  [UserRole.ADMIN]: [
    { resource: '*', actions: ['read', 'write', 'delete'] }
  ]
}
```

### 2. Middleware d'Autorisation

#### Vérification des Permissions
```typescript
// middlewares/auth.ts
import { FastifyPluginAsync } from 'fastify'
import { UserRole, RolePermissions } from '../types/roles'

export const authMiddleware: FastifyPluginAsync = async (fastify) => {
  fastify.decorate('checkPermission', async (request, reply, done) => {
    const userRole = request.user?.role || UserRole.VISITOR
    const { resource, action } = request.routeConfig.permission

    const hasPermission = RolePermissions[userRole].some(
      permission => 
        (permission.resource === '*' || permission.resource === resource) &&
        permission.actions.includes(action)
    )

    if (!hasPermission) {
      reply.code(403).send({
        error: 'Forbidden',
        message: 'Insufficient permissions'
      })
    }
  })
}
```

### 3. Gestion des Accès Base de Données

#### Configuration TypeORM
```typescript
// config/database.ts
export const databaseConfig = {
  type: 'postgres',
  host: process.env.DB_HOST,
  port: parseInt(process.env.DB_PORT || '5432'),
  username: process.env.DB_USER,
  password: process.env.DB_PASSWORD,
  database: process.env.DB_NAME,
  entities: ['src/entities/**/*.ts'],
  synchronize: false,
  logging: false,
  ssl: process.env.NODE_ENV === 'production',
  maxQueryExecutionTime: 1000,
  extra: {
    max: 20, // Limite du pool de connexions
    idleTimeoutMillis: 30000
  }
}
```

### 4. Sécurisation des Routes

#### Définition des Routes avec Permissions
```typescript
// routes/events.ts
export const eventRoutes = {
  schema: {
    tags: ['events'],
    security: [{ bearerAuth: [] }]
  },
  routes: [
    {
      method: 'GET',
      url: '/events',
      permission: { resource: 'events', action: 'read' },
      handler: async (request, reply) => {
        // Handler implementation
      }
    },
    {
      method: 'POST',
      url: '/events',
      permission: { resource: 'events', action: 'write' },
      handler: async (request, reply) => {
        // Handler implementation
      }
    }
  ]
}
```

### 5. Gestion des Sessions

#### Configuration des Sessions
```typescript
// config/session.ts
export const sessionConfig = {
  secret: process.env.SESSION_SECRET,
  cookie: {
    secure: process.env.NODE_ENV === 'production',
    httpOnly: true,
    sameSite: 'strict',
    maxAge: 24 * 60 * 60 * 1000 // 24 heures
  },
  name: 'sessionId',
  resave: false,
  saveUninitialized: false,
  rolling: true
}
```

## Bonnes Pratiques

1. **Gestion des Accès**
   - Attribution minimale des droits
   - Révision régulière des permissions
   - Journalisation des changements de droits

2. **Sécurité des Données**
   - Chiffrement des données sensibles
   - Accès restreint aux logs
   - Protection des fichiers de configuration

3. **Processus de Développement**
   - Code review obligatoire
   - Tests de sécurité automatisés
   - Documentation des changements

4. **Monitoring**
   - Suivi des tentatives d'accès
   - Détection des comportements anormaux
   - Alertes de sécurité

## Procédures de Maintenance

1. **Gestion des Comptes**
   - Désactivation automatique des comptes inactifs
   - Rotation régulière des mots de passe
   - Audit des comptes privilégiés

2. **Mises à jour**
   - Patchs de sécurité prioritaires
   - Mise à jour des dépendances
   - Tests de régression

3. **Documentation**
   - Mise à jour des procédures
   - Formation de l'équipe
   - Documentation des incidents

## Conformité

1. **Audit**
   - Revue régulière des permissions
   - Vérification des accès
   - Documentation des changements

2. **Reporting**
   - Rapports de sécurité
   - Statistiques d'utilisation
   - Incidents de sécurité

3. **Formation**
   - Sensibilisation à la sécurité
   - Bonnes pratiques
   - Procédures d'urgence 