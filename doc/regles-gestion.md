-------------------------------------------------------------
----------------------REGLES DE GESTION----------------------
-------------------------------------------------------------

## Événement
---
```
- RG01 : Un événement est représenté par un identifiant unique
- RG02 : Un événement possède un titre
- RG03 : Un événement possède une description
- RG04 : Un événement possède une date
- RG05 : Un événement peut avoir une heure de début (optionnel)
- RG06 : Un événement peut avoir une heure de fin (optionnel)
- RG07 : Un événement possède un lieu
- RG08 : Un événement possède un type (anniversaire, convention, tournoi, à domicile, en salle)
- RG09 : Un événement possède une image (URL)
- RG10 : Un événement possède un statut (planifié, en cours, terminé, annulé)
- RG11 : Un événement possède une visibilité (public/privé)???
- RG13 : Un événement peut avoir une description détaillée
```

- **RG15 :** Un événement est associé à **un seul type d'événement**
- **RG16 :** Un événement peut être associé à **0 ou 1 image**
- **RG17 :** Un événement est créé par **un seul utilisateur**
- **RG19 :** Un événement peut être partagé sur **0 ou n réseaux sociaux** ???

## Type d'Événement
---
```
- RG20 : Un type d'événement est représenté par un identifiant unique
- RG21 : Un type d'événement possède un nom
- RG22 : Un type d'événement possède une icône
- RG23 : Un type d'événement possède une image par défaut
```

- **RG24 :** Un type d'événement est attribué à **1 ou n événements** ( si un evenement est créé il a forcement un type ?)

## Image
---
```
- RG25 : Une image est représentée par un identifiant unique
- RG26 : Une image possède un nom de fichier
- RG27 : Une image possède un chemin d'accès
- RG28 : Une image possède un format
- RG29 : Une image possède une taille
- RG30 : Une image possède une date d'upload
```

- **RG31 :** Une image est associée à **un ou n événements**

## Utilisateur
---
```
- RG32 : Un utilisateur est représenté par un identifiant unique
- RG33 : Un utilisateur possède un nom
- RG34 : Un utilisateur possède un prénom
- RG35 : Un utilisateur possède un email
- RG36 : Un utilisateur possède un mot de passe (hashé)
- RG37 : Un utilisateur possède un rôle (admin/utilisateur)
- RG38 : Un utilisateur possède une date de création
- RG39 : Un utilisateur possède une date de dernière modification
- RG40 : Un utilisateur possède une date de dernière connexion
- RG41 : Un utilisateur possède un statut (actif/inactif)
- RG42 : Un utilisateur possède un token de réinitialisation de mot de passe
- RG43 : Un utilisateur possède une date d'expiration du token
- RG44 : Un utilisateur possède un statut de vérification d'email
```

- **RG45 :** Un utilisateur peut créer **0 ou n événements**
- **RG46 :** Un utilisateur peut modifier **0 ou n événements**
- **RG47 :** Un utilisateur peut supprimer **0 ou n événements**
- **RG48 :** Un utilisateur peut recevoir **0 ou n emails**
- **RG49 :** Un utilisateur peut avoir **0 ou n sessions**
- **RG50 :** Un utilisateur peut avoir **0 ou n droits** ??


## Droit
---
```
- RG52 : Un droit est représenté par un identifiant unique
- RG53 : Un droit possède un nom
- RG54 : Un droit possède une description
- RG55 : Un droit possède un niveau (lecture, écriture, suppression)
- RG56 : Un droit possède une ressource (événements, utilisateurs, etc.)
- RG57 : Un droit possède une date d'attribution
- RG58 : Un droit possède une date d'expiration ???
```

- **RG59 :** Un droit est associé à **0 ou n utilisateurs**

## Email
---
```
- RG60 : Un email est représenté par un identifiant unique
- RG61 : Un email possède un destinataire
- RG62 : Un email possède un sujet
- RG63 : Un email possède un contenu
- RG64 : Un email possède une date d'envoi
- RG65 : Un email possède un statut (en attente, envoyé, échoué)
- RG66 : Un email possède un type (notification, réinitialisation mot de passe, etc.)
- RG67 : Un email possède un template
- RG68 : Un email possède des variables de template ????
```

- **RG69 :** Un email est associé à **un seul utilisateur**


## Statistique
---
```
- RG71 : Une statistique est représentée par un identifiant unique
- RG72 : Une statistique possède un type (visite, partage, etc.)
- RG73 : Une statistique possède une valeur
- RG74 : Une statistique possède une date
- RG75 : Une statistique possède une période (jour, semaine, mois)
```

- **RG76 :** Une statistique est associée à **un seul événement**

## Page d'Accueil
---
```
- RG77 : La page d'accueil est représentée par un identifiant unique
- RG78 : La page d'accueil possède un titre
- RG79 : La page d'accueil possède une description
- RG80 : La page d'accueil possède une image de fond
- RG81 : La page d'accueil possède un contenu principal
```

- **RG82 :** La page d'accueil affiche **0 ou n événements** mis en avant

## Calendrier
---
```
- RG83 : Le calendrier est représenté par un identifiant unique
- RG84 : Le calendrier possède une vue (jour, semaine, mois)
- RG85 : Le calendrier possède une date de début
- RG86 : Le calendrier possède une date de fin
```

- **RG87 :** Le calendrier affiche **0 ou n événements**

## Log
---
```
- RG88 : Un log est représenté par un identifiant unique
- RG89 : Un log possède une action
- RG90 : Un log possède une date
- RG91 : Un log possède des détails
- RG92 : Un log possède un niveau (info, warning, error)
```

- **RG93 :** Un log est associé à **un seul utilisateur**

## Session
---
```
- RG94 : Une session est représentée par un identifiant unique
- RG95 : Une session possède un token
- RG96 : Une session possède une date de création
- RG97 : Une session possède une date d'expiration
- RG98 : Une session possède un statut (active/expirée)
```

- **RG99 :** Une session est associée à **un seul utilisateur**

