-------------------------------------------------------------
----------------------REGLES DE GESTION----------------------
-------------------------------------------------------------

## Visiteur
---
```
- RG01 : Un visiteur est une personne non enregistrée dans le système
- RG02 : Un visiteur peut consulter les événements publics
- RG03 : Un visiteur peut s'inscrire pour devenir membre
```

## Membre (Inscrit)
---
```
- RG04 : Un membre est représenté par un identifiant unique
- RG05 : Un membre possède un nom
- RG06 : Un membre possède un prénom
- RG07 : Un membre possède un email
- RG08 : Un membre possède un mot de passe (hashé)
- RG09 : Un membre possède une date d'inscription
- RG10 : Un membre possède une date de dernière connexion
- RG11 : Un membre possède un statut (actif/inactif)
- RG12 : Un membre peut demander une réinitialisation de mot de passe
```

- **RG13 :** Un membre peut consulter **tous les événements**
- **RG14 :** Un membre peut s'inscrire à **0 ou n événements**
- **RG15 :** Un membre peut recevoir **des notifications par email**

## Collaborateur
---
```
- RG16 : Un collaborateur est représenté par un identifiant unique
- RG17 : Un collaborateur possède un nom
- RG18 : Un collaborateur possède un prénom
- RG19 : Un collaborateur possède un email
- RG20 : Un collaborateur possède un mot de passe (hashé)
- RG21 : Un collaborateur possède une photo de profil
- RG22 : Un collaborateur possède une description
- RG23 : Un collaborateur possède un ordre d'affichage dans la section "Qui sommes-nous"
- RG24 : Un collaborateur possède une date de création
- RG25 : Un collaborateur possède une date de dernière connexion
- RG26 : Un collaborateur possède un statut (actif/inactif)
- RG27 : Un collaborateur peut demander une réinitialisation de mot de passe
- RG28 : Un collaborateur doit être créé par un administrateur
```

- **RG29 :** Un collaborateur peut créer **0 ou n événements**
- **RG30 :** Un collaborateur peut modifier **0 ou n événements**
- **RG31 :** Un collaborateur peut supprimer **0 ou n événements**
- **RG32 :** Un collaborateur peut avoir **0 ou n sessions**
- **RG33 :** Un collaborateur peut être **supprimé par un administrateur**

## Administrateur
---
```
- RG34 : Un administrateur est représenté par un identifiant unique
- RG35 : Un administrateur possède un nom
- RG36 : Un administrateur possède un prénom
- RG37 : Un administrateur possède un email
- RG38 : Un administrateur possède un mot de passe (hashé)
- RG39 : Un administrateur possède une photo de profil
- RG40 : Un administrateur possède une description
- RG41 : Un administrateur possède un ordre d'affichage dans la section "Qui sommes-nous"
- RG42 : Un administrateur possède une date de création
- RG43 : Un administrateur possède une date de dernière connexion
- RG44 : Un administrateur possède un statut (actif/inactif)
- RG45 : Un administrateur peut demander une réinitialisation de mot de passe
```

- **RG46 :** Un administrateur peut créer **0 ou n événements**
- **RG47 :** Un administrateur peut modifier **0 ou n événements**
- **RG48 :** Un administrateur peut supprimer **0 ou n événements**
- **RG49 :** Un administrateur peut gérer **0 ou n collaborateurs**
- **RG50 :** Un administrateur peut gérer **0 ou n membres**
- **RG51 :** Un administrateur peut avoir **0 ou n sessions**
- **RG52 :** Un administrateur **ne peut pas être supprimé**
- **RG53 :** Un administrateur peut envoyer **des invitations par email** pour créer des collaborateurs

## Événement
---
```
- RG54 : Un événement est représenté par un identifiant unique
- RG55 : Un événement possède un titre
- RG56 : Un événement possède une description
- RG57 : Un événement possède une date
- RG58 : Un événement peut avoir une heure de début (optionnel)
- RG59 : Un événement peut avoir une heure de fin (optionnel)
- RG60 : Un événement possède un lieu
- RG61 : Un événement possède un type (anniversaire, convention, tournoi, à domicile, en salle)
- RG62 : Un événement peut avoir une image (optionnel)
- RG63 : Un événement possède un statut (planifié, en cours, terminé, annulé)
- RG64 : Un événement possède une visibilité (public/privé)
```

- **RG65 :** Un événement est associé à **un seul type d'événement**
- **RG66 :** Un événement peut être associé à **0 ou n images**
- **RG67 :** Un événement est créé par **un seul collaborateur ou administrateur**
- **RG68 :** Un événement peut avoir **0 ou n inscriptions**

## Type d'Événement
---
```
- RG69 : Un type d'événement est représenté par un identifiant unique
- RG70 : Un type d'événement possède un nom
- RG71 : Un type d'événement possède une icône
```

- **RG72 :** Un type d'événement peut contenir **0 ou n événements**

## Inscription
---
```
- RG73 : Une inscription est représentée par un identifiant unique
- RG74 : Une inscription possède une date d'inscription
- RG75 : Une inscription possède un statut (en attente, confirmée, annulée)
```

- **RG76 :** Une inscription est associée à **un seul événement**
- **RG77 :** Une inscription est associée à **un seul membre**

## Image
---
```
- RG78 : Une image est représentée par un identifiant unique
- RG79 : Une image possède un nom de fichier
- RG80 : Une image possède un chemin d'accès
- RG81 : Une image possède un format
- RG82 : Une image possède une taille
- RG83 : Une image possède une date d'upload
```

- **RG84 :** Une image est associée à **un seul événement**

## Session
---
```
- RG85 : Une session est représentée par un identifiant unique
- RG86 : Une session possède un token
- RG87 : Une session possède une date de création
- RG88 : Une session possède une date d'expiration
- RG89 : Une session possède un statut (active/expirée)
```

- **RG90 :** Une session est associée à **un seul collaborateur ou administrateur**

## Email
---
```
- RG91 : Un email est représenté par un identifiant unique
- RG92 : Un email possède un destinataire
- RG93 : Un email possède un sujet
- RG94 : Un email possède un contenu
- RG95 : Un email possède une date d'envoi
- RG96 : Un email possède un statut (en attente, envoyé, échoué)
- RG97 : Un email possède un type (notification, réinitialisation mot de passe, invitation collaborateur)
- RG98 : Un email possède un template
- RG99 : Un email possède des variables de template
- RG100 : Un email d'invitation contient un lien unique et temporaire pour créer un compte
- RG101 : Un email de réinitialisation contient un lien unique et temporaire pour réinitialiser le mot de passe
```

- **RG102 :** Un email est associé à **un seul membre, collaborateur ou administrateur**
- **RG103 :** Un email peut être associé à **un seul événement** (optionnel)
- **RG104 :** Un email d'invitation est envoyé par **un seul administrateur**

