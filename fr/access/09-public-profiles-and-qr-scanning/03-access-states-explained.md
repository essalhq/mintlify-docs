---
title: "Explication des États d'Accès"
---
{/* category: Public Profiles & QR Scanning */}


Lorsqu'un badge est scanné, le résultat affiché au visiteur dépend de l'état actuel du badge et du dossier de l'employé. Cet article décrit tous les résultats possibles et ce qui les déclenche.

---

## États des Badges d'Employés

### ✅ Actif — Profil Affiché

Toutes les vérifications sont concluantes. Le visiteur voit le profil public de l'employé avec les informations configurées dans l'Éditeur de Page Publique.

Cet état nécessite :

- Le statut de l'employé est **Actif**.
- Le statut du badge est **Actif**.
- La vérification publique est activée.
- Aucune restriction de calendrier d'accès ne s'applique au moment actuel.
- Aucun code PIN n'est requis (ou le code PIN correct a été saisi).

### 🔒 Badge Signalé comme Perdu

Le badge a été signalé comme perdu ou volé, soit par l'employé via le portail, soit par un administrateur.

Le visiteur voit un message **Badge Signalé comme Perdu** avec une icône d'avertissement ambre. Le scan est enregistré sous le libellé `badge_lost`.

### ⚠️ Badge Suspendu

L'employé ou son badge a été temporairement suspendu par un administrateur.

Le visiteur voit un message **Badge Suspendu**. C'est un état temporaire — le badge peut être réactivé.

### ✗ Badge Désactivé

Le badge a été définitivement désactivé. Cela diffère de la suspension car la désactivation n'est pas censée être annulée.

Le visiteur voit un message **Badge Désactivé** avec une icône de barre oblique.

### ⏱ Badge Expiré

Le badge a atteint sa date d'expiration.

Le visiteur voit un message **Badge Expiré**.

### ✗ Emploi Terminé

Le dossier de l'employé possède le statut **Licencié** (Terminated). Le visiteur voit un message **Emploi Terminé**.

### 🔒 Vérification Publique Désactivée

L'organisation a désactivé le scan public des badges dans les paramètres. Tous les scans pour tous les employés sont bloqués.

Si le **Mode Carte de Visite** est également activé, le visiteur voit la carte de visite de l'employé au lieu de cette erreur.

### 🔒 Profil Désactivé

Un administrateur a désactivé le profil public pour cet employé spécifique. Les profils des autres employés continuent de fonctionner normalement.

### 🔔 Maintenance du Système

Le système est en maintenance. Tous les scans publics sont temporairement bloqués et les visiteurs voient une notice de maintenance.

### 🛡 Accès Restreint (Scanneurs Authentifiés Uniquement)

Le badge de cet employé est configuré pour nécessiter un scanneur authentifié — ce qui signifie que le scanneur doit être connecté à un compte au sein de la même organisation.

Un visiteur non authentifié (comme quelqu'un utilisant l'appareil photo d'un téléphone) voit un message **Accès Restreint** et est invité à se connecter.

### 🕐 En Dehors des Heures de Travail

Cet employé a un calendrier d'accès configuré, et le scan a lieu en dehors de la fenêtre horaire autorisée. Les heures et jours autorisés sont affichés au visiteur afin qu'il sache quand revenir.

### ❓ Badge Invalide

Aucun employé, badge visiteur ou ticket ne correspond à l'identifiant scanné — l'ID du badge n'existe pas dans le système. Le visiteur voit une page **Badge Invalide** sur fond sombre avec une icône X rouge.

---

## États des Badges Visiteurs

| État           | Ce que le visiteur voit         |
| -------------- | ------------------------------- |
| **Actif**      | Coche verte — "Badge Valide"    |
| **Expiré**     | Horloge ambre — "Badge Expiré"  |
| **Révoqué**    | X rouge — "Badge Révoqué"       |
| **Non trouvé** | X rouge — erreur badge invalide |

---

## États des Tickets

| État                  | Ce que le visiteur voit              |
| --------------------- | ------------------------------------ |
| **Actif**             | Coche verte                          |
| **Expire bientôt**    | Horloge ambre — expire d'ici 3 jours |
| **Expiré**            | Horloge ambre                        |
| **Utilisé / Révoqué** | X rouge                              |
