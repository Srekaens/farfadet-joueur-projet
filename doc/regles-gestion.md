# REGLES DE GESTION


## Événement
---
```
- RG01 : Un événement est représenté par un identifiant unique
- RG02 : Un événement possède un titre descriptif
- RG03 : Un événement contient une description détaillée
- RG04 : Un événement doit avoir une date 
- RG04 : Un événement peut avoir une heure de début et une heure de fin ??
- RG06 : Un événement doit faire partie d'une catégorie
- RG07 : Un événement peut avoir une image
- RG08 : Un événement peut être récurrent ???
- RG09 : Un événement peut être partagé sur les réseaux sociaux
```

- **RG12 :** Un événement **appartient à une seule catégorie**
- **RG15 :** Un événement **est créé par un administrateur**
- **RG13 :** Un événement **peut avoir une seule image**

---

## Catégorie d'Événement
---
```
- RG16 : Une catégorie est représentée par un identifiant unique
- RG17 : Une catégorie possède un nom descriptif
- RG18 : Une catégorie possède une description
- RG19 : Une catégorie a une date de création
- RG20 : Une catégorie a une date de modification
```

- **RG13 :**Une catégorie possède une image par defaut**
- **RG21 :** Une catégorie **peut contenir plusieurs événements**
- **RG22 :** Une catégorie **est gérée par les administrateurs**

---

## Image
---
```
- RG23 : Une image est représentée par un identifiant unique
- RG24 : Une image possède un titre descriptif
- RG25 : Une image a une URL de stockage
- RG26 : Une image a une taille en octets
- RG27 : Une image a un format (jpg, png, etc.)
- RG28 : Une image a une date de création
- RG29 : Une image a une date de modification
```

- **RG30 :** Une image **est associée à un seul événement**
- **RG31 :** Une image **est optimisée pour le chargement**

---

## Utilisateur
---
```
- RG32 : Un utilisateur est représenté par un identifiant unique
- RG33 : Un utilisateur possède un nom
- RG34 : Un utilisateur possède un prénom
- RG35 : Un utilisateur est identifié par son email
- RG36 : Un utilisateur possède un mot de passe hashé
- RG37 : Un utilisateur a un rôle (admin/utilisateur)
- RG38 : Un utilisateur a une date de création
- RG39 : Un utilisateur a une date de modification
- RG40 : Un utilisateur a une date de dernière connexion
- RG41 : Un utilisateur peut être actif ou inactif
```

- **RG42 :** Un utilisateur **peut créer plusieurs événements**
- **RG43 :** Un utilisateur **peut avoir plusieurs sessions**
- **RG44 :** Un utilisateur **peut générer plusieurs logs**

---

## Session
---
```
- RG61 : Une session est représentée par un identifiant unique
- RG62 : Une session est associée à un utilisateur
- RG63 : Une session possède un token d'authentification
- RG64 : Une session a une date de création
- RG65 : Une session a une date d'expiration
- RG66 : Une session enregistre l'adresse IP
```

- **RG67 :** Une session **est associée à un seul utilisateur**
- **RG68 :** Une session **expire après 30 minutes d'inactivité**

---

<!-- ## Statistique
---
```
- RG45 : Une statistique est représentée par un identifiant unique
- RG46 : Une statistique est associée à un événement
- RG47 : Une statistique enregistre le nombre de consultations
- RG48 : Une statistique enregistre la source du trafic
- RG49 : Une statistique enregistre la date de consultation
- RG50 : Une statistique a une date de création
```

- **RG51 :** Une statistique **est associée à un seul événement**
- **RG52 :** Les statistiques **sont conservées pendant 6 mois**

--- -->

<!-- ## Log
---
```
- RG53 : Un log est représenté par un identifiant unique
- RG54 : Un log est associé à un utilisateur
- RG55 : Un log enregistre le type d'action
- RG56 : Un log enregistre l'entité concernée
- RG57 : Un log contient des détails sur l'action
- RG58 : Un log enregistre la date de l'action
```

- **RG59 :** Un log **est associé à un seul utilisateur**
- **RG60 :** Les logs **sont conservés pendant 6 mois**

--- -->

