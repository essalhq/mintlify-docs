---
title: "Dépannage des Problèmes de Qualité d'Impression"
---

{/* keywords: qualité d'impression, badge flou, photo manquante impression, badge coupé, impression ne fonctionne pas, badge PDF, conseils impression navigateur, impression basse résolution */}
{/* category: Printing & Exporting Badges */}
{/* audience: Admins, Managers */}

Cet article traite des problèmes courants liés à l'impression des badges et aux exportations PNG, ainsi que des solutions pour les résoudre.

---

## Le Badge Paraît Flou ou en Basse Résolution à l'Impression

**Cause** : La photo de profil de l'employé a été téléchargée dans une résolution trop faible.

**Solution** :

1. Ouvrez la fiche de l'employé → onglet **Profil**.
2. Téléchargez une photo de plus haute résolution — idéalement au moins **600 × 600 px**, recommandé **1000 × 1000 px** ou plus.
3. L'aperçu du badge et l'exportation utiliseront automatiquement la nouvelle photo.

> **La qualité de la photo source est primordiale** : Les exportations de badges utilisent un ratio de pixels de 4x, ce qui signifie qu'une photo source de 150 × 150 px paraîtra visiblement floue une fois le badge imprimé au format carte. Utilisez toujours des photos d'au moins 600 px sur le côté le plus court.

Les éléments du modèle de badge (couleurs, QR code, texte) sont vectoriels et nets à toutes les tailles — seules les photos (fichiers matriciels) peuvent paraître floues.

---

## La Photo de l'Employé est Manquante sur le Badge Imprimé

**Causes possibles et solutions :**

| Cause                                 | Solution                                                                                                                                                                        |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Photo non téléchargée                 | Ouvrez la fiche de l'employé et téléchargez une photo                                                                                                                           |
| Téléchargement de la photo en cours   | Attendez quelques secondes et rechargez le Centre d'Impression                                                                                                                  |
| URL de la photo bloquée par CORS      | Le système convertit automatiquement les photos en base64 pour l'exportation — si la photo a été ajoutée via une URL externe plutôt que téléchargée, téléchargez-la directement |
| Option "Afficher la Photo" désactivée | Activez **Afficher la Photo** dans le Badge Designer → Structure & Éléments                                                                                                     |

---

## Le Logo de l'Entreprise est Manquant sur le Badge Imprimé

**Causes possibles :**

- Logo non téléchargé dans Paramètres → Branding, ou dans le Badge Designer → onglet Branding.
- Option "Afficher le Logo" désactivée dans le Badge Designer.

**Solution** : Naviguez vers **Badge Designer → onglet Branding** et téléchargez ou vérifiez le logo. Assurez-vous que **Afficher le Logo** est activé dans Structure & Éléments.

---

## La Mise en Page du Badge est Coupée ou Tronquée

**Cause** : Les marges d'impression du navigateur ajoutent de l'espace supplémentaire, ou l'échelle est trop grande.

**Solutions** :

1. Dans la boîte de dialogue d'impression du navigateur, réglez les **Marges** sur **Aucune** ou **Minimum**.
2. Dans l'onglet **Configuration** du Centre d'Impression, réduisez l'**Échelle des Badges** à 90% ou 95%.
3. Assurez-vous que le **Format de Papier** dans l'onglet Configuration correspond au papier chargé dans votre imprimante.
4. Désactivez **Ajuster à la page** ou **Mettre à l'échelle** dans la boîte de dialogue du navigateur — utilisez toujours **100%**.

---

## Les Couleurs Paraissent Fausses ou Délavées à l'Impression

**Cause** : Le navigateur imprime sans que les couleurs d'arrière-plan soient activées.

**Solution** : Dans la boîte de dialogue d'impression de votre navigateur, recherchez une option nommée :

- **Graphiques d'arrière-plan** (Chrome)
- **Imprimer les fonds de page** (Firefox)
- **Couleurs et images d'arrière-plan** (Edge)

Activez cette option avant d'imprimer. Les couleurs du badge, les dégradés et l'arrière-plan du QR code nécessitent tous que l'impression de l'arrière-plan soit activée.

---

## La Boîte de Dialogue d'Impression est Vide ou n'Affiche aucun Badge

**Cause** : Le navigateur a bloqué l'appel `window.print()`, ou le rendu du badge n'était pas terminé avant le début de l'impression.

**Solutions** :

1. Cliquez à nouveau sur **Imprimer le Badge** — les navigateurs bloquent parfois la première fenêtre contextuelle.
2. Autorisez les fenêtres contextuelles pour `access.essal.cloud` dans les paramètres de votre navigateur.
3. Attendez que l'aperçu du badge soit complètement chargé dans le Centre d'Impression avant de cliquer sur Imprimer.
4. Si vous utilisez une connexion lente, attendez quelques secondes de plus — le moteur de rendu a besoin que les photos et le logo soient chargés en premier.

---

## L'Exportation ZIP se Bloque ou ne se Termine Pas

**Cause** : Une ou plusieurs photos d'employés n'ont pas pu être chargées, ou l'onglet du navigateur est devenu inactif.

**Solutions** :

1. Gardez l'onglet du navigateur actif et visible pendant l'exportation — certains navigateurs ralentissent les onglets en arrière-plan.
2. Si la progression s'arrête (ex: bloqué à 5/20), rafraîchissez la page et réessayez avec moins d'employés.
3. Vérifiez votre connexion internet — chaque photo doit être téléchargée pendant le rendu.
4. Essayez d'exporter par plus petits lots (ex: 25 à la fois au lieu de tous les employés).

---

## Le PNG Téléchargé n'a pas de Photo ou la Mise en Page est Défectueuse

**Cause** : L'exportation a été lancée avant que toutes les images n'aient fini de charger.

**Solution** : Dans le Centre d'Impression, sélectionnez l'employé et attendez de voir sa photo dans le panneau d'aperçu du badge avant de cliquer sur **Télécharger en PNG**. L'exportation utilise le même processus de rendu — si l'aperçu affiche la photo, le PNG l'affichera aussi.

---

## Conseils pour l'Exportation en PDF

Essal Access ne génère pas de PDF directement — il utilise la fonction d'impression vers PDF du navigateur. Pour enregistrer en PDF :

1. Cliquez sur **Imprimer le Badge** ou **Téléchargement Sécurisé** (groupé).
2. Dans la boîte de dialogue d'impression du navigateur, changez la **Destination** / **Imprimante** en **Enregistrer au format PDF**.
3. Cliquez sur **Enregistrer**.

Pour une qualité PDF optimale :

- Réglez les marges sur **Aucune**.
- Activez les graphiques d'arrière-plan.
- Utilisez une **échelle de 100%**.
- Choisissez le même format de papier que celui défini dans votre onglet Configuration.

---

## Vous avez toujours des problèmes ?

Si aucune des solutions ci-dessus ne résout le problème, contactez le Support Essal en joignant :

- Une capture d'écran du Centre d'Impression montrant le problème.
- Le navigateur et la version que vous utilisez (Chrome / Firefox / Edge / Safari).
- Indiquez si le problème concerne l'impression via le navigateur ou le téléchargement PNG/ZIP.
