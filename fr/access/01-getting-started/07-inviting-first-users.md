---
title: "Inviter vos premiers utilisateurs"
---

{/* keywords: inviter un utilisateur, créer un utilisateur, utilisateur système, compte admin, compte manager, compte sécurité, suspendre, supprimer un utilisateur, gestion des utilisateurs */}
{/* category: Getting Started */}
{/* audience: Admins */}

Cet article explique comment créer des comptes d'utilisateurs système pour que votre équipe puisse se connecter au panneau d'administration d'Essal Access. Seuls les **Admins** peuvent créer, suspendre et supprimer d'autres utilisateurs.

Accédez aux **Utilisateurs système** dans la barre latérale (ou **Paramètres → Utilisateurs**).

![Liste des utilisateurs système affichant les membres de l'équipe avec leurs rôles et les heures de dernière connexion](../screenshots/system-users.png)

---

## Créer un nouveau compte utilisateur

1. Cliquez sur **Ajouter un utilisateur** en haut à droite de la page Utilisateurs système
2. Remplissez le formulaire :

   | Champ           | Remarques                                                                                             |
   | --------------- | ----------------------------------------------------------------------------------------------------- |
   | **Nom complet** | Le nom de la personne — affiché dans le panneau d'administration et dans les notifications par e-mail |
   | **E-mail**      | Son adresse e-mail professionnelle — c'est son nom d'utilisateur de connexion                         |
   | **Rôle**        | Choisir Admin, Manager ou Sécurité (voir ci-dessous)                                                  |

3. Cliquez sur **Créer un utilisateur**

Essal Access crée le compte et envoie un **e-mail avec un lien magique** à l'adresse que vous avez saisie. Le nouvel utilisateur clique sur le lien pour se connecter pour la première fois — aucune configuration de mot de passe n'est requise sauf s'il choisit d'en définir un plus tard.

> **Le rôle Employé n'est pas disponible ici** : Le rôle Employé est attribué automatiquement lorsque vous liez un utilisateur système à un enregistrement d'employé. Vous ne pouvez pas le sélectionner dans le formulaire Ajouter un utilisateur. Pour donner à un employé l'accès au portail, créez d'abord son enregistrement d'employé et liez-y un compte de portail.

---

## Choisir un rôle

| Rôle         | À qui l'attribuer                                                                                                     |
| ------------ | --------------------------------------------------------------------------------------------------------------------- |
| **Admin**    | Responsables informatiques, propriétaires du système — accès complet incluant la gestion des utilisateurs             |
| **Manager**  | Personnel RH, gestionnaires de bureau — peut gérer les employés et les badges, ne peut pas gérer les utilisateurs     |
| **Sécurité** | Agents de sécurité, réceptionnistes — peut voir les employés, les badges visiteurs et les journaux de scan uniquement |

Pour une description détaillée de ce que chaque rôle peut et ne peut pas faire, consultez Comprendre les rôles utilisateurs.

Limitez les comptes Admin au minimum. La plupart du personnel au quotidien devrait être Manager ou Sécurité.

---

## Ce que le nouvel utilisateur reçoit

Lorsque vous créez un compte utilisateur, Essal Access envoie automatiquement un e-mail d'invitation contenant :

- Un message de bienvenue avec le nom de votre entreprise
- Un lien de connexion (lien magique) pour accéder au panneau d'administration
- L'URL du panneau d'administration (`access.essal.cloud`)

Les liens magiques expirent après **10 minutes**. Si le nouvel utilisateur manque le lien, il peut en demander un nouveau depuis la page de connexion en saisissant son e-mail et en cliquant sur **Continuer** — un nouveau lien magique sera envoyé immédiatement.

---

## Lier un utilisateur à un enregistrement d'employé

Si la personne est également un employé avec un badge, vous pouvez lier son compte utilisateur système à son enregistrement d'employé. Cela connecte son identité admin à son badge, son QR code et l'accès au portail employé.

Pour lier après création :

1. Allez dans **Employés**, trouvez l'enregistrement de l'employé
2. Ouvrez la modale de l'employé → onglet **Sécurité**
3. Sous **Utilisateur système lié**, sélectionnez le compte utilisateur correspondant dans le menu déroulant et enregistrez

Une fois lié, le nom et la photo de l'utilisateur dans le panneau d'administration proviennent de l'enregistrement d'employé, et son Employee Portal (`portal.access.essal.cloud`) devient actif.

---

## Suspendre un utilisateur

Suspendre un utilisateur l'empêche de se connecter sans supprimer son compte. Utilisez cette option lorsqu'une personne est en congé, que son rôle change ou que vous devez supprimer temporairement l'accès.

1. Dans la liste Utilisateurs système, trouvez l'utilisateur
2. Cliquez sur l'**icône de suspension** (l'icône utilisateur avec X) dans sa ligne
3. Confirmez l'action

Un compte suspendu affiche un **badge ambré "Suspendu"** dans la liste des utilisateurs. L'utilisateur verra une erreur s'il essaie de se connecter. Les données et l'historique de son compte sont préservés.

Pour **lever la suspension**, cliquez à nouveau sur la même icône (elle devient une icône utilisateur avec coche lorsque le compte est suspendu).

> Vous ne pouvez pas suspendre votre propre compte. L'action de suspension n'est disponible que pour les autres utilisateurs.

---

## Supprimer un utilisateur

La suppression retire définitivement le compte et l'accès de connexion de l'utilisateur. Cette action est irréversible.

1. Dans la liste Utilisateurs système, trouvez l'utilisateur
2. Cliquez sur l'**icône de corbeille** dans sa ligne
3. Confirmez la suppression dans l'invite

Utilisez la suppression pour les anciens employés ou les comptes créés par erreur. Pour une suppression temporaire, préférez la **suspension** — elle conserve l'historique du compte intact et est réversible.

> Seuls les admins peuvent supprimer des utilisateurs. Vous ne pouvez pas supprimer votre propre compte.

---

## Voir la dernière connexion

La liste Utilisateurs système affiche la **dernière heure de connexion** de chaque utilisateur. C'est utile pour identifier :

- Les comptes qui n'ont jamais été utilisés (invitation non acceptée)
- Les comptes inactifs qui peuvent être suspendus ou supprimés
- Les connexions récentes inattendues qui peuvent nécessiter une investigation
