---
title: "Enregistrer un Nouvel Appareil"
---

{/* keywords: enregistrer appareil, configuration appareil d'enregistrement, ajouter scanner, code d'enregistrement, enregistrement de l'appareil */}
{/* category: Check-In Devices */}
{/* audience: Admins, Managers */}

L'enregistrement d'un appareil le relie à votre organisation et lui permet d'accéder aux données de vos employés et visiteurs. L'enregistrement prend quelques minutes et ne doit être effectué qu'une seule fois par appareil.

![Liste des terminaux d'enregistrement montrant le bouton Générer Code et les entrées des appareils enregistrés](../screenshots/checkin-devices-list.png)

---

## Avant de Commencer

- L'appareil doit disposer d'un navigateur prenant en charge l'accès à la caméra (Chrome recommandé).
- L'appareil doit pouvoir accéder à `https://scan.idpage.link`.
- Vous aurez besoin d'un compte administrateur dans le panneau d'administration Essal Access pour générer le code d'enregistrement.

---

## Étape 1 — Générer un Code d'Enregistrement

1. Connectez-vous au panneau d'administration Essal Access.
2. Naviguez vers **Terminaux d'Enregistrement** dans la barre latérale.
3. Cliquez sur **Générer Code**.
4. Un code de 6 caractères apparaît (ex: `A3F7B2`) avec un compte à rebours.
5. Le code est valide pendant **15 minutes** — le minuteur devient rouge lorsqu'il reste moins de 60 secondes.
6. Cliquez sur l'icône de copie pour copier le code, ou lisez-le à haute voix à la personne qui configure l'appareil.

> Si le code expire avant d'être utilisé, cliquez sur **Générer à Nouveau** pour en obtenir un nouveau immédiatement.

---

## Étape 2 — Ouvrir l'App d'Enregistrement sur l'Appareil

1. Sur l'appareil, ouvrez un navigateur et allez sur **`https://scan.idpage.link`**.
2. Si vous êtes invité à installer l'application, suivez les instructions **Ajouter à l'écran d'accueil** (optionnel mais recommandé).
3. L'assistant de configuration se lance automatiquement à la première ouverture.

---

## Étape 3 — Terminer l'Assistant de Configuration

L'assistant vous guide à travers les étapes suivantes :

**1. Choisir la langue** — sélectionnez English, Français ou Arabic (العربية). L'interface de l'application et les résultats seront affichés dans cette langue.

**2. Installer l'application (optionnel)** — si le navigateur affiche une invite d'installation, cliquez sur **Installer** pour ajouter l'application à l'écran d'accueil pour un accès plus facile. Appuyez sur **Continuer dans le navigateur** pour ignorer.

**3. Saisir le code d'enregistrement** — tapez le code à 6 caractères généré dans le panneau d'administration. Le code est automatiquement converti en majuscules au fur et à mesure que vous tapez. Appuyez sur **Confirmer** — Essal vérifie le code avec le serveur et relie l'appareil à votre organisation.

**4. Saisir les détails de l'appareil :**

- **Nom de l'agent** (requis) — le nom de l'opérateur utilisant cet appareil (ex: "Sécurité Porte Principale").
- **Nom de l'appareil** (requis) — un libellé pour cet appareil (ex: "Tablette Entrée Principale").
- **Emplacement** (optionnel) — une description de l'endroit où l'appareil est placé.

**5. Confirmer** — l'application enregistre la configuration localement et ouvre l'écran de scan.

---

## Que se Passe-t-il Après l'Enregistrement ?

- L'appareil apparaît immédiatement dans la liste **Terminaux d'Enregistrement** du panneau d'administration.
- Le cache des données des employés et des visiteurs de l'appareil commence à se synchroniser en arrière-plan.
- L'appareil envoie un **signal ("heartbeat") toutes les 2 minutes** afin que le panneau d'administration puisse afficher son statut en ligne.
- Tous les événements de scan sont enregistrés et visibles dans la vue **Logs de Scan**.

---

## Modifier les Détails de l'Appareil Plus Tard

Le nom de l'appareil, le nom de l'agent et l'emplacement peuvent être modifiés ultérieurement depuis l'onglet **Settings** à l'intérieur de l'application d'enregistrement. Ces changements sont enregistrés localement sur l'appareil et ne nécessitent pas de ré-enregistrement.
