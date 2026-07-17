---
title: "Gérer les Appareils depuis le Panneau d'Administration"
---

{/* keywords: gérer appareils, désactiver appareil, réactiver appareil, révoquer appareil, liste des appareils, appareils panneau administration */}
{/* category: Check-In Devices */}
{/* audience: Admins, Managers */}

La section **Terminaux d'Enregistrement** du panneau d'administration vous offre une visibilité complète sur tous les appareils enregistrés dans votre établissement — ainsi que la possibilité de les désactiver ou de les supprimer définitivement.

![Liste des terminaux d'enregistrement montrant les appareils enregistrés avec des indicateurs de statut et des menus d'action](../screenshots/checkin-devices-list.png)

---

## La Liste des Appareils

Chaque ligne de la liste des appareils affiche :

| Colonne               | Description                                                                                               |
| --------------------- | --------------------------------------------------------------------------------------------------------- |
| **Point de statut**   | **Vert** = en ligne (vu au cours des 5 dernières minutes) ; **Gris** = hors ligne ; **Rouge** = désactivé |
| **Nom de l'appareil** | Le libellé attribué lors de la configuration (ex : "Tablette Entrée Principale")                          |
| **Emplacement**       | Le libellé de l'emplacement défini sur l'appareil                                                         |
| **Nom de l'agent**    | Le nom de l'opérateur attribué à cet appareil                                                             |
| **Dernière activité** | Temps écoulé depuis le dernier signal reçu ("à l'instant", "il y a 5 min", "il y a 2h")                   |
| **Badge Désactivé**   | Une pastille rouge affichée uniquement lorsque l'appareil a été désactivé par un administrateur           |

---

## Actions sur les Appareils

Cliquez sur le **menu à trois points (⋮)** sur n'importe quelle ligne d'appareil pour accéder à :

### Désactiver

Empêche temporairement l'appareil d'effectuer des scans. L'appareil reçoit le signal de désactivation lors de son prochain signal de présence (sous 2 minutes) et est immédiatement verrouillé avec un écran **Révoqué**. L'opérateur ne peut pas contourner cela — il doit se déconnecter.

- L'enregistrement de l'appareil est conservé ; aucune donnée n'est perdue.
- Vous pouvez **réactiver** l'appareil à tout moment.
- **Utilisez cette option si :** un appareil est perdu, volé ou temporairement mis hors service.

### Réactiver

Réactive un appareil précédemment désactivé. L'appareil reprendra les scans normalement lors de son prochain signal de présence. L'opérateur devra peut-être appuyer sur **Se Reconnecter** sur l'écran de verrouillage.

### Révoquer

Supprime définitivement l'appareil de votre organisation. L'appareil est effacé du système — il ne peut pas être réactivé et doit être ré-enregistré de zéro si nécessaire.

- Une boîte de dialogue de confirmation s'affiche avant la suppression.
- Tous les logs de scan de l'appareil restent dans votre historique **Logs de Scan**.
- **Utilisez cette option si :** un appareil est définitivement retiré, remplacé ou si l'application a été réinstallée.

---

## Enregistrer un Nouvel Appareil

Le haut de la page Terminaux d'Enregistrement contient les outils d'enregistrement :

- **Générer Code** — crée un code unique à 6 caractères (valide 15 minutes) que l'opérateur saisit lors de la configuration de l'appareil.
- **Envoyer E-mail de Configuration** — envoie un code d'enregistrement sans expiration et des instructions de configuration par e-mail à un opérateur.

Consultez l'article Enregistrer un Nouvel Appareil pour un guide étape par étape.

---

## Surveiller l'État des Appareils

L'horodatage `dernière activité` vous indique si chaque appareil envoie activement des signaux de présence :

- **"À l'instant"** ou **"il y a X min" (< 5 min)** — l'appareil est en ligne et opérationnel.
- **"il y a X min" (5+ min)** — l'appareil peut avoir perdu sa connexion ; vérifiez l'emplacement.
- **"il y a X h"** ou une date — l'appareil est hors ligne depuis une période prolongée ; une vérification est nécessaire.

Un appareil qui est resté hors ligne pendant sa durée maximale configurée (par défaut 24 heures) affichera un écran de verrouillage à son opérateur et nécessitera une reconnexion avant que les scans puissent reprendre.
