---
title: "Statuts des Badges Visiteurs"
---

{/* keywords: statut badge visiteur, badge actif, badge expiré, badge révoqué, validité badge, états badge */}
{/* category: Guest Badges */}
{/* audience: Admins, Managers, Reception, Security */}

Chaque badge visiteur possède un statut qui détermine si l'accès doit être accordé. Cet article explique la signification de chaque statut et comment il est défini.

![Liste des Badges Visiteurs montrant les badges actifs, expirés et révoqués avec des pastilles de statut colorées](../screenshots/guest-badges-list.png)

---

## Aperçu des Statuts

| Statut      | Couleur | Signification                                                        |
| ----------- | ------- | -------------------------------------------------------------------- |
| **Actif**   | Vert    | Le badge est valide — l'accès peut être accordé au visiteur          |
| **Expiré**  | Ambre   | La fenêtre de validité est passée — l'accès ne doit pas être accordé |
| **Révoqué** | Rouge   | Annulé manuellement par un administrateur — ne pas accorder l'accès  |

---

## Actif

Un badge est **Actif** lorsque :

- Son statut en base de données est `active`, **et**
- L'heure actuelle se situe dans la fenêtre `valide du` / `valide jusqu'au`.

Un badge actif affiche une pastille de statut **verte** dans la liste d'administration et une barre supérieure **bleue** sur la page de vérification publique.

> **Les badges nouvellement créés** sont actifs immédiatement, à moins que vous ne définissiez une date "valide du" ultérieure.

---

## Expiré

Un badge est **Expiré** lorsque son heure "valide jusqu'au" est passée. L'expiration est **automatique** — aucune action manuelle n'est requise.

- L'expiration est calculée côté client à chaque chargement de page.
- L'enregistrement sous-jacent en base de données reste `active` ; seul le statut affiché change.
- La page de vérification publique évalue également le champ "valide jusqu'au" et affiche **Expiré** aux agents de sécurité.

Un badge expiré affiche une pastille de statut **ambre** dans la liste d'administration et une barre supérieure **ambre** sur la page de vérification.

> **Important :** Un badge expiré ne peut pas être réactivé. Si un visiteur doit prolonger sa visite, créez un nouveau badge avec une fenêtre de validité mise à jour.

---

## Révoqué

Un badge est **Révoqué** lorsqu'un administrateur l'annule explicitement avant ou après sa fenêtre de validité. Cela vous permet de bloquer immédiatement l'accès même si la date "valide jusqu'au" du badge n'est pas encore atteinte.

Lorsqu'un badge est révoqué :

- Son statut en base de données est défini sur `revoked`.
- Le nom de l'administrateur qui l'a révoqué et l'horodatage sont enregistrés (`revoked_by` et `revoked_at`).
- La page de vérification affiche **Badge Révoqué** en rouge à tout agent qui le scanne.

Pour révoquer un badge :

1. Naviguez vers **Badges Visiteurs**.
2. Cliquez sur le **menu à trois points (⋮)** sur la ligne du badge.
3. Sélectionnez **Révoquer**.
4. Confirmez l'action dans la boîte de dialogue.

> **Note :** L'option Révoquer n'apparaît que pour les badges qui sont actuellement **Actifs**. Les badges expirés ou déjà révoqués ne peuvent plus être révoqués à nouveau.

---

## Ce que voit le Personnel de Sécurité

Sur la page de vérification publique, le statut est communiqué visuellement et textuellement :

| Statut  | Couleur barre sup. | Texte pastille statut |
| ------- | ------------------ | --------------------- |
| Actif   | Bleu               | "Badge Valide"        |
| Expiré  | Ambre              | "Badge Expiré"        |
| Révoqué | Rouge              | "Badge Révoqué"       |

Si un agent scanne un lien qui n'existe pas (le jeton est invalide ou le badge a été supprimé), il verra un écran d'erreur avec une icône X et un message explicatif.
