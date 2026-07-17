---
title: "Vérifier un Ticket via QR"
---

{/* keywords: vérification de ticket, vérifier ticket, ticket code QR, lien ticket, scanner ticket, page publique ticket */}
{/* category: Tickets */}
{/* audience: Admins, Security, Operators */}

Chaque ticket possède un lien de vérification public unique qui peut être ouvert ou scanné par n'importe qui — aucune connexion n'est requise. C'est ainsi que le personnel de sécurité ou les organisateurs d'événements confirment qu'un ticket est authentique et actuellement valide.

---

## L'URL de Vérification du Ticket

Chaque ticket est accessible à l'adresse suivante :

```
https://idpage.link/ticket/{ticketId}
```

Où `{ticketId}` est un identifiant unique au format `TKT-A1B2C3D4E5`. Cette URL est permanente et reflète toujours le statut actuel du ticket.

---

## Copier le Lien du Ticket

Pour obtenir le lien d'un ticket spécifique :

1. Naviguez vers **Tickets** dans le panneau d'administration.
2. Trouvez la ligne du ticket.
3. Cliquez sur le **menu à trois points (⋮)**.
4. Sélectionnez **Copier le Lien**.

Le lien est copié dans votre presse-papiers. Vous pouvez le partager par e-mail, SMS, WhatsApp ou l'imprimer sur un document. Le lien contient également un code QR intégré lorsque la page est ouverte — cela permet au destinataire de présenter la page sur son téléphone pour le scan.

---

## Ce que la Page de Vérification Affiche

Lorsqu'on ouvre un lien de ticket, on accède à une page de vérification claire comportant :

| Élément                    | Détails                                                                                 |
| -------------------------- | --------------------------------------------------------------------------------------- |
| **Logo de l'organisation** | Extrait de vos paramètres whitelabel                                                    |
| **Badge de statut**        | "Ticket Valide" / "Expire Bientôt" / "Expiré" / "Révoqué"                               |
| **Titre du ticket**        | Le titre saisi lors de l'émission du ticket                                             |
| **Type de ticket**         | Point de couleur + nom du type (ex : "● Repas")                                         |
| **Description**            | Affichée uniquement si une description a été saisie                                     |
| **Émis à**                 | Nom complet et département de l'employé                                                 |
| **Valide jusqu'au**        | La date d'expiration, ou "N'expire jamais" en vert si aucune expiration n'a été définie |
| **Emplacement**            | Affiché uniquement si un emplacement a été renseigné                                    |
| **ID du Ticket**           | ID complet au format monospace (ex : `TKT-A1B2C3D4E5`)                                  |
| **Sélecteur de langue**    | Permet à l'utilisateur de changer la langue de la page                                  |

---

## Couleurs de Statut sur la Page de Vérification

La bande de couleur en haut de la carte du ticket et le badge de statut changent en fonction de l'état actuel du ticket :

| Statut         | Couleur                 | Signification                                        |
| -------------- | ----------------------- | ---------------------------------------------------- |
| Valide (Actif) | Couleur de votre marque | Le ticket est valide — autoriser l'entrée ou l'accès |
| Expire Bientôt | Ambre                   | Valide actuellement mais expire dans les 3 jours     |
| Expiré         | Ambre                   | La fenêtre de validité est passée — ne pas accepter  |
| Révoqué        | Rouge                   | Annulé manuellement — ne pas accepter                |

---

## Support de Langue

La page de vérification détecte automatiquement la langue du navigateur du visiteur et affiche le contenu dans la langue correspondante. Langues supportées :

- Anglais
- Arabe (mise en page de droite à gauche)
- Français
- Espagnol
- Allemand

Un **sélecteur de langue** au bas de la page permet un changement manuel.

---

## Ticket Non Trouvé

Si le lien est ouvert avec un ID de ticket invalide ou supprimé, la page affiche une carte d'erreur avec une icône rouge et un message "Ticket non trouvé". Cela peut se produire si le ticket a été **supprimé** du panneau d'administration. Les tickets révoqués ont toujours une page visible — ils affichent le statut Révoqué plutôt qu'une erreur de type "non trouvé".

---

## Utiliser l'App d'Enregistrement pour Vérifier les Tickets

Les codes QR des tickets peuvent également être scannés à l'aide de l'application d'enregistrement Essal (scan.idpage.link) de la même manière que les badges d'employés. La carte de résultat affichera le nom du détenteur du ticket et le résultat de l'accès. Consultez la section Terminaux d'Enregistrement pour les instructions de configuration.
