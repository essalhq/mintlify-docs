---
title: "Présentation de l'Application d'Enregistrement"
---

{/* keywords: application d'enregistrement, application de scan, présentation de l'appareil, scanner essal, scan.idpage.link */}
{/* category: Check-In Devices */}
{/* audience: Admins, Managers, Security */}

L'application d'enregistrement Essal est une application de scan dédiée installée sur des tablettes ou des téléphones à vos points d'accès. Elle lit les codes QR des badges d'employés et les liens des badges visiteurs, les vérifie par rapport aux données de votre organisation et affiche instantanément si l'accès doit être accordé ou refusé.

![Liste des terminaux d'enregistrement montrant les appareils enregistrés avec leur statut de connexion et l'heure de leur dernière activité](../screenshots/checkin-devices-list.png)

---

## Ce que fait l'Application d'Enregistrement

- **Scanne les codes QR** imprimés sur les badges d'employés ou affichés sur le téléphone d'un visiteur.
- **Vérifie l'identité et les droits d'accès** en temps réel, y compris les horaires d'accès et les zones.
- **Fonctionne hors ligne** — les données sont mises en cache localement afin que les scans fonctionnent même en cas de coupure de la connexion Internet.
- **Enregistre chaque scan** avec un horodatage, un résultat et le nom de l'opérateur.
- **Prend en charge plusieurs modes de scan** — scan QR par caméra, capture de photo ou reconnaissance faciale par IA.

---

## Comment est-elle installée ?

L'application d'enregistrement est une application web distincte (PWA) hébergée sur **`https://scan.idpage.link`**. Elle ne fait pas partie du panneau d'administration principal d'Essal Access.

Pour l'installer sur un appareil :

1. Ouvrez **`https://scan.idpage.link`** dans le navigateur de l'appareil.
2. Suivez l'invite du navigateur pour **Ajouter à l'écran d'accueil** (ou installer en tant que PWA).
3. Saisissez le code d'enregistrement fourni par votre administrateur.

Un **APK Android** ("Essal Scanner") est également disponible pour les organisations qui préfèrent une expérience d'application native. La version Android ajoute la prise en charge des scanners de codes-barres USB et Bluetooth.

---

## Aperçu des Écrans de l'Application

Une fois enregistrée et déverrouillée, l'application dispose de quatre onglets :

| Onglet       | Objectif                                                                                           |
| ------------ | -------------------------------------------------------------------------------------------------- |
| **Scan**     | Scanner caméra en direct — l'écran d'utilisation principal                                         |
| **Log**      | Historique des enregistrements du jour avec les détails des résultats                              |
| **Manual**   | Saisie manuelle d'un badge ou d'un ID employé via le clavier physique ou numérique                 |
| **Settings** | Configuration du nom de l'appareil, du comportement du scan, de l'apparence et du cache de données |

---

## Gérer les Appareils depuis le Panneau d'Administration

Les administrateurs peuvent visualiser, désactiver et révoquer tous les appareils enregistrés depuis **Admin → Terminaux d'Enregistrement**. Le panneau d'administration affiche le nom de chaque appareil, son emplacement, le nom de l'agent, le statut en ligne et l'horodatage de dernière activité, offrant une visibilité complète sur les appareils actifs dans votre établissement.

---

## Différences : PWA vs Application Android

| Fonctionnalité                     | PWA (scan.idpage.link)                   | Application Android |
| ---------------------------------- | ---------------------------------------- | ------------------- |
| Scanner code-barres USB/Bluetooth  | ✗                                        | ✓                   |
| Notification de scan non bloquante | ✗                                        | ✓                   |
| Support du bouton retour matériel  | ✗                                        | ✓                   |
| Navigation par balayage d'onglets  | ✗                                        | ✓                   |
| Installation                       | Navigateur / Ajouter à l'écran d'accueil | Installation APK    |
