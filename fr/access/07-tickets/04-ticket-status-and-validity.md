---
title: "Statut et Validité des Tickets"
---

{/* keywords: statut ticket, ticket actif, ticket expiré, expire bientôt, ticket révoqué, validité ticket */}
{/* category: Tickets */}
{/* audience: Admins, Managers, Security */}

Chaque ticket possède un statut qui reflète sa validité actuelle. Les statuts sont calculés automatiquement à partir de la date d'expiration du ticket et de son état enregistré — aucune mise à jour manuelle n'est requise.

![Liste des tickets montrant des tickets avec différents statuts incluant actif, expire bientôt et expiré](../screenshots/tickets-list.png)

---

## Aperçu des Statuts

| Statut             | Couleur | Signification                                                   |
| ------------------ | ------- | --------------------------------------------------------------- |
| **Actif**          | Vert    | Le ticket est valide et se trouve dans sa fenêtre de validité   |
| **Expire Bientôt** | Ambre   | Le ticket est valide mais expire dans les 3 prochains jours     |
| **Expiré**         | Gris    | La fenêtre de validité est passée — le ticket n'est plus valide |
| **Révoqué**        | Rouge   | Le ticket a été annulé manuellement par un administrateur       |

---

## Actif

Un ticket est **Actif** lorsque :

- Son statut enregistré est `active`, **et**
- Soit il n'a pas de date d'expiration, soit l'heure actuelle est antérieure à la date "valide jusqu'au".

Les tickets actifs sont pleinement valides et la page de vérification affichera une confirmation d'accès dans la couleur de la marque de votre organisation.

---

## Expire Bientôt

Un ticket est en statut **Expire Bientôt** lorsqu'il est encore actif mais que sa date "valide jusqu'au" se situe **dans les 3 jours** à venir. Ce statut aide les administrateurs à identifier les tickets qui doivent être renouvelés avant leur expiration.

La page de vérification affiche un badge de statut ambre pour les tickets expirant bientôt.

---

## Expiré

Un ticket est **Expiré** lorsque sa date "valide jusqu'au" est passée. L'expiration est automatique — aucune action de l'administrateur n'est requise.

- La ligne du ticket dans la liste d'administration est affichée avec une opacité réduite et un fond gris.
- La page de vérification affiche un badge **Expiré** en ambre.
- Les tickets expirés ne peuvent pas être révoqués (l'action Révoquer est masquée pour eux).

> **Note :** L'expiration est calculée côté client au moment de l'affichage. L'enregistrement du ticket conserve le statut `status: "active"` dans la base de données — seul le statut affiché change en "Expiré".

---

## Révoqué

Un ticket est **Révoqué** lorsqu'un administrateur l'a annulé manuellement à l'aide de l'action **Révoquer**. La révocation définit le statut enregistré du ticket sur `used`, ce qui l'invalide immédiatement.

- La page de vérification affiche un badge **Révoqué** en rouge.
- La date "valide jusqu'au" est affichée barrée.
- Les tickets révoqués ne peuvent pas être révoqués à nouveau.

**Quand révoquer :**

- L'employé n'a plus besoin du laissez-passer avant son expiration.
- Le ticket a été émis par erreur.
- L'employé a été licencié ou suspendu.

---

## Tickets qui n'expirent jamais

Si un ticket a été créé avec la case **Le ticket expire** décochée, il n'a pas de date "valide jusqu'au". Ces tickets restent **Actifs** indéfiniment jusqu'à ce qu'ils soient manuellement **Révoqués** ou **Supprimés**.

Sur la page de vérification, le champ de validité affiche le texte **"N'expire jamais"** en vert.

---

## Filtrer par Statut

Dans la liste des **Tickets**, utilisez la barre d'onglets de statut au-dessus du tableau pour filtrer :

- **Tous** — affiche tous les tickets quel que soit leur statut.
- **Actifs** — uniquement les tickets actuellement valides (inclut "Expire bientôt").
- **Expire bientôt** — tickets qui expirent dans les 3 jours.
- **Expirés** — tickets dont la fenêtre de validité est passée.
