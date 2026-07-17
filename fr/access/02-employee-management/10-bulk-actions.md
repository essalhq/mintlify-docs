---
title: "Actions en masse — Sélectionner et gérer plusieurs employés"
---

{/* keywords: actions en masse, sélection multiple, approbation en masse, désactivation en masse, export CSV, suppression en masse, cases à cocher */}
{/* category: Employee Management */}
{/* audience: Admins, Managers */}

Les actions en masse vous permettent d'effectuer des opérations sur plusieurs employés à la fois — approuver des nouveaux arrivants, exporter un groupe filtré, désactiver des équipes entières, et plus encore.

![Liste des employés avec sélection en masse et menu Actions en masse](../screenshots/employees-list-bulk.png)

---

## Sélectionner des employés

- **Sélectionner individuellement** : Cochez la case à gauche de n'importe quelle ligne
- **Sélectionner tous sur la page** : Cochez la case dans l'en-tête du tableau — sélectionne tous les employés de la page actuelle
- **Désélectionner tout** : Appuyez sur **Échap** ou décochez la case de l'en-tête

Lorsqu'un ou plusieurs employés sont sélectionnés, le menu déroulant **Actions en masse** apparaît en haut de la liste.

---

## Actions disponibles

### Exporter en CSV

Exporte tous les employés sélectionnés sous forme d'un fichier CSV nommé `employees-export-AAAA-MM-JJ.csv`.

Colonnes incluses : Nom complet, E-mail, Rôle, Département, Statut, ID Employé, ID Badge.

Utilisez cette option pour générer des rapports, importer dans d'autres systèmes, ou créer des sauvegardes.

---

### Approbation en masse

Visible uniquement dans l'onglet **Requiert une approbation**. Approuve tous les employés sélectionnés en un seul clic, faisant passer leur statut de En attente à **Actif**.

---

### Désactivation en masse

Fait passer tous les employés sélectionnés au statut **Suspendu** (désactive les badges immédiatement).

---

### Réactivation en masse

Fait passer tous les employés suspendus sélectionnés au statut **Actif** (réactive les badges immédiatement).

---

### Résiliation en masse

Fait passer tous les employés sélectionnés au statut **Résilié**. Les badges sont révoqués, les données sont conservées. Les employés sont déplacés vers l'onglet Archivé.

---

### Suppression en masse

*(Admins uniquement)* Supprime **définitivement** tous les employés sélectionnés, y compris leurs données, photos et journaux de badge. Cette action est **irréversible**.

> Préférez la **Résiliation en masse** à la Suppression en masse pour les départs, afin de conserver les journaux d'audit.

---

## Conseils pour les opérations ciblées

Pour appliquer des actions en masse à un groupe spécifique :

1. Utilisez la **barre de filtre** pour affiner la liste par département, statut, rôle ou date
2. Cochez la case de l'en-tête pour sélectionner tous les employés filtrés
3. Choisissez votre action depuis le menu **Actions en masse**

Cela vous permet, par exemple, d'exporter uniquement le département Finance, ou de désactiver tous les employés d'un site spécifique en quelques clics.
