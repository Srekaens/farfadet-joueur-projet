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
- RG18 : Un type d'événement possède une image par défaut
```

- **RG19 :** Un type d'événement peut contenir **0 ou n événements**

## Collaborateur
---
```
- RG20 : Un collaborateur est représenté par un identifiant unique
- RG21 : Un collaborateur possède un nom
- RG22 : Un collaborateur possède un prénom
- RG23 : Un collaborateur possède un email
- RG24 : Un collaborateur possède un mot de passe (hashé)
- RG25 : Un collaborateur possède un rôle (admin, éditeur, modérateur)
- RG26 : Un collaborateur possède une date de création
- RG27 : Un collaborateur possède une date de dernière modification
- RG28 : Un collaborateur possède une date de dernière connexion
- RG29 : Un collaborateur possède un statut (actif/inactif)
- RG30 : Un collaborateur possède une photo de profil
- RG31 : Un collaborateur possède une description
- RG32 : Un collaborateur possède un ordre d'affichage dans la section "Qui sommes-nous"
```

- **RG33 :** Un collaborateur peut créer **0 ou n événements**
- **RG34 :** Un collaborateur peut modifier **0 ou n événements**
- **RG35 :** Un collaborateur peut supprimer **0 ou n événements**
- **RG36 :** Un collaborateur peut gérer **0 ou n autres collaborateurs** (si admin)

## Image
---
```
- RG37 : Une image est représentée par un identifiant unique
- RG38 : Une image possède un nom de fichier
- RG39 : Une image possède un chemin d'accès
- RG40 : Une image possède un format
- RG41 : Une image possède une taille
- RG42 : Une image possède une date d'upload
```

- **RG43 :** Une image est associée à **un seul événement**

## Session
---
```
- RG44 : Une session est représentée par un identifiant unique
- RG45 : Une session possède un token
- RG46 : Une session possède une date de création
- RG47 : Une session possède une date d'expiration
- RG48 : Une session possède un statut (active/expirée)
```

- **RG49 :** Une session est associée à **un seul collaborateur**

## Notification
---
```
- RG50 : Une notification est représentée par un identifiant unique
- RG51 : Une notification possède un type (email, push, in-app)
- RG52 : Une notification possède un titre
- RG53 : Une notification possède un contenu
- RG54 : Une notification possède une date d'envoi
- RG55 : Une notification possède un statut (en attente, envoyée, échouée)
- RG56 : Une notification possède une priorité
- RG57 : Une notification possède une date de lecture
```

- **RG58 :** Une notification est associée à **un seul utilisateur**
- **RG59 :** Une notification peut être associée à **un seul événement**

## Commentaire
---
```
- RG60 : Un commentaire est représenté par un identifiant unique
- RG61 : Un commentaire possède un contenu
- RG62 : Un commentaire possède une date de création
- RG63 : Un commentaire possède une date de modification
- RG64 : Un commentaire possède un statut (actif/supprimé)
```

- **RG65 :** Un commentaire est associé à **un seul utilisateur**
- **RG66 :** Un commentaire est associé à **un seul événement**

## Pièce Jointe
---
```
- RG67 : Une pièce jointe est représentée par un identifiant unique
- RG68 : Une pièce jointe possède un nom de fichier
- RG69 : Une pièce jointe possède un type MIME
- RG70 : Une pièce jointe possède une taille
- RG71 : Une pièce jointe possède une URL de téléchargement
- RG72 : Une pièce jointe possède une date d'upload
```

- **RG73 :** Une pièce jointe est associée à **un seul événement**

## Rappel
---
```
- RG74 : Un rappel est représenté par un identifiant unique
- RG75 : Un rappel possède un délai (avant l'événement)
- RG85 : Un rappel est représenté par un identifiant unique
- RG86 : Un rappel possède un délai (avant l'événement)
- RG87 : Un rappel possède un type (email, push, in-app)
- RG88 : Un rappel possède un statut (actif/inactif)
- RG89 : Un rappel possède une date d'envoi
```

- **RG90 :** Un rappel est associé à **un seul événement**
- **RG91 :** Un rappel est associé à **0 ou n utilisateurs**

## Préférence Utilisateur
---
```
- RG92 : Une préférence est représentée par un identifiant unique
- RG93 : Une préférence possède un type (notification, affichage, langue)
- RG94 : Une préférence possède une valeur
- RG95 : Une préférence possède une date de modification
```

- **RG96 :** Une préférence est associée à **un seul utilisateur**

## Session
---
```
- RG97 : Une session est représentée par un identifiant unique
- RG98 : Une session possède un token
- RG99 : Une session possède une date de création
- RG100 : Une session possède une date d'expiration
- RG101 : Une session possède un statut (active/expirée)
- RG102 : Une session possède une adresse IP
- RG103 : Une session possède un user-agent
```

- **RG104 :** Une session est associée à **un seul utilisateur**

