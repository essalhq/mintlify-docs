---
title: "Révocation et Suppression de Tickets"
---

{/* keywords: révoquer ticket, supprimer ticket, suppression groupée, annuler ticket, retirer ticket */}
{/* category: Tickets */}
{/* audience: Admins, Managers */}

Les tickets peuvent être annulés ou supprimés individuellement ou par lots depuis la vue **Tickets**.

![Liste des tickets montrant les menus d'action de ligne et les cases à cocher sélectionnables pour les opérations groupées](../screenshots/tickets-list.png)

---

## Actions Individuelles sur les Tickets

Cliquez sur le **menu à trois points (⋮)** sur n'importe quelle ligne de ticket pour accéder à :

| Action             | Disponibilité             | Description                                                                                        |
| ------------------ | ------------------------- | -------------------------------------------------------------------------------------------------- |
| **Voir le Ticket** | Toujours                  | Ouvre un panneau de détails affichant tous les champs du ticket et son statut actuel               |
| **Copier le Lien** | Toujours                  | Copie l'URL de vérification publique (`https://idpage.link/ticket/{id}`) dans votre presse-papiers |
| **Révoquer**       | Tickets actifs uniquement | Marque le ticket comme étant utilisé — l'invalide immédiatement. Confirmation requise.             |
| **Supprimer**      | Toujours                  | Supprime définitivement l'enregistrement du ticket du profil de l'employé. Confirmation requise.   |

---

## Révoquer vs Supprimer

|                                            | Révoquer              | Supprimer                       |
| ------------------------------------------ | --------------------- | ------------------------------- |
| Le ticket apparaît toujours dans la liste  | ✓ (comme Révoqué)     | ✗                               |
| La page de vérification se charge toujours | ✓ (affiche "Révoqué") | ✗ (affiche "Ticket non trouvé") |
| Peut être annulé                           | ✗                     | ✗                               |
| Conserve une piste d'audit du ticket       | ✓                     | ✗                               |

**Utilisez Révoquer** lorsque vous souhaitez annuler un ticket tout en conservant l'enregistrement à des fins d'audit ou de référence.

**Utilisez Supprimer** lorsque le ticket a été émis par erreur ou que vous souhaitez nettoyer entièrement les anciens enregistrements.

---

## Révoquer un seul ticket

1. Trouvez le ticket dans la liste **Tickets**.
2. Cliquez sur **⋮** sur la ligne.
3. Sélectionnez **Révoquer**.
4. Confirmez dans la boîte de dialogue.

Le statut du ticket change immédiatement en **Révoqué** (rouge) dans la liste et sur sa page de vérification publique.

---

## Supprimer un seul ticket

1. Trouvez le ticket dans la liste **Tickets**.
2. Cliquez sur **⋮** sur la ligne.
3. Sélectionnez **Supprimer**.
4. Confirmez dans la boîte de dialogue.

Le ticket est définitivement supprimé. Quiconque ouvrira le lien de vérification du ticket verra une page d'erreur "Ticket non trouvé".

---

## Suppression Groupée

Pour supprimer plusieurs tickets à la fois :

1. Cliquez sur la **case à cocher** de chaque ligne que vous souhaitez sélectionner, ou utilisez la **case à cocher de l'en-tête** pour sélectionner tous les tickets correspondant aux filtres actuels.
2. La barre de filtrage change pour afficher **N sélectionné(s)** et un bouton **Actions**.
3. Cliquez sur **Actions** → **Supprimer**.
4. Confirmez dans la boîte de dialogue.

Tous les tickets sélectionnés sont définitivement supprimés.

> **Note :** La **Révocation** groupée n'est pas disponible — pour révoquer plusieurs tickets, vous devez le faire individuellement. Si vous devez invalider un grand nombre de tickets à la fois, l'utilisation de la Suppression peut être plus pratique.

---

## Nettoyer les Tickets Expirés

Pour supprimer les tickets expirés en masse :

1. Cliquez sur l'onglet **Expirés** dans la barre de filtre de statut au-dessus du tableau.
2. Cliquez sur la case à cocher de l'en-tête pour sélectionner tous les tickets expirés de la page actuelle.
3. Augmentez le sélecteur de lignes par page (10 / 25 / 50 / 100) pour en charger davantage à la fois.
4. Cliquez sur **Actions** → **Delete** et confirmez.

Répétez l'opération sur les pages suivantes jusqu'à ce que tous les enregistrements expirés soient effacés.
