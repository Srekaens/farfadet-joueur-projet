-------------------------------------------------------------
----------------------REGLES DE GESTION----------------------
-------------------------------------------------------------

## Utilisateur
---
```
- RG01 : Un utilisateur est représenté par un identifiant unique
- RG02 : Un utilisateur possède un nom
- RG03 : Un utilisateur possède un prénom
- RG04 : Un utilisateur possède un email
- RG05 : Un utilisateur possède un mot de passe (hashé)
- RG06 : Un utilisateur possède une date d'inscription
- RG07 : Un utilisateur possède une date de dernière connexion
- RG08 : Un utilisateur possède un statut (actif/inactif)
- RG09 : Un utilisateur peut demander une réinitialisation de mot de passe
```

- **RG10 :** Un utilisateur peut proposer **0 ou n événements**
- **RG11 :** Un utilisateur peut s'inscrire à **0 ou n événements**
- **RG12 :** Un utilisateur peut créer **0 ou n commentaires**
- **RG13 :** Un utilisateur peut avoir **0 ou n sessions**
- **RG14 :** Un utilisateur peut recevoir **0 ou n emails**

## Collaborateur
---
```
- RG15 : Un collaborateur est représenté par un identifiant unique
- RG16 : Un collaborateur possède un nom
- RG17 : Un collaborateur possède un prénom
- RG18 : Un collaborateur possède un email
- RG19 : Un collaborateur possède un mot de passe (hashé)
- RG20 : Un collaborateur possède une photo de profil (optionnel)
- RG21 : Un collaborateur possède une description (optionnel)
- RG22 : Un collaborateur possède un ordre d'affichage dans la section "Qui sommes-nous" (optionnel)
- RG23 : Un collaborateur possède une date de création
- RG24 : Un collaborateur possède une date de dernière connexion
- RG25 : Un collaborateur possède un statut (actif/inactif)
- RG26 : Un collaborateur peut demander une réinitialisation de mot de passe
```

- **RG27 :** Un collaborateur peut créer **0 ou n événements**
- **RG28 :** Un collaborateur peut créer **0 ou n commentaires**
- **RG29 :** Un collaborateur peut avoir **0 ou n sessions**
- **RG30 :** Un collaborateur peut recevoir **0 ou n emails**
- **RG31 :** Un collaborateur peut valider **0 ou n événements**

## Administrateur
---
```
- RG32 : Un administrateur est représenté par un identifiant unique
- RG33 : Un administrateur possède un nom
- RG34 : Un administrateur possède un prénom
- RG35 : Un administrateur possède un email
- RG36 : Un administrateur possède un mot de passe (hashé)
- RG37 : Un administrateur possède une photo de profil (optionnel)
- RG38 : Un administrateur possède une description (optionnel)
- RG39 : Un administrateur possède un ordre d'affichage dans la section "Qui sommes-nous" (optionnel)
- RG40 : Un administrateur possède une date de création
- RG41 : Un administrateur possède une date de dernière connexion
- RG42 : Un administrateur possède un statut (actif/inactif)
- RG43 : Un administrateur peut demander une réinitialisation de mot de passe
```

- **RG44 :** Un administrateur peut créer **0 ou n événements**
- **RG45 :** Un administrateur peut créer **0 ou n commentaires**
- **RG46 :** Un administrateur peut avoir **0 ou n sessions**
- **RG47 :** Un administrateur peut recevoir **0 ou n emails**
- **RG48 :** Un administrateur peut valider **0 ou n événements**
- **RG49 :** Un administrateur peut gérer **0 ou n collaborateurs**
- **RG50 :** Un administrateur peut gérer **0 ou n utilisateurs**

## Événement
---
```
- RG51 : Un événement est représenté par un identifiant unique
- RG52 : Un événement possède un titre
- RG53 : Un événement possède une description
- RG54 : Un événement possède une date
- RG55 : Un événement peut avoir une heure de début (optionnel)
- RG56 : Un événement peut avoir une heure de fin (optionnel)
- RG57 : Un événement possède un lieu
- RG58 : Un événement possède un type (anniversaire, convention, tournoi, à domicile, en salle)
- RG59 : Un événement possède une icône pour son type
- RG60 : Un événement possède une couleur pour son type
- RG61 : Un événement peut avoir une image (optionnel)
- RG62 : Un événement possède un statut (en attente, validé, refusé, planifié, en cours, terminé, annulé)
- RG63 : Un événement possède une visibilité (public/privé)
- RG64 : Un événement peut être récurrent (optionnel)
- RG65 : Un événement peut avoir une fréquence de récurrence (quotidienne, hebdomadaire, mensuelle, annuelle)
- RG66 : Un événement peut avoir une date de fin de récurrence
- RG67 : Un événement peut être une proposition (est_proposition)
- RG68 : Un événement qui est une proposition possède une date de soumission
- RG69 : Un événement qui est une proposition possède un email de contact
- RG70 : Un événement qui est une proposition refusée peut avoir un commentaire de refus (optionnel)
```

- **RG71 :** Un événement peut être associé à **0 ou n images**
- **RG72 :** Un événement est créé par **un seul collaborateur ou administrateur**
- **RG73 :** Un événement peut être proposé par **un seul utilisateur**
- **RG74 :** Un événement peut être validé par **un seul collaborateur ou administrateur**
- **RG75 :** Un événement peut avoir **0 ou n inscriptions**
- **RG76 :** Un événement peut avoir **0 ou n commentaires**

## Inscription
---
```
- RG77 : Une inscription est représentée par un identifiant unique
- RG78 : Une inscription possède une date d'inscription
- RG79 : Une inscription possède un statut (en attente, confirmée, annulée)
- RG80 : Une inscription peut avoir des invités supplémentaires (optionnel)
```

- **RG81 :** Une inscription est associée à **un seul événement**
- **RG82 :** Une inscription est associée à **un seul utilisateur**

## Image
---
```
- RG83 : Une image est représentée par un identifiant unique
- RG84 : Une image possède un nom de fichier
- RG85 : Une image possède un chemin d'accès
- RG86 : Une image possède un format
- RG87 : Une image possède une taille
- RG88 : Une image possède une date d'upload
- RG89 : Une image possède un type (photo, bannière, logo)
```

- **RG90 :** Une image est associée à **un seul événement**

## Commentaire
---
```
- RG91 : Un commentaire est représenté par un identifiant unique
- RG92 : Un commentaire possède un contenu
- RG93 : Un commentaire possède une date de création
- RG94 : Un commentaire possède un statut (visible, masqué)
```

- **RG95 :** Un commentaire est associé à **un seul événement**
- **RG96 :** Un commentaire est créé par **un seul utilisateur, collaborateur ou administrateur**

## Session
---
```
- RG97 : Une session est représentée par un identifiant unique
- RG98 : Une session possède un token
- RG99 : Une session possède une date de création
- RG100 : Une session possède une date d'expiration
- RG101 : Une session possède un statut (active/expirée)
- RG102 : Une session possède une adresse IP
- RG103 : Une session possède un navigateur
```

- **RG104 :** Une session est associée à **un seul utilisateur, collaborateur ou administrateur**

## Email
---
```
- RG105 : Un email est représenté par un identifiant unique
- RG106 : Un email possède un destinataire
- RG107 : Un email possède un sujet
- RG108 : Un email possède un contenu
- RG109 : Un email possède une date d'envoi
- RG110 : Un email possède un statut (en attente, envoyé, échoué)
- RG111 : Un email possède un type (notification, réinitialisation mot de passe, invitation collaborateur, confirmation proposition)
- RG112 : Un email possède un template
- RG113 : Un email possède des variables de template
- RG114 : Un email d'invitation contient un lien unique et temporaire pour créer un compte
- RG115 : Un email de réinitialisation contient un lien unique et temporaire pour réinitialiser le mot de passe
```

- **RG116 :** Un email est associé à **un seul utilisateur, collaborateur ou administrateur**
- **RG117 :** Un email peut être associé à **un seul événement** (optionnel)
- **RG118 :** Un email d'invitation est envoyé par **un seul administrateur**
- **RG119 :** Un email de confirmation de proposition est envoyé à **un utilisateur non inscrit**

