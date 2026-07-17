---
title: "Dépannage des Appareils"
---

{/* keywords: dépannage appareils, scanner ne fonctionne pas, verrouillage hors-ligne, impossible de scanner, appareil ne se connecte pas, réparer terminal enregistrement */}
{/* category: Check-In Devices */}
{/* audience: Admins, Operators */}

Cet article traite des problèmes les plus courants rencontrés avec les appareils d'enregistrement et explique comment les résoudre.

---

## L'appareil affiche un écran "Verrouillage Hors-Ligne"

**Cause :** L'appareil ne s'est pas connecté à Internet pendant une durée supérieure à la limite hors-ligne configurée (par défaut : 24 heures).

**Solution :**

1. Assurez-vous que l'appareil dispose d'une connexion Internet fonctionnelle (essayez d'ouvrir un site web dans le navigateur).
2. Appuyez sur **Se Reconnecter** sur l'écran de verrouillage.
3. Si la connexion réussit, l'application s'ouvre à nouveau sur l'écran de scan.

Si l'écran de verrouillage affiche une icône **🚫 (Révoqué)** au lieu de **📡**, l'appareil a été désactivé depuis le panneau d'administration — voir la section Révoqué ci-dessous.

---

## L'appareil affiche un écran de verrouillage "Révoqué"

**Cause :** Un administrateur a désactivé cet appareil depuis le panneau d'administration, ou l'appareil tente de se connecter à une organisation différente de celle attendue.

**Solution (si désactivé par erreur) :**

1. Connectez-vous au panneau d'administration.
2. Allez dans **Terminaux d'Enregistrement**.
3. Trouvez l'appareil et cliquez sur **Réactiver**.
4. L'appareil rétablira le scan lors de son prochain signal de présence (appuyez sur **Se Reconnecter** pour forcer l'action immédiatement).

**Solution (si l'appareil doit être définitivement retiré) :**

1. L'opérateur appuie sur **Se Déconnecter** sur l'écran de verrouillage.
2. Ré-enregistrez l'appareil avec un nouveau code.

---

## La caméra ne s'ouvre pas ou affiche un écran noir

**Cause :** La permission d'accès à la caméra a été refusée, ou une autre application utilise la caméra.

**Solution :**

1. Vérifiez que la permission caméra est accordée — allez dans les **paramètres du site du navigateur** de l'appareil et autorisez l'accès à la caméra pour `scan.idpage.link`.
2. Fermez toutes les autres applications susceptibles d'utiliser la caméra.
3. Actualisez l'application (balayez vers le bas pour rafraîchir ou rouvrez-la depuis l'écran d'accueil).
4. Sur iOS, si la permission est refusée au niveau du système, allez dans **Réglages → Safari → Appareil photo** et autorisez l'accès.

---

## Les codes QR ne sont pas détectés

**Cause :** Mauvais éclairage, problème de mise au point de la caméra, ou code QR trop petit ou endommagé.

**Solution :**

- Assurez-vous qu'il y a un éclairage adéquat au point de scan.
- Tenez le badge à 15–30 cm de l'objectif et maintenez-le immobile.
- Nettoyez l'objectif de la caméra.
- Essayez de passer en mode **Manuel** et de saisir l'ID du badge au clavier ou via le pavé numérique à l'écran.
- Si le code QR du badge est imprimé, vérifiez si la qualité d'impression est trop faible — consultez la section Impression et Exportation de Badges pour obtenir des conseils.

---

## Les scans affichent "Non Trouvé" pour des employés valides

**Cause :** Le cache des données des employés ne s'est pas encore synchronisé, ou l'enregistrement de l'employé se trouve dans une autre organisation.

**Solution :**

1. Allez dans **Settings** → **Data Cache** → appuyez sur **Force Sync**.
2. Attendez que la synchronisation se termine et réessayez le scan.
3. Vérifiez dans le panneau d'administration que l'employé existe et que son statut est **Actif**.

---

## Le même scan apparaît plusieurs fois dans le log

**Cause :** La fenêtre de scan en double est réglée sur une durée trop courte, ou un scanner de codes-barres USB a envoyé le code plusieurs fois.

**Solution :**

1. Ouvrez **Settings** → **Scanner** → augmentez la **Fenêtre de scan en double** (ex : passez de 5 à 10 secondes).
2. Si vous utilisez un scanner de codes-barres USB/Bluetooth (app Android), vérifiez la propre configuration du scanner pour la suppression des scans répétés.

---

## L'application est très lente ou ralentit

**Solution :**

1. Allez dans **Settings** → **Data Cache** → appuyez sur **Clear Cache**, puis sur **Force Sync** pour reconstruire proprement la base de données.
2. Si l'appareil est ancien ou dispose d'un stockage limité, envisagez de réduire le pré-chargement des photos des employés en supprimant les photos de profil qui ne sont pas strictement nécessaires.
3. Redémarrer l'application (fermer et rouvrir depuis l'écran d'accueil) libère toute mémoire résiduelle.

---

## Un appareil a disparu du panneau d'administration

**Cause :** L'appareil a été révoqué (supprimé) du panneau d'administration, ou l'entrée en base de données a expiré.

**Solution :** L'appareil doit être ré-enregistré. Gérez un nouveau code depuis **Terminaux d'Enregistrement** et suivez à nouveau l'assistant de configuration sur l'appareil. Les logs de scan précédents pour cet appareil sont conservés.

---

## Résultat de refus "Cache expiré"

**Cause :** L'appareil est hors ligne depuis plus de 24 heures et ses données locales sont obsolètes. Par mesure de sécurité, l'application refuse l'accès plutôt que de se baser sur des enregistrements potentiellement périmés.

**Solution :** Connectez l'appareil à Internet et appuyez sur **Force Sync** dans les paramètres. Une fois le cache rafraîchi (généralement en quelques secondes), les scans fonctionneront correctement.
