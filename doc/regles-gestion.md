-------------------------------------------------------------
----------------------REGLES DE GESTION----------------------
-------------------------------------------------------------

## Visiteur
---
```
- RG01 : Un visiteur est une personne non enregistrée dans le système
- RG02 : Un visiteur peut consulter les événements publics
- RG03 : Un visiteur peut s'inscrire pour devenir membre
- RG04 : Un visiteur peut partager des événements publics sur les réseaux sociaux
```

## Membre (Inscrit)
---
```
- RG05 : Un membre est représenté par un identifiant unique
- RG06 : Un membre possède un nom
- RG07 : Un membre possède un prénom
- RG08 : Un membre possède un email
- RG09 : Un membre possède un mot de passe (hashé)
- RG10 : Un membre possède une date d'inscription
- RG11 : Un membre possède une date de dernière connexion
- RG12 : Un membre possède un statut (actif/inactif)
- RG13 : Un membre peut demander une réinitialisation de mot de passe
```

- **RG14 :** Un membre peut consulter **tous les événements**
- **RG15 :** Un membre peut s'inscrire à **0 ou n événements**
- **RG16 :** Un membre peut recevoir **des notifications par email**
- **RG17 :** Un membre peut partager **des événements sur les réseaux sociaux**

## Collaborateur
---
```
- RG18 : Un collaborateur est représenté par un identifiant unique
- RG19 : Un collaborateur possède un nom
- RG20 : Un collaborateur possède un prénom
- RG21 : Un collaborateur possède un email
- RG22 : Un collaborateur possède un mot de passe (hashé)
- RG23 : Un collaborateur possède une photo de profil
- RG24 : Un collaborateur possède une description
- RG25 : Un collaborateur possède un ordre d'affichage dans la section "Qui sommes-nous"
- RG26 : Un collaborateur possède une date de création
- RG27 : Un collaborateur possède une date de dernière connexion
- RG28 : Un collaborateur possède un statut (actif/inactif)
- RG29 : Un collaborateur peut demander une réinitialisation de mot de passe
- RG30 : Un collaborateur doit être créé par un administrateur
```

- **RG31 :** Un collaborateur peut créer **0 ou n événements**
- **RG32 :** Un collaborateur peut modifier **0 ou n événements**
- **RG33 :** Un collaborateur peut supprimer **0 ou n événements**
- **RG34 :** Un collaborateur peut avoir **0 ou n sessions**
- **RG35 :** Un collaborateur peut être **supprimé par un administrateur**
- **RG36 :** Un collaborateur peut partager **des événements sur les réseaux sociaux**

## Administrateur
---
```
- RG37 : Un administrateur est représenté par un identifiant unique
- RG38 : Un administrateur possède un nom
- RG39 : Un administrateur possède un prénom
- RG40 : Un administrateur possède un email
- RG41 : Un administrateur possède un mot de passe (hashé)
- RG42 : Un administrateur possède une photo de profil
- RG43 : Un administrateur possède une description
- RG44 : Un administrateur possède un ordre d'affichage dans la section "Qui sommes-nous"
- RG45 : Un administrateur possède une date de création
- RG46 : Un administrateur possède une date de dernière connexion
- RG47 : Un administrateur possède un statut (actif/inactif)
- RG48 : Un administrateur peut demander une réinitialisation de mot de passe
```

- **RG49 :** Un administrateur peut créer **0 ou n événements**
- **RG50 :** Un administrateur peut modifier **0 ou n événements**
- **RG51 :** Un administrateur peut supprimer **0 ou n événements**
- **RG52 :** Un administrateur peut gérer **0 ou n collaborateurs**
- **RG53 :** Un administrateur peut gérer **0 ou n membres**
- **RG54 :** Un administrateur peut avoir **0 ou n sessions**
- **RG55 :** Un administrateur **ne peut pas être supprimé**
- **RG56 :** Un administrateur peut envoyer **des invitations par email** pour créer des collaborateurs
- **RG57 :** Un administrateur peut partager **des événements sur les réseaux sociaux**

## Événement
---
```
- RG58 : Un événement est représenté par un identifiant unique
- RG59 : Un événement possède un titre
- RG60 : Un événement possède une description
- RG61 : Un événement possède une date
- RG62 : Un événement peut avoir une heure de début (optionnel)
- RG63 : Un événement peut avoir une heure de fin (optionnel)
- RG64 : Un événement possède un lieu
- RG65 : Un événement possède un type (anniversaire, convention, tournoi, à domicile, en salle)
- RG66 : Un événement peut avoir une image (optionnel)
- RG67 : Un événement possède un statut (planifié, en cours, terminé, annulé)
- RG68 : Un événement possède une visibilité (public/privé)
- RG69 : Un événement peut être récurrent (optionnel)
- RG70 : Un événement peut avoir une fréquence de récurrence (quotidienne, hebdomadaire, mensuelle, annuelle)
- RG71 : Un événement peut avoir une date de fin de récurrence
```

- **RG72 :** Un événement est associé à **un seul type d'événement**
- **RG73 :** Un événement peut être associé à **0 ou n images**
- **RG74 :** Un événement est créé par **un seul collaborateur ou administrateur**
- **RG75 :** Un événement peut avoir **0 ou n inscriptions**
- **RG76 :** Un événement peut avoir **0 ou n commentaires**

## Type d'Événement
---
```
- RG77 : Un type d'événement est représenté par un identifiant unique
- RG78 : Un type d'événement possède un nom
- RG79 : Un type d'événement possède une icône
- RG80 : Un type d'événement possède une couleur
```

- **RG81 :** Un type d'événement peut contenir **0 ou n événements**

## Inscription
---
```
- RG82 : Une inscription est représentée par un identifiant unique
- RG83 : Une inscription possède une date d'inscription
- RG84 : Une inscription possède un statut (en attente, confirmée, annulée)
- RG85 : Une inscription peut avoir des invités supplémentaires (optionnel)
```

- **RG86 :** Une inscription est associée à **un seul événement**
- **RG87 :** Une inscription est associée à **un seul membre**

## Image
---
```
- RG88 : Une image est représentée par un identifiant unique
- RG89 : Une image possède un nom de fichier
- RG90 : Une image possède un chemin d'accès
- RG91 : Une image possède un format
- RG92 : Une image possède une taille
- RG93 : Une image possède une date d'upload
- RG94 : Une image possède un type (photo, bannière, logo)
```

- **RG95 :** Une image est associée à **un seul événement**

## Commentaire
---
```
- RG96 : Un commentaire est représenté par un identifiant unique
- RG97 : Un commentaire possède un contenu
- RG98 : Un commentaire possède une date de création
- RG99 : Un commentaire possède un statut (visible, masqué)
```

- **RG100 :** Un commentaire est associé à **un seul événement**
- **RG101 :** Un commentaire est créé par **un seul membre, collaborateur ou administrateur**

## Session
---
```
- RG102 : Une session est représentée par un identifiant unique
- RG103 : Une session possède un token
- RG104 : Une session possède une date de création
- RG105 : Une session possède une date d'expiration
- RG106 : Une session possède un statut (active/expirée)
- RG107 : Une session possède une adresse IP
- RG108 : Une session possède un navigateur
```

- **RG109 :** Une session est associée à **un seul collaborateur ou administrateur**

## Email
---
```
- RG110 : Un email est représenté par un identifiant unique
- RG111 : Un email possède un destinataire
- RG112 : Un email possède un sujet
- RG113 : Un email possède un contenu
- RG114 : Un email possède une date d'envoi
- RG115 : Un email possède un statut (en attente, envoyé, échoué)
- RG116 : Un email possède un type (notification, réinitialisation mot de passe, invitation collaborateur)
- RG117 : Un email possède un template
- RG118 : Un email possède des variables de template
- RG119 : Un email d'invitation contient un lien unique et temporaire pour créer un compte
- RG120 : Un email de réinitialisation contient un lien unique et temporaire pour réinitialiser le mot de passe
- RG121 : Un email peut avoir des pièces jointes (optionnel)
```

- **RG122 :** Un email est associé à **un seul membre, collaborateur ou administrateur**
- **RG123 :** Un email peut être associé à **un seul événement** (optionnel)
- **RG124 :** Un email d'invitation est envoyé par **un seul administrateur**

## Pièce jointe
---
```
- RG125 : Une pièce jointe est représentée par un identifiant unique
- RG126 : Une pièce jointe possède un nom de fichier
- RG127 : Une pièce jointe possède un chemin d'accès
- RG128 : Une pièce jointe possède un format
- RG129 : Une pièce jointe possède une taille
- RG130 : Une pièce jointe possède une date d'upload
```

- **RG131 :** Une pièce jointe est associée à **un seul email**

