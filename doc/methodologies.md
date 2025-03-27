# Méthodologie de Développement

## Approche Agile

Le projet Farfadet Joueur suit une méthodologie agile, adaptée à la durée de 3 mois et aux besoins spécifiques du projet. Cette approche permet une gestion flexible et itérative du développement.

### Rôles et Responsabilités

#### Product Owner
- **Franck Leroy**
  - Définit la vision du produit
  - Priorise le backlog produit
  - Valide les fonctionnalités développées
  - Assure la communication avec les parties prenantes

#### Scrum Master
- **Justin Didelot**
  - Facilite les cérémonies Scrum
  - Assure le respect des pratiques agiles
  - Résout les obstacles
  - Coache l'équipe

### Cérémonies Scrum

1. **Sprint Planning**
   - Durée : 2 heures
   - Fréquence : Début de chaque sprint
   - Objectif : Sélection et décomposition des tâches du sprint

2. **Daily Scrum**
   - Durée : 15 minutes
   - Fréquence : Quotidienne
   - Format : Stand-up meeting
   - Points abordés :
     - Accomplissements de la veille
     - Objectifs du jour
     - Blocages éventuels

3. **Sprint Review**
   - Durée : 1 heure
   - Fréquence : Fin de chaque sprint
   - Objectif : Présentation des fonctionnalités développées

4. **Sprint Retrospective**
   - Durée : 1 heure
   - Fréquence : Fin de chaque sprint
   - Objectif : Amélioration continue des pratiques

### Gestion des Tâches

#### Jira
- Plateforme principale de gestion des tâches
- Utilisation des tableaux Kanban pour le suivi visuel
- Configuration des workflows adaptés au projet

#### Structure des Tickets
- **Épics** : Fonctionnalités majeures
  - Gestion des événements
  - Interface administrateur
  - Système de communication
  - Interface publique

- **User Stories** : Fonctionnalités détaillées
  - Format : "En tant que [rôle], je veux [action] pour [bénéfice]"
  - Critères d'acceptation clairs
  - Estimation en points de complexité

- **Tâches techniques** : Implémentations spécifiques
  - Développement
  - Tests
  - Documentation

### Tableau Kanban

#### Colonnes
1. **Backlog**
   - Tâches non commencées
   - Priorisées par le Product Owner

2. **À faire**
   - Tâches sélectionnées pour le sprint
   - Prêtes à être développées

3. **En cours**
   - Tâches en développement
   - Limite WIP (Work In Progress) : 3 tâches par développeur

4. **En revue**
   - Tâches en cours de revue de code
   - Validation par les pairs

5. **Fait**
   - Tâches terminées et validées
   - Prêtes pour la production

### Sprints

#### Durée
- 2 semaines par sprint
- 6 sprints au total pour le projet

#### Planning Type
1. **Semaine 1**
   - Sprint Planning
   - Développement
   - Daily Scrums

2. **Semaine 2**
   - Développement
   - Daily Scrums
   - Sprint Review
   - Sprint Retrospective

### Outils de Collaboration

1. **Jira**
   - Gestion des tickets
   - Suivi des sprints
   - Tableaux Kanban
   - Rapports de vélocité

2. **GitHub**
   - Gestion du code source
   - Pull Requests
   - Code Review
   - CI/CD

3. **Discord**
   - Communication quotidienne
   - Partage d'écran
   - Réunions à distance

### Mesures de Suivi

1. **Vélocité**
   - Points complétés par sprint
   - Tendance sur plusieurs sprints

2. **Burndown Chart**
   - Suivi de l'avancement
   - Détection des retards

3. **Qualité**
   - Couverture des tests
   - Dette technique
   - Bugs critiques

### Adaptation et Amélioration Continue

- Revue des pratiques à chaque rétrospective
- Ajustement des processus selon les retours
- Optimisation du workflow
- Mise à jour des conventions de code
