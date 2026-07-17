---
title: "Paramètres de l'Appareil"
---

{/* keywords: paramètres appareil, réglages application, fermeture automatique, volume bip, vibration, thème, langue, code pin, déconnexion */}
{/* category: Check-In Devices */}
{/* audience: Operators, Admins */}

L'onglet **Settings** (icône d'engrenage) à l'intérieur de l'application d'enregistrement permet aux opérateurs et aux administrateurs de configurer l'apparence et le comportement de l'appareil. Les modifications prennent effet immédiatement et sont enregistrées localement sur l'appareil.

---

## Apparence

| Paramètre | Options                  | Par défaut |
| --------- | ------------------------ | ---------- |
| **Thème** | Sombre / Clair / Système | Sombre     |

Le thème Sombre est recommandé pour les environnements peu éclairés (entrepôts, lieux d'événements). Le thème Clair fonctionne mieux dans les bureaux bien éclairés.

---

## Langue

| Paramètre                 | Options                      | Par défaut |
| ------------------------- | ---------------------------- | ---------- |
| **Langue de l'interface** | English / Français / العربية | English    |

Le changement de langue met à jour tous les libellés de l'application, y compris les cartes de résultat de scan. L'arabe bascule l'intégralité de l'interface en mode de lecture de droite à gauche.

---

## Informations sur l'Appareil

Ces champs sont modifiables et stockés localement. Ils sont affichés aux administrateurs dans le panneau **Terminaux d'Enregistrement**.

| Paramètre             | Notes                                                            |
| --------------------- | ---------------------------------------------------------------- |
| **Nom de l'appareil** | Un libellé pour cet appareil (ex : "Tablette Entrée Principale") |
| **Nom de l'agent**    | Le nom de l'opérateur (ex : "Ahmed — Équipe de Nuit")            |
| **Emplacement**       | Une description du lieu où l'appareil est placé                  |

Cliquez sur **Enregistrer** après avoir effectué des modifications. Ces mises à jour sont stockées localement et reflétées dans l'identité de l'appareil au sein des logs d'enregistrement.

---

## Comportement du Scanner

| Paramètre                     | Plage              | Par défaut | Notes                                                                                          |
| ----------------------------- | ------------------ | ---------- | ---------------------------------------------------------------------------------------------- |
| **Délai de fermeture auto**   | 1 – 15 secondes    | 4 secondes | Durée pendant laquelle la carte de résultat reste à l'écran avant de disparaître               |
| **Fenêtre de scan en double** | 1 – 30 secondes    | 5 secondes | Pendant cette période après un scan, le même code de badge est ignoré pour éviter les doublons |
| **Volume du bip**             | 0 – 100%           | 60%        | Volume du son d'accès accordé / refusé                                                         |
| **Vibration**                 | Activé / Désactivé | Activé     | Active ou désactive le retour haptique. L'activation déclenche une vibration de test.          |

---

## Cache de Données

La section cache de données indique la quantité de données stockées localement pour le scan hors-ligne :

| Compteur         | Ce qu'il affiche                                          |
| ---------------- | --------------------------------------------------------- |
| Employés         | Nombre d'enregistrements d'employés mis en cache          |
| Visiteurs        | Nombre d'enregistrements de badges visiteurs mis en cache |
| Entrées de log   | Total des événements de scan stockés localement           |
| Non synchronisés | Événements pas encore envoyés au serveur                  |

**Synchronisation forcée (Force Sync)** — déclenche immédiatement un rafraîchissement complet des données depuis le serveur. Utilisez cette option après avoir effectué des modifications massives d'employés dans le panneau d'administration, ou après une utilisation prolongée hors-ligne.

**Vider le cache (Clear Cache)** — supprime tous les enregistrements d'employés et de visiteurs mis en cache localement. L'appareil téléchargera à nouveau les données lors de la prochaine synchronisation. Utilisez cette option pour libérer de l'espace de stockage ou résoudre des problèmes de données obsolètes.

---

## Sécurité (Verrouillage par PIN)

Si un code PIN de sécurité a été configuré pour cet appareil, la section **Verrouillage par PIN** affiche son statut. Lorsqu'il est activé :

- L'application se verrouille automatiquement lorsqu'elle passe en arrière-plan ou que l'écran s'éteint.
- Un code PIN est requis pour reprendre le scan.
- Le code PIN est stocké sous forme de valeur hachée (jamais en texte clair).

La configuration du PIN est gérée par l'administrateur depuis le panneau d'administration.

---

## Autres Paramètres

| Paramètre           | Notes                                                                                                                                      |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **Installer l'App** | Affiche un bouton pour déclencher l'invite d'installation PWA du navigateur (visible uniquement si l'application n'est pas déjà installée) |
| **Géolocalisation** | Demande ou affiche le statut de la permission de géolocalisation (utilisée pour les logs de scan géomarqués)                               |

---

## Déconnexion

Le bouton **Se Déconnecter** en bas des paramètres :

- Efface la configuration de l'appareil du stockage local.
- Supprime le cache local hors-ligne (IndexedDB).
- Renvoie l'application à l'assistant de configuration.

> **Avertissement :** La déconnexion supprime définitivement les données locales et l'enregistrement de l'appareil. L'appareil devra être ré-enregistré. Avant de vous déconnecter, assurez-vous que tous les événements de scan hors-ligne en attente ont été synchronisés (vérifiez le compteur **Non synchronisés** dans le cache de données).
