---
title: "Créer des Types de Tickets Personnalisés"
---

{/* keywords: type de ticket personnalisé, type de ticket, ajouter type ticket, couleur ticket, gérer types tickets */}
{/* category: Tickets */}
{/* audience: Admins, Managers */}

Essal Access inclut six types de tickets prédéfinis, mais vous pouvez ajouter les vôtres pour répondre aux besoins spécifiques de votre organisation — chacun avec un nom, une couleur et une description facultative personnalisés.

![Liste des tickets montrant la variété des types de tickets disponibles](../screenshots/tickets-list.png)

---

## Types de Tickets par Défaut

Les types suivants sont disponibles d'emblée :

| Type      | Couleur |
| --------- | ------- |
| Accès     | Bleu    |
| Repas     | Vert    |
| Événement | Violet  |
| Parking   | Ambre   |
| Transport | Cyan    |
| Coupon    | Rose    |

---

## Ajouter un Type de Ticket Personnalisé

1. Naviguez vers **Tickets** dans la barre latérale.
2. Cliquez sur **Nouveau Ticket** (ou **+ Émettre Ticket**) pour ouvrir la fenêtre de création de ticket.
3. Dans la section **Type de Ticket**, cliquez sur **Gérer les types**.
4. Le panneau Gestionnaire de Types de Tickets s'ouvre.

### Dans le Gestionnaire de Types :

| Champ           | Requis    | Notes                                                                             |
| --------------- | --------- | --------------------------------------------------------------------------------- |
| **Nom**         | ✓         | Le nom d'affichage du type (ex : "Accès Salle de Sport", "Carte de Bibliothèque") |
| **Couleur**     | ✓         | Choisissez une couleur à l'aide du sélecteur (bleu par défaut)                    |
| **Description** | Optionnel | Note interne sur le moment où ce type doit être utilisé                           |

5. Cliquez sur **Ajouter** (ou sur le bouton **+**) pour enregistrer le nouveau type.
6. Il apparaît immédiatement dans la grille de sélection des types de tickets et est disponible pour tous les futurs tickets.

---

## Fonctionnement des IDs de Type de Ticket

L'identifiant interne (`id`) du type est automatiquement généré à partir du nom — les espaces sont remplacés par des tirets et tous les caractères sont mis en minuscules (ex : "Accès Salle de Sport" → `accès-salle-de-sport`). Cet ID est stocké sur chaque ticket émis avec ce type.

---

## Supprimer un Type de Ticket

1. Ouvrez **Gérer les types** depuis la fenêtre de création de ticket.
2. Trouvez le type à supprimer et cliquez sur l'icône de **suppression** (poubelle) à côté.
3. Confirmez la suppression dans la boîte de dialogue.

> **Note :** La suppression d'un type de ticket n'affecte pas les tickets déjà émis. Les tickets existants conservent leur ID de type, mais le nom et la couleur du type ne seront plus résolus sur la page de vérification — le ticket affichera l'ID brut du type au lieu de son nom. Il est recommandé de révoquer ou de supprimer tous les tickets d'un type avant de supprimer le type lui-même.

---

## Où sont stockés les Types de Tickets

Les types de tickets personnalisés sont stockés dans les paramètres de votre organisation et sont accessibles à tous les administrateurs. Les modifications sont appliquées immédiatement — tout administrateur ouvrant la fenêtre de création de ticket verra la liste des types mise à jour.
