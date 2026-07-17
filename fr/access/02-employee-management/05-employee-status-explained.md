---
title: "Statut des employés expliqué"
---

{/* keywords: statut employé, actif, suspendu, badge perdu, en attente, résilié, statut badge, changement de statut */}
{/* category: Employee Management */}
{/* audience: Admins, Managers */}

Chaque fiche employé possède un **statut** qui détermine si le badge est valide et quels accès sont autorisés. Cet article explique la signification de chaque statut et comment le modifier.

![Liste des employés avec différents badges de statut](../screenshots/employees-list.png)

---

## Les cinq statuts

### Actif

Le badge de l'employé est valide. Les scans aux dispositifs de contrôle d'accès sont traités normalement selon les zones d'accès, le planning et les paramètres PIN de l'employé.

- Affiché sous forme d'un badge **vert** dans la liste des employés
- L'employé apparaît dans l'onglet **Actif** (vue par défaut)
- Les nouveaux employés démarrent en statut Actif après enregistrement (sauf si le workflow d'approbation est activé)

---

### Suspendu

Le badge de l'employé est temporairement désactivé. Les scans sur tous les dispositifs affichent un résultat **Refusé — Suspendu**. Le QR code du badge fonctionne toujours pour afficher le profil public, mais l'accès est bloqué.

- Affiché sous forme d'un badge **orange** dans la liste des employés
- L'employé apparaît dans l'onglet **Actif** (toujours visible aux côtés des employés actifs)
- La suspension est réversible — utilisez **Réactiver** depuis le menu d'actions de la ligne pour restaurer le statut Actif

Utilisez la suspension lorsqu'un employé est en congé prolongé, pendant une enquête, ou lorsque l'accès doit être temporairement suspendu sans mettre fin définitivement à l'emploi.

---

### Perdu / Volé

Le badge de l'employé a été signalé comme perdu ou volé. Les scans affichent un résultat **Refusé — Badge Perdu**. Le badge est immédiatement désactivé lorsque ce statut est défini.

- Affiché sous forme d'un badge **rouge** dans la liste des employés
- L'employé apparaît dans l'onglet **Actif**
- Pour rétablir l'accès, utilisez **Réémettre le badge** (génère un nouvel ID de badge) ou **Retrouvé** (réactive sans nouvel ID) depuis le menu d'actions de la ligne

> **Perdu vs Suspendu** : Suspendu signifie que l'accès est suspendu à la discrétion d'un administrateur. Perdu signifie que la carte badge physique est compromise — un nouveau badge doit être émis.

---

### En attente

La fiche employé a été créée mais pas encore approuvée. Le badge n'est pas actif et les scans seront refusés.

- Affiché sous forme d'un badge **bleu** dans la liste des employés
- L'employé apparaît **uniquement** dans l'onglet **Requiert une approbation** — il est masqué de l'onglet Actif principal
- Pour activer, utilisez **Approuver** depuis le menu d'actions de la ligne, ou utilisez **Approbation en masse** pour approuver plusieurs employés simultanément

Le statut En attente n'est utilisé que lorsque le bouton **Requiert une approbation pour émettre le badge** est activé dans l'onglet Sécurité de l'employé, ou lorsqu'une nouvelle fiche est créée avec ce paramètre activé.

> Si vous ne voyez pas d'onglet **Requiert une approbation** dans votre liste d'employés, le workflow d'approbation n'est pas activé sur votre tenant.

---

### Résilié

L'employé a quitté l'organisation. Son badge est définitivement révoqué. Les scans affichent un résultat **Refusé — Résilié**.

- Affiché sous forme d'un badge **gris** dans la liste des employés
- L'employé apparaît **uniquement** dans l'onglet **Archivé** — il est retiré de la vue Active
- La résiliation peut être annulée — utilisez **Réactiver** depuis le menu de la ligne dans l'onglet Archivé si nécessaire
- Les données de l'employé sont conservées après la résiliation à des fins d'audit et de reporting

Utilisez la résiliation (pas la suppression) lorsqu'un employé part afin que son historique de badge, ses journaux de scan et ses données soient préservés.

---

## Résumé des statuts

| Statut | Couleur badge | Onglet | Scans | Réversible |
|---|:---:|---|---|:---:|
| Actif | Vert | Actif | Accordé (si les règles sont respectées) | — |
| Suspendu | Orange | Actif | Refusé | ✅ |
| Perdu | Rouge | Actif | Refusé | ✅ |
| En attente | Bleu | Requiert une approbation | Refusé | ✅ |
| Résilié | Gris | Archivé | Refusé | ✅ |

---

## Comment modifier le statut d'un employé

Les changements de statut s'effectuent depuis les **actions de ligne de la liste d'employés** — pas depuis l'intérieur de la fiche.

1. Trouvez l'employé dans la liste
2. Cliquez sur le menu d'actions **⋯** sur sa ligne
3. Sélectionnez l'action appropriée :

| Action | Résultat |
|---|---|
| **Désactiver** | Actif → Suspendu |
| **Signaler perdu** | Actif → Perdu (immédiatement) |
| **Résilier** | N'importe lequel → Résilié |
| **Approuver** | En attente → Actif |
| **Réactiver** | Suspendu → Actif |
| **Réémettre le badge** | Perdu → Actif (nouvel ID de badge) |
| **Retrouvé** | Perdu → Actif (même ID de badge) |

> Le statut peut également être modifié depuis le menu déroulant **Statut** dans l'onglet **Sécurité** de la fiche employé — mais uniquement entre Actif, Suspendu et Perdu. Les statuts En attente et Résilié ne peuvent être définis que via les actions de la liste.

---

## Statut et le Portail Employé

Lorsque le statut change, l'effet sur le Portail Employé est immédiat :

| Statut | Accès au portail |
|---|---|
| Actif | L'employé peut se connecter et voir son badge |
| Suspendu | L'employé peut se connecter mais le badge apparaît comme suspendu |
| Perdu | L'employé peut se connecter mais le badge apparaît comme perdu |
| En attente | L'employé peut se connecter mais aucun badge actif n'est affiché |
| Résilié | Le compte employé est également généralement suspendu — contactez votre administrateur |
