---
title: "Comprendre les rôles utilisateurs"
---

{/* keywords: rôles, permissions, admin, manager, sécurité, employé, contrôle d'accès, utilisateurs système, gestion des utilisateurs */}
{/* category: Getting Started */}
{/* audience: Admins */}

Essal Access dispose de quatre rôles d'utilisateur système — **Admin**, **Manager**, **Sécurité** et **Employé**. Chaque rôle contrôle les pages auxquelles un utilisateur peut accéder et les actions qu'il peut effectuer dans le panneau d'administration. Cet article explique ce que chaque rôle peut faire et comment décider quel rôle attribuer.

![Liste des utilisateurs système affichant les rôles avec des badges colorés](../screenshots/system-users.png)

---

## Les quatre rôles en un coup d'œil

| Capacité                                              | Admin | Manager | Sécurité | Employé |
| ----------------------------------------------------- | :---: | :-----: | :------: | :-----: |
| Tableau de bord                                       |  ✅   |   ✅    |    ✅    |    —    |
| Voir la liste des employés                            |  ✅   |   ✅    |    ✅    |    —    |
| Ajouter / modifier des employés                       |  ✅   |   ✅    |    —     |    —    |
| Supprimer des employés                                |  ✅   |    —    |    —     |    —    |
| Importer des employés (CSV)                           |  ✅   |   ✅    |    —     |    —    |
| Badge Designer                                        |  ✅   |   ✅    |    —     |    —    |
| Imprimer / impression en masse de badges              |  ✅   |   ✅    |    —     |    —    |
| Badges visiteurs                                      |  ✅   |   ✅    |    ✅    |    —    |
| Tickets                                               |  ✅   |   ✅    |    —     |    —    |
| Journaux de scan                                      |  ✅   |   ✅    |    ✅    |    —    |
| Journaux d'audit                                      |  ✅   |   ✅    |    ✅    |    —    |
| Paramètres                                            |  ✅   |   ✅    |    —     |    —    |
| Utilisateurs système                                  |  ✅   |   ✅    |    —     |    —    |
| Éditeur de page publique                              |  ✅   |   ✅    |    —     |    —    |
| Éditeur de carte de visite                            |  ✅   |   ✅    |    —     |    —    |
| Inviter / suspendre / supprimer d'autres utilisateurs |  ✅   |    —    |    —     |    —    |
| Accès au portail employé                              |   —   |    —    |    —     |   ✅    |

> Les utilisateurs avec le rôle **Employé** n'ont pas accès au panneau d'administration. Ils se connectent via l'Employee Portal sur `portal.access.essal.cloud`.

---

## Admin

**Accès complet.** Les admins peuvent tout faire dans le système — il n'y a aucune restriction sur une page ou une action.

Seuls les admins peuvent :

- **Supprimer définitivement des enregistrements d'employés**
- **Inviter, suspendre et supprimer d'autres utilisateurs système** — y compris d'autres admins
- **Voir les chaînes user-agent brutes** dans le panneau de détails du journal d'audit

Attribuez le rôle Admin aux responsables informatiques, aux administrateurs RH ou à toute personne responsable de la gestion du système Essal Access lui-même. Limitez le nombre de comptes Admin.

> Un admin ne peut pas modifier son propre compte depuis le panneau Utilisateurs système — c'est une protection pour éviter le verrouillage accidentel. Pour modifier votre propre mot de passe ou profil, utilisez le menu de profil en haut à droite.

---

## Manager

**Accès étendu, pas d'actions destructives.** Les managers peuvent accéder à presque tout — employés, badges, paramètres, tickets, badges visiteurs, journaux d'audit — mais ils ne peuvent pas supprimer des employés ni gérer d'autres comptes d'utilisateurs système.

Utilisez le rôle Manager pour :

- **Le personnel RH** qui doit ajouter et modifier des employés mais ne doit pas pouvoir supprimer définitivement des enregistrements
- **Les gestionnaires de bureau** qui gèrent l'impression de badges et l'émission de badges visiteurs
- **Les chefs de département** qui ont besoin d'accéder en lecture aux données et rapports des employés

La différence clé avec Admin : un manager voit le panneau d'administration complet mais les actions **supprimer employé**, **inviter utilisateur**, **suspendre utilisateur** et **supprimer utilisateur** ne lui sont pas disponibles.

---

## Sécurité

**Accès en lecture seule, opérationnel.** Les agents de sécurité et le personnel d'accueil ont besoin de vérifier les badges et de consulter l'activité de scan récente — ils n'ont pas besoin de gérer les données des employés ni de configurer le système.

Les utilisateurs Sécurité peuvent accéder à :

- **Tableau de bord** — vue d'ensemble en direct de l'activité de scan récente et des alertes
- **Employés** — voir la liste et rechercher un employé (lecture seule ; pas d'ajout, de modification ou de suppression)
- **Badges visiteurs** — voir et vérifier le statut des badges visiteurs
- **Journaux de scan** — consulter l'historique complet des scans de badges
- **Journaux d'audit** — consulter l'activité du système

Les utilisateurs Sécurité **ne peuvent pas** accéder à : Badge Designer, Centre d'impression, Tickets, Paramètres, Utilisateurs système, Éditeur de page publique ou Éditeur de carte de visite.

Utilisez ce rôle pour le personnel de sécurité de première ligne, les réceptionnistes et les opérateurs de portail.

---

## Employé

**Accès portail uniquement.** Les utilisateurs avec le rôle Employé ne voient pas du tout le panneau d'administration. Lorsqu'ils se connectent, ils sont redirigés vers l'**Employee Portal** — une interface séparée où ils peuvent :

- Consulter et afficher leur propre badge et QR code
- Voir leur profil, rôle, département et détails d'emploi
- Mettre à jour leurs propres informations (nom, photo, coordonnées) si leur admin a activé la modification personnelle
- Signaler un badge perdu ou volé
- Consulter leur carte de visite numérique

Le rôle Employé est généralement attribué automatiquement lorsqu'un compte utilisateur système est lié à un enregistrement d'employé.

---

## Lier un utilisateur système à un enregistrement d'employé

Un compte utilisateur système peut être **lié à un enregistrement d'employé**, ce qui connecte son identité de connexion admin à son badge et son profil. C'est utile lorsqu'un manager ou un membre du personnel RH est également un employé avec un badge.

Pour lier un compte :

1. Ouvrez **Utilisateurs système**, trouvez ou créez l'utilisateur
2. Sélectionnez l'enregistrement d'employé correspondant dans le champ **Employé lié** du formulaire utilisateur

---

## Guide de décision — Quel rôle attribuer ?

| Scénario                                                            | Rôle recommandé                            |
| ------------------------------------------------------------------- | ------------------------------------------ |
| Administrateur informatique / propriétaire du système               | Admin                                      |
| Responsable RH qui ajoute et modifie des employés                   | Manager                                    |
| Gestionnaire de bureau qui imprime des badges et gère les visiteurs | Manager                                    |
| Chef de département qui a besoin d'un accès en lecture aux rapports | Manager                                    |
| Agent de sécurité à une entrée                                      | Sécurité                                   |
| Réceptionniste qui vérifie les badges visiteurs                     | Sécurité                                   |
| Employé ordinaire qui a seulement besoin de son propre badge        | Employé                                    |
| Employé qui est aussi gestionnaire de bureau                        | Manager (lié à l'enregistrement d'employé) |

En cas de doute, commencez par le rôle le plus **restrictif** qui permet à la personne de faire son travail. Les rôles peuvent être modifiés à tout moment par un admin.
