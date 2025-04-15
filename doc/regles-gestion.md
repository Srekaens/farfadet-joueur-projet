-------------------------------------------------------------
----------------------REGLES DE GESTION----------------------
-------------------------------------------------------------

## Visiteur
---
```
- RG01 : Un visiteur est identifié par un identifiant unique
```

- **RG02 :** Un visiteur **peut devenir 0 ou n client**

---

## Collaborateur
---
```
- RG03 : Un collaborateur est identifié par un identifiant unique
- RG04 : Un collaborateur possède un nom
- RG05 : Un collaborateur possède un prénom
- RG06 : Un collaborateur possède un email
- RG07 : Un collaborateur possède un mot de passe 
- RG08 : Un collaborateur possède une photo de profil (optionnel)
- RG09 : Un collaborateur possède une description (optionnel)
- RG11 : Un collaborateur possède une date de création
```
<!-- - RG13 : Un collaborateur possède un statut (actif/inactif) -->
<!-- - RG12 : Un collaborateur possède une date de dernière connexion -->

- **RG14 :** Un collaborateur **peut créer 0 ou n événements**
- **RG15 :** Un collaborateur **peut gérer 0 ou n réservations**

---

## Administrateur
---
```
- RG16 : Un administrateur est identifié par un identifiant unique
- RG17 : Un administrateur possède un nom
- RG18 : Un administrateur possède un prénom
- RG19 : Un administrateur possède un email
- RG20 : Un administrateur possède un mot de passe
- RG21 : Un administrateur possède une photo de profil (optionnel)
- RG22 : Un administrateur possède une description (optionnel)
- RG23 : Un administrateur possède un ordre d'affichage dans la section "Qui sommes-nous" (optionnel)
- RG24 : Un administrateur possède une date de création
```
<!-- - RG25 : Un administrateur possède une date de dernière connexion
- RG26 : Un administrateur possède un statut (actif/inactif) -->

- **RG27 :** Un administrateur **peut créer 0 ou n événements**
- **RG28 :** Un administrateur **peut gérer 0 ou n collaborateurs**
- **RG29 :** Un administrateur **peut gérer 0 ou n réservations**

---

## Événement
---
```
- RG30 : Un événement est identifié par un identifiant unique
- RG31 : Un événement possède un titre
- RG32 : Un événement possède une description
- RG33 : Un événement possède une date
- RG34 : Un événement peut avoir une heure de début (optionnel)
- RG35 : Un événement peut avoir une heure de fin (optionnel)
- RG36 : Un événement possède un lieu
- RG37 : Un événement possède un type (anniversaire, convention, tournoi, à domicile, en salle)
- RG38 : Un événement possède une icône pour son type
- RG39 : Un événement possède une couleur pour son type
- RG40 : Un événement possède un statut (planifié, en cours, terminé, annulé)
- RG45 : Un événement peut avoir un nombre maximum de participants
- RG46 : Un événement peut avoir un prix (optionnel)
```
<!-- - RG42 : Un événement peut être récurrent (optionnel)
- RG43 : Un événement peut avoir une fréquence de récurrence (quotidienne, hebdomadaire, mensuelle, annuelle) -->

- **RG48 :** Un événement **peut être associé à 0 ou n images**
- **RG49 :** Un événement **est créé par un seul collaborateur ou administrateur**
- **RG50 :** Un événement **peut avoir 0 ou n réservations**

---

## Client
---
```
- RG51 : Un client est identifié par un identifiant unique
- RG52 : Un client possède un nom
- RG53 : Un client possède un prénom
- RG54 : Un client possède un email
- RG55 : Un client possède un numéro de téléphone (optionnel)
- RG56 : Un client possède une date d'inscription
```
<!-- - RG57 : Un client possède un statut (inscrit, confirmé, annulé) -->

- **RG58 :** Un client **peut être associé à 0 ou n événements**
- **RG59 :** Un client **peut être un visiteur**

---

## Réservation
---
```
- RG66 : Une réservation est identifiée par un identifiant unique
- RG67 : Une réservation possède une date de création
- RG69 : Une réservation possède un nombre de participants
- RG70 : Une réservation peut avoir un commentaire (optionnel)
```
<!-- - RG71 : Une réservation peut avoir un mode de réservation (en ligne, par téléphone) -->
<!-- - RG68 : Une réservation possède un statut (en attente, confirmée, annulée) -->

- **RG75 :** Une réservation **est associée à un seul événement**
- **RG76 :** Une réservation **est associée à un seul client**
- **RG77 :** Une réservation **peut être gérée par un seul collaborateur ou administrateur**
- **RG78 :** Une réservation **peut être confirmée par un seul collaborateur ou administrateur**

---

## Image
---
```
- RG79 : Une image est identifiée par un identifiant unique
- RG80 : Une image possède un nom de fichier
- RG81 : Une image possède un chemin d'accès
- RG82 : Une image possède un format
- RG83 : Une image possède une taille
- RG84 : Une image possède une date d'upload
- RG85 : Une image possède un type (photo, bannière, logo)
```

- **RG86 :** Une image **est associée à un seul événement**

## Email
---
```
- RG87 : Un email est identifié par un identifiant unique
- RG89 : Un email possède un sujet
- RG90 : Un email possède un contenu HTML
- RG91 : Un email possède un contenu texte
- RG92 : Un email possède une date d'envoi
- RG94 : Un email possède un destinataire
```
<!-- - RG93 : Un email possède un statut (en attente, envoyé, échoué) -->
<!-- - RG88 : Un email possède un type (confirmation de réservation, rappel, annulation) -->

- **RG95 :** Un email **peut être associé à une seule réservation**
