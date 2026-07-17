---
title: "Créer un Badge Visiteur"
---

{/* keywords: créer badge visiteur, nouveau laissez-passer visiteur, invitation visiteur, inviter visiteur, ajouter visiteur */}
{/* category: Guest Badges */}
{/* audience: Admins, Managers, Reception */}

Cet article détaille comment remplir le formulaire de création d'un Badge Visiteur et envoyer l'invitation.

![Fenêtre modale Créer un Badge Visiteur montrant les détails du visiteur, les détails de la visite et les champs d'adresse](../screenshots/create-guest-badge-modal.png)

---

## Ouverture de la Fenêtre de Création

1. Naviguez vers **Badges Visiteurs** dans la barre latérale.
2. Cliquez sur le bouton **Nouveau Badge Visiteur** (ou **+ Ajouter**) dans le coin supérieur droit.
3. La fenêtre modale **Créer un Badge Visiteur** s'ouvre.

---

## Étape 1 — Détails du Visiteur

Saisissez les informations relatives à la personne (ou aux personnes) que vous invitez.

| Champ          | Requis    | Notes                                            |
| -------------- | --------- | ------------------------------------------------ |
| **Nom**        | ✓         | Nom complet du visiteur                          |
| **Email**      | ✓         | L'e-mail d'invitation est envoyé à cette adresse |
| **Entreprise** | Optionnel | Affiché sur la page de vérification              |

### Inviter plusieurs visiteurs à la fois

Vous pouvez créer jusqu'à **10 badges visiteurs en une seule soumission** :

1. Remplissez les détails du premier visiteur.
2. Cliquez sur **Ajouter un Visiteur** pour ajouter une autre ligne.
3. Répétez l'opération jusqu'à 10 visiteurs.
4. Utilisez l'icône de corbeille sur n'importe quelle ligne pour supprimer un visiteur.

Chaque visiteur de la liste reçoit son propre lien de badge unique.

---

## Étape 2 — Détails de la Visite

Définissez la période de validité du badge et le motif de la visite.

| Champ               | Par défaut          | Options                                                         |
| ------------------- | ------------------- | --------------------------------------------------------------- |
| **Motif**           | —                   | Visite de site, Entretien, Réunion, Livraison, Événement, Autre |
| **Valide du**       | Date/heure actuelle | Toute date ultérieure ou présente                               |
| **Valide jusqu'au** | Dans 24 heures      | Toute date postérieure à "Valide du"                            |

> **Conseil :** Si vous sélectionnez **Autre** comme motif, un champ de texte libre apparaît pour vous permettre de saisir une raison personnalisée.

---

## Étape 3 — Zones d'Accès Autorisées (Optionnel)

Si votre organisation a défini des **zones d'accès**, une liste de badges de zones apparaît ici. Cliquez sur une zone pour l'activer ou la désactiver. Seules les zones sélectionnées seront affichées sur la page de vérification du visiteur.

Cette section est masquée si aucune zone n'a été configurée.

---

## Étape 4 — Adresse / Localisation (Optionnel)

Ajoutez une adresse pour aider le visiteur à se rendre au bon endroit. Ceci est particulièrement utile pour les grands campus ou les sites multi-bâtiments.

- **Nom de l'adresse** — un libellé court (ex: "Entrée principale", "Réception Bâtiment B").
- **Lien Maps** — une URL directe vers Google Maps ou tout autre service de cartographie.
- Cliquez sur **Rechercher sur Google Maps** pour ouvrir une recherche Maps dans un nouvel onglet et copier le lien.

Vous pouvez ajouter plusieurs adresses. La **dernière adresse utilisée est mémorisée** d'une session à l'autre — la prochaine fois que vous ouvrirez la fenêtre modale, les champs d'adresse seront pré-remplis.

---

## Étape 5 — Notes (Optionnel)

Utilisez le champ **Notes** pour toute instruction ou contexte supplémentaire destiné au visiteur (ex: "Veuillez apporter une pièce d'identité avec photo", "Parking disponible au Lot C"). Les notes sont enregistrées dans le dossier du badge mais ne sont pas affichées sur la page de vérification publique.

---

## Envoi de l'Invitation

Une fois tous les champs obligatoires remplis :

- **"Envoyer l'Invitation"** — apparaît lorsque vous avez saisi un visiteur.
- **"Envoyer N Invitations"** — apparaît lorsque vous avez plusieurs visiteurs dans la liste (N = nombre).

Cliquez sur le bouton pour :

1. Créer les enregistrements de badges dans la base de données pour tous les visiteurs.
2. Envoyer à chaque visiteur un e-mail contenant son lien de badge unique.
3. Fermer la fenêtre modale et actualiser la liste des Badges Visiteurs.

### Que se passe-t-il si un e-mail échoue ?

Si une adresse e-mail est invalide et que l'invitation échoue (bounce), le badge est tout de même créé avec succès. La ligne du visiteur sera surlignée en ambre pour indiquer l'échec d'envoi. Vous pouvez toujours copier le lien du badge manuellement et le partager par un autre moyen.
