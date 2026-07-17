---
title: "Gérer les Badges Visiteurs — Révocation et Suppression"
---

{/* keywords: révoquer badge visiteur, supprimer badge visiteur, révocation groupée, suppression groupée, gérer laissez-passer visiteurs, annuler badge */}
{/* category: Guest Badges */}
{/* audience: Admins, Managers */}

Cet article explique comment révoquer ou supprimer les badges visiteurs individuellement ou par lots, et comment filtrer la liste pour trouver ce dont vous avez besoin.

![Liste des Badges Visiteurs avec plusieurs lignes sélectionnées et le menu déroulant Actions ouvert](../screenshots/guest-badges-list.png)

---

## Actions Individuelles

Pour tout badge individuel, cliquez sur le **menu à trois points (⋮)** à la fin de sa ligne pour accéder à :

| Action             | Disponibilité            | Description                                                  |
| ------------------ | ------------------------ | ------------------------------------------------------------ |
| **Voir le Badge**  | Toujours                 | Ouvre la page de vérification publique dans un nouvel onglet |
| **Copier le Lien** | Toujours                 | Copie l'URL du badge dans votre presse-papiers               |
| **Révoquer**       | Badges actifs uniquement | Marque le badge comme révoqué (action irréversible)          |
| **Supprimer**      | Toujours                 | Supprime définitivement l'enregistrement du badge            |

### Révoquer un seul badge

1. Cliquez sur **⋮** sur la ligne du badge.
2. Sélectionnez **Révoquer**.
3. Confirmez dans la boîte de dialogue.

Le badge est immédiatement invalidé. La révocation est enregistrée avec votre nom et l'horodatage actuel.

### Supprimer un seul badge

1. Cliquez sur **⋮** sur la ligne du badge.
2. Sélectionnez **Supprimer**.
3. Confirmez dans la boîte de dialogue.

L'enregistrement du badge et son lien sont définitivement supprimés. Tout visiteur tentant d'ouvrir le lien verra une erreur "page non trouvée".

> **Révoquer vs Supprimer :** La révocation conserve l'enregistrement du badge visible dans la liste d'administration (utile pour les pistes d'audit). La suppression le retire entièrement.

---

## Actions Groupées

Pour gérer plusieurs badges à la fois :

1. Cochez la **case à cocher** sur chaque ligne que vous souhaitez sélectionner, ou utilisez la **case à cocher de l'en-tête** pour sélectionner toutes les lignes de la page actuelle.
2. La barre d'actions en haut du tableau change pour afficher **N sélectionné(s)** et un bouton **Actions**.
3. Cliquez sur **Actions** et choisissez :

| Action Groupée | S'applique à                                  | Comportement                                                     |
| -------------- | --------------------------------------------- | ---------------------------------------------------------------- |
| **Révoquer**   | Uniquement les badges **Actifs** sélectionnés | Les badges non actifs de la sélection sont ignorés               |
| **Supprimer**  | Tous les badges sélectionnés                  | Supprime tous les badges sélectionnés, quel que soit leur statut |

Ces deux actions affichent une boîte de dialogue de confirmation avant de continuer. Appuyez sur **Échap** pour annuler la sélection sans apporter de modifications.

---

## Filtrer la Liste

Utilisez le filtre de statut (au-dessus du tableau) pour restreindre la liste à un statut spécifique :

- **Tous** — affiche tous les badges.
- **Actifs** — badges actuellement valides.
- **Expirés** — badges dont la fenêtre de validité est passée.
- **Révoqués** — badges annulés manuellement.

Le filtrage est utile pour :

- **Supprimer en masse les anciens badges expirés** — filtrez par Expiré, tout sélectionner, supprimer.
- **Trouver et révoquer un badge actif spécifique** — filtrez par Actif, recherchez par nom.
- **Auditer qui était sur site** — filtrez par plage de dates ou par statut.

---

## Pagination

La liste affiche par défaut **10 lignes par page**. Utilisez le sélecteur de lignes par page (10 / 25 / 50 / 100) pour afficher plus de badges à la fois, ou naviguez entre les pages à l'aide des commandes de navigation.
