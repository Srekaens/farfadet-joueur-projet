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
- RG09 : Un événement peut avoir une image (optionnel)
- RG10 : Un événement possède un statut (planifié, en cours, terminé, annulé)
- RG11 : Un événement possède une visibilité (public/privé)
```

- **RG12 :** Un événement est associé à **un seul type d'événement**
- **RG13 :** Un événement peut être associé à **0 ou n images**
- **RG14 :** Un événement est créé par **un seul collaborateur**

## Type d'Événement
---
```
- RG15 : Un type d'événement est représenté par un identifiant unique
- RG16 : Un type d'événement possède un nom
- RG17 : Un type d'événement possède une icône
```

- **RG18 :** Un type d'événement peut contenir **0 ou n événements**

## Collaborateur
---
```
- RG19 : Un collaborateur est représenté par un identifiant unique
- RG20 : Un collaborateur possède un nom
- RG21 : Un collaborateur possède un prénom
- RG22 : Un collaborateur possède un email
- RG23 : Un collaborateur possède un mot de passe (hashé)
- RG24 : Un collaborateur possède un rôle (admin, éditeur, modérateur)
- RG25 : Un collaborateur possède un statut (actif/inactif)
- RG26 : Un collaborateur possède une photo de profil
- RG27 : Un collaborateur possède une description
- RG28 : Un collaborateur possède un ordre d'affichage dans la section "Qui sommes-nous"
```

- **RG29 :** Un collaborateur peut créer **0 ou n événements**
- **RG30 :** Un collaborateur peut modifier **0 ou n événements**
- **RG31 :** Un collaborateur peut supprimer **0 ou n événements**
- **RG32 :** Un collaborateur peut gérer **0 ou n autres collaborateurs** (si admin)
- **RG33 :** Un collaborateur peut recevoir **0 ou n emails**

## Utilisateur
---
```
- RG34 : Un utilisateur est représenté par un identifiant unique
- RG35 : Un utilisateur possède un nom
- RG36 : Un utilisateur possède un prénom
- RG37 : Un utilisateur possède un email
- RG38 : Un utilisateur possède un statut (actif/inactif)
- RG39 : Un utilisateur possède une date de création
- RG40 : Un utilisateur possède une date de dernière connexion
```

- **RG41 :** Un utilisateur peut s'inscrire à **0 ou n événements**
- **RG42 :** Un utilisateur peut recevoir **0 ou n emails**

## Image
---
```
- RG43 : Une image est représentée par un identifiant unique
- RG44 : Une image possède un nom de fichier
- RG45 : Une image possède un chemin d'accès
- RG46 : Une image possède un format
- RG47 : Une image possède une taille
- RG48 : Une image possède une date d'upload
```

- **RG49 :** Une image est associée à **un seul événement**

## Session
---
```
- RG50 : Une session est représentée par un identifiant unique
- RG51 : Une session possède un token
- RG52 : Une session possède une date de création
- RG53 : Une session possède une date d'expiration
- RG54 : Une session possède un statut (active/expirée)
```

- **RG55 :** Une session est associée à **un seul collaborateur**

## Email
---
```
- RG56 : Un email est représenté par un identifiant unique
- RG57 : Un email possède un destinataire
- RG58 : Un email possède un sujet
- RG59 : Un email possède un contenu
- RG60 : Un email possède une date d'envoi
- RG61 : Un email possède un statut (en attente, envoyé, échoué)
- RG62 : Un email possède un type (notification, réinitialisation mot de passe, etc.)
- RG63 : Un email possède un template
- RG64 : Un email possède des variables de template
```

- **RG65 :** Un email est associé à **un seul utilisateur ou collaborateur**
- **RG66 :** Un email peut être associé à **un seul événement** (optionnel)

