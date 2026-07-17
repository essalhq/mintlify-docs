---
title: "Que Sont les Tickets ?"
---

{/* keywords: tickets, ticket employé, laissez-passer, bon de repas, ticket d'événement, types de tickets */}
{/* category: Tickets */}
{/* audience: Admins, Managers */}

Les tickets sont des laissez-passer numériques que vous pouvez émettre pour les membres de votre personnel pour un usage et une période spécifiques — comme un laissez-passer d'accès, un bon de repas, un permis de stationnement ou une entrée à un événement. Chaque ticket génère un lien unique avec un code QR qui peut être scanné pour vérifier sa validité.

![Liste des tickets montrant les tickets émis avec le type, l'employé, le statut et les informations d'expiration](../screenshots/tickets-list.png)

---

## Fonctionnement des Tickets

Lorsque vous émettez un ticket pour un employé, Essal Access :

1. Crée un enregistrement de ticket rattaché au profil de l'employé avec un identifiant unique (ex : `TKT-A1B2C3D4E5`).
2. Génère un lien de vérification public : `https://idpage.link/ticket/{ticketId}`.
3. L'employé (ou un opérateur) peut ouvrir ou partager ce lien pour afficher le statut actuel du ticket.

Aucun compte ou application supplémentaire n'est nécessaire pour le destinataire — le lien ouvre une page publique affichant les détails du ticket.

---

## Types de Tickets

Chaque ticket appartient à un **type de ticket** qui définit son nom et sa couleur. Essal Access est fourni avec six types prédéfinis :

| Type      | Couleur | Utilisation typique                         |
| --------- | ------- | ------------------------------------------- |
| Accès     | Bleu    | Laissez-passer pour un bâtiment ou une zone |
| Repas     | Vert    | Cafétéria ou bon de repas                   |
| Événement | Violet  | Entrée à un événement ou une conférence     |
| Parking   | Ambre   | Permis de stationnement                     |
| Transport | Cyan    | Titre de transport                          |
| Coupon    | Rose    | Bon d'achat ou coupon à usage général       |

Vous pouvez également créer vos propres types de tickets personnalisés avec n'importe quel nom et couleur. Consultez Création de Types de Tickets Personnalisés pour plus de détails.

---

## Différences entre les Tickets et les Badges Visiteurs

|                          | Tickets                                  | Badges Visiteurs                            |
| ------------------------ | ---------------------------------------- | ------------------------------------------- |
| Émis à                   | **Employés** (enregistrements existants) | **Visiteurs** (aucun compte employé requis) |
| Système de types         | Types entièrement personnalisables       | Type unique                                 |
| Émission groupée         | Oui — tout un département à la fois      | Non                                         |
| Option "N'expire jamais" | Oui                                      | Non                                         |
| Stockage                 | Rattaché au profil de l'employé          | Enregistrement visiteur séparé              |

---

## Visualiser tous les Tickets

Naviguez vers **Tickets** dans la barre latérale pour voir tous les tickets émis au sein de votre organisation. Vous pouvez filtrer par type de ticket, département, statut, et rechercher par nom d'employé, titre du ticket ou emplacement.
