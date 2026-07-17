---
title: "Suspendre et réactiver les employés"
---

{/* keywords: suspendre employé, réactiver employé, désactiver badge, suspension temporaire, accès révoqué */}
{/* category: Employee Management */}
{/* audience: Admins, Managers */}

La suspension désactive temporairement le badge d'un employé sans mettre fin à son emploi ni supprimer ses données. Elle est idéale pour les congés prolongés, les congés maladie ou les enquêtes internes.

![Liste des employés avec le menu d'actions ouvert](../screenshots/employees-list.png)

---

## Suspendre un employé

1. Accédez à **Employés** dans la barre latérale
2. Trouvez l'employé que vous souhaitez suspendre
3. Cliquez sur le menu **⋯** sur sa ligne
4. Sélectionnez **Désactiver**

Le statut de l'employé passe immédiatement à **Suspendu** (badge orange). Toute tentative de scan à un dispositif de contrôle d'accès retourne **Refusé — Suspendu**.

> Le profil public de l'employé et la page d'affichage du badge restent accessibles via le QR code — seul l'accès physique est bloqué.

---

## Réactiver un employé suspendu

1. Trouvez l'employé suspendu dans la liste (onglet **Actif** — les employés suspendus y restent visibles)
2. Cliquez sur le menu **⋯** sur sa ligne
3. Sélectionnez **Réactiver**

Le statut revient à **Actif** immédiatement. Le badge recommence à fonctionner normalement selon les règles d'accès configurées.

---

## Suspendre via la fiche employé

Vous pouvez également modifier le statut directement depuis la fiche de l'employé :

1. Ouvrez la fiche d'un employé
2. Allez dans l'onglet **Sécurité**
3. Changez le menu déroulant **Statut** sur **Suspendu**
4. Cliquez sur **Enregistrer**

---

## Suspension en masse

Pour suspendre plusieurs employés à la fois :

1. Cochez les cases à côté des employés souhaités
2. Ouvrez le menu déroulant **Actions en masse**
3. Sélectionnez **Désactivation en masse**

Tous les employés sélectionnés passent immédiatement à l'état Suspendu.

---

## Suspension vs autres statuts

| Situation | Statut recommandé |
|---|---|
| Congé temporaire / enquête | **Suspendu** |
| Badge physique perdu ou volé | **Perdu / Volé** |
| L'employé a définitivement quitté | **Résilié** |

Utilisez Suspendu uniquement pour les situations temporaires. Pour les départs permanents, utilisez Résilier un employé à la place afin de préserver les journaux d'audit.
