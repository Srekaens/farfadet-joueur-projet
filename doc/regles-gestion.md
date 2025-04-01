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
- RG05 : Un événement peut avoir une heure de début 
- RG07 : Un événement possède un lieu
- RG08 : Un événement possède un type (anniversaire, convention, tournoi, à domicile, en salle)
- RG09 : Un événement possède une image (URL)
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

## Utilisateur
---
```
- RG20 : Un collaborateur est représenté par un identifiant unique
- RG21 : Un collaborateur possède un nom
- RG22 : Un collaborateur possède un prénom
- RG23 : Un collaborateur possède un email
- RG24 : Un collaborateur possède un mot de passe (hashé)
- RG25 : Un collaborateur possède un rôle (admin, éditeur, modérateur)
- RG29 : Un collaborateur possède un statut (actif/inactif)
- RG29 : Un collaborateur possède une photo de profil (prévoir image par defaut avec chapeau du farfadet)


```

<!-- - RG26 : Un collaborateur possède une date de création
- RG27 : Un collaborateur possède une date de dernière modification
- RG28 : Un collaborateur possède une date de dernière connexion
- RG30 : Un collaborateur possède une photo de profil
- RG31 : Un collaborateur possède une description
- RG32 : Un collaborateur possède un ordre d'affichage dans la section "Qui sommes-nous"
 -->



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

