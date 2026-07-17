---
title: "Fonctionnement du Scan Public des Badges"
---
{/* category: Public Profiles & QR Scanning */}


Chaque badge d'employé contient un code QR. Lorsque quelqu'un le scanne, il est dirigé vers une page de vérification publique qui affiche le profil de l'employé — aucune connexion n'est requise. Cet article explique l'intégralité du processus, du scan à l'affichage.

---

## Ce qui se passe lorsqu'un badge est scanné

1. Le scanner (l'appareil photo d'un téléphone, un terminal d'enregistrement ou un navigateur) ouvre l'URL encodée dans le code QR.
2. Le système recherche l'ID du badge et récupère le dossier de l'employé.
3. Une série de vérifications est effectuée pour déterminer si l'accès doit être accordé, bloqué ou limité.
4. La page appropriée s'affiche pour le scanner : un profil public complet, une carte de visite, un écran d'accès restreint, un écran de saisie de code PIN ou une page de badge invalide.

Tout ce processus se déroule automatiquement et ne nécessite aucune action de la part de l'employé ou d'un administrateur.

---

## Points d'entrée

| Modèle d'URL         | Ce qu'il vérifie                                  |
| -------------------- | ------------------------------------------------- |
| `/{badgeId}`         | Badge employé (sous-domaine ou domaine principal) |
| `/public/{badgeId}`  | Badge employé (chemin public explicite)           |
| `/guest/{token}`     | Badge visiteur                                    |
| `/ticket/{ticketId}` | Ticket d'événement                                |

---

## Les vérifications de validation

Lorsqu'une URL de badge employé est ouverte, le système effectue les vérifications suivantes dans l'ordre :

1. **Recherche du badge** — l'ID du badge est mis en correspondance avec un dossier employé. Si aucune correspondance n'est trouvée, le visiteur voit la page Badge Invalide.
2. **Vérification du locataire (tenant)** — si l'URL se trouve sur un sous-domaine d'entreprise, le badge doit appartenir à cette entreprise. Une non-correspondance affiche la page Badge Invalide.
3. **Statut bloqué** — si le badge ou l'employé est suspendu, perdu, désactivé, expiré ou licencié, le visiteur voit une page Accès Restreint expliquant la raison.
4. **Paramètre de vérification publique** — si l'organisation a désactivé le scan public des badges, le scan est bloqué (ou redirigé vers la carte de visite, si cette option est activée).
5. **Mode maintenance** — si le système est en maintenance, tous les scans publics sont bloqués.
6. **Scanneurs authentifiés uniquement** — si le badge de cet employé nécessite un scanneur connecté, le visiteur doit être connecté à un compte de la même organisation.
7. **Calendrier d'accès** — si l'employé a des horaires restreints, les scans en dehors de ces heures affichent un message "En dehors des heures de travail".
8. **Code PIN 2FA** — si un code PIN est requis pour le badge de cet employé, le visiteur doit saisir le code correct à 4 chiffres avant que le profil ne s'affiche.

Une fois toutes les vérifications passées, le profil public de l'employé s'affiche.

---

## Scan de Badge Visiteur et de Ticket

Les **badges visiteurs** sont vérifiés à l'adresse `/guest/{token}`. Le système vérifie le jeton (token) et affiche le nom du visiteur, son entreprise, le motif de la visite, le nom de l'hôte, les zones d'accès autorisées et les dates de validité. Le badge peut apparaître comme Valide, Expiré ou Révoqué.

Les **tickets** sont vérifiés à l'adresse `/ticket/{ticketId}`. Le système en déduit l'état actuel du ticket et l'affiche comme Actif, Expire Bientôt, Expiré ou Révoqué.

---

## Journalisation des Scans

Chaque scan — qu'il soit réussi ou non — est enregistré automatiquement. Les consultations réussies de badges d'employés sont journalisées avec le type d'appareil, le navigateur et l'adresse IP du scanneur. Les scans bloqués sont enregistrés avec le motif du blocage. Consultez Journalisation des Scans pour plus de détails.
