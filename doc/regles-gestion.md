-------------------------------------------------------------
----------------------REGLES DE GESTION----------------------
-------------------------------------------------------------

## Visiteur
---
```
- RG01 : Un visiteur est identifié par un identifiant unique
- RG02 : Un visiteur possède une date de première visite
- RG03 : Un visiteur possède une date de dernière visite
- RG04 : Un visiteur possède une adresse IP
- RG05 : Un visiteur possède un navigateur
```

- **RG06 :** Un visiteur **peut proposer 0 ou n propositions**
- **RG07 :** Un visiteur **peut devenir 0 ou n participant**

---

## Collaborateur
---
```
- RG08 : Un collaborateur est identifié par un identifiant unique
- RG09 : Un collaborateur possède un nom
- RG10 : Un collaborateur possède un prénom
- RG11 : Un collaborateur possède un email
- RG12 : Un collaborateur possède un mot de passe (hashé)
- RG13 : Un collaborateur possède une photo de profil (optionnel)
- RG14 : Un collaborateur possède une description (optionnel)
- RG15 : Un collaborateur possède un ordre d'affichage dans la section "Qui sommes-nous" (optionnel)
- RG16 : Un collaborateur possède une date de création
- RG17 : Un collaborateur possède une date de dernière connexion
- RG18 : Un collaborateur possède un statut (actif/inactif)
```

- **RG19 :** Un collaborateur **peut créer 0 ou n événements**
- **RG20 :** Un collaborateur **peut valider 0 ou n propositions**
- **RG21 :** Un collaborateur **peut gérer 0 ou n réservations**

---

## Administrateur
---
```
- RG22 : Un administrateur est identifié par un identifiant unique
- RG23 : Un administrateur possède un nom
- RG24 : Un administrateur possède un prénom
- RG25 : Un administrateur possède un email
- RG26 : Un administrateur possède un mot de passe (hashé)
- RG27 : Un administrateur possède une photo de profil (optionnel)
- RG28 : Un administrateur possède une description (optionnel)
- RG29 : Un administrateur possède un ordre d'affichage dans la section "Qui sommes-nous" (optionnel)
- RG30 : Un administrateur possède une date de création
- RG31 : Un administrateur possède une date de dernière connexion
- RG32 : Un administrateur possède un statut (actif/inactif)
```

- **RG33 :** Un administrateur **peut créer 0 ou n événements**
- **RG34 :** Un administrateur **peut valider 0 ou n propositions**
- **RG35 :** Un administrateur **peut gérer 0 ou n collaborateurs**
- **RG36 :** Un administrateur **peut gérer 0 ou n réservations**

---

## Événement
---
```
- RG37 : Un événement est identifié par un identifiant unique
- RG38 : Un événement possède un titre
- RG39 : Un événement possède une description
- RG40 : Un événement possède une date
- RG41 : Un événement peut avoir une heure de début (optionnel)
- RG42 : Un événement peut avoir une heure de fin (optionnel)
- RG43 : Un événement possède un lieu
- RG44 : Un événement possède un type (anniversaire, convention, tournoi, à domicile, en salle)
- RG45 : Un événement possède une icône pour son type
- RG46 : Un événement possède une couleur pour son type
- RG47 : Un événement possède un statut (planifié, en cours, terminé, annulé)
- RG48 : Un événement possède une visibilité (public/privé)
- RG49 : Un événement peut être récurrent (optionnel)
- RG50 : Un événement peut avoir une fréquence de récurrence (quotidienne, hebdomadaire, mensuelle, annuelle)
- RG51 : Un événement peut avoir une date de fin de récurrence
- RG52 : Un événement peut avoir un nombre maximum de participants
- RG53 : Un événement peut avoir un prix (optionnel)
- RG54 : Un événement peut avoir des modalités de réservation (en ligne, par téléphone, les deux)
```

- **RG55 :** Un événement **peut être associé à 0 ou n images**
- **RG56 :** Un événement **est créé par un seul collaborateur ou administrateur**
- **RG57 :** Un événement **peut avoir 0 ou n réservations**

---

## Proposition
---
```
- RG58 : Une proposition est identifiée par un identifiant unique
- RG59 : Une proposition possède un titre
- RG60 : Une proposition possède une description
- RG61 : Une proposition possède une date
- RG62 : Une proposition peut avoir une heure de début (optionnel)
- RG63 : Une proposition peut avoir une heure de fin (optionnel)
- RG64 : Une proposition possède un lieu
- RG65 : Une proposition possède un type (anniversaire, convention, tournoi, à domicile, en salle)
- RG66 : Une proposition possède une date de soumission
- RG67 : Une proposition possède un email de contact
- RG68 : Une proposition possède un statut (en attente, validée, refusée)
- RG69 : Une proposition refusée peut avoir un commentaire de refus (optionnel)
```

- **RG70 :** Une proposition **est créée par un seul visiteur**
- **RG71 :** Une proposition **peut être validée par un seul collaborateur ou administrateur**
- **RG72 :** Une proposition validée **devient un seul événement**

---

## Participant
---
```
- RG73 : Un participant est identifié par un identifiant unique
- RG74 : Un participant possède un nom
- RG75 : Un participant possède un prénom
- RG76 : Un participant possède un email (optionnel)
- RG77 : Un participant possède un numéro de téléphone (optionnel)
- RG78 : Un participant possède une date d'inscription
- RG79 : Un participant possède un statut (inscrit, confirmé, annulé)
```

- **RG80 :** Un participant **peut être associé à 0 ou n événements**
- **RG81 :** Un participant **peut avoir 0 ou n accompagnants**
- **RG82 :** Un participant **peut être un visiteur**

---

## Accompagnant
---
```
- RG83 : Un accompagnant est identifié par un identifiant unique
- RG84 : Un accompagnant possède un nom
- RG85 : Un accompagnant possède un prénom
- RG86 : Un accompagnant possède un âge (optionnel)
```

- **RG87 :** Un accompagnant **est associé à un seul participant**

---

## Réservation
---
```
- RG88 : Une réservation est identifiée par un identifiant unique
- RG89 : Une réservation possède une date de création
- RG90 : Une réservation possède un statut (en attente, confirmée, annulée)
- RG91 : Une réservation possède un nombre total de participants (participant + accompagnants)
- RG92 : Une réservation peut avoir un commentaire (optionnel)
- RG93 : Une réservation peut avoir un mode de réservation (en ligne, par téléphone)
- RG94 : Une réservation peut avoir un montant payé (optionnel)
- RG95 : Une réservation peut avoir une date de paiement (optionnel)
- RG96 : Une réservation peut avoir un mode de paiement (espèces, carte bancaire, virement, etc.)
```

- **RG97 :** Une réservation **est associée à un seul événement**
- **RG98 :** Une réservation **est associée à un seul participant**
- **RG99 :** Une réservation **peut être gérée par un seul collaborateur ou administrateur**
- **RG100 :** Une réservation **peut être confirmée par un seul collaborateur ou administrateur**

---

## Image
---
```
- RG101 : Une image est identifiée par un identifiant unique
- RG102 : Une image possède un nom de fichier
- RG103 : Une image possède un chemin d'accès
- RG104 : Une image possède un format
- RG105 : Une image possède une taille
- RG106 : Une image possède une date d'upload
- RG107 : Une image possède un type (photo, bannière, logo)
```

- **RG108 :** Une image **est associée à un seul événement**

---

# ╭─━━━━━─╯ Brief ╰─━━━━━─╮ 

```
- Un visiteur peut proposer des événements qui seront validés par un collaborateur ou un administrateur.
- Un visiteur peut devenir participant à un événement.
- Un participant peut ajouter des accompagnants.
- Le nombre total de participants (participant + accompagnants) ne peut pas dépasser le maximum autorisé pour l'événement.
- Les participants peuvent être confirmés ou annulés par les collaborateurs ou administrateurs.
- Les réservations sont créées lorsqu'un participant s'inscrit à un événement.
- Les réservations peuvent être faites en ligne ou par téléphone.
- Les réservations sont en attente jusqu'à confirmation.
- Les réservations peuvent inclure des paiements.
- Les collaborateurs et administrateurs gèrent et confirment les réservations.
- Les événements peuvent avoir plusieurs images associées.
- Les événements peuvent être publics ou privés.
- Les événements peuvent être récurrents avec différentes fréquences.
- Les événements peuvent avoir un nombre maximum de participants.
- Les événements peuvent avoir un prix et des modalités de réservation.
```

