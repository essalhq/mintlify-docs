---
title: "Configurer l'image de marque de votre entreprise"
---

{/* keywords: image de marque, nom de l'entreprise, logo, couleurs, slogan, BrandFetch, marque blanche, couleur principale, image de marque du badge */}
{/* category: Getting Started */}
{/* audience: Admins */}

Cet article explique comment configurer l'identité de votre entreprise dans Essal Access — le nom, le slogan, le logo et les couleurs de marque qui apparaissent sur les badges, les profils publics et dans toute l'interface d'administration.

Accédez à **Paramètres** dans la barre latérale, puis cliquez sur l'onglet **Image de marque**.

![Panneau de paramètres affichant l'onglet Image de marque avec le nom de l'entreprise, le téléchargement du logo et les sélecteurs de couleur](../screenshots/settings-general.png)

---

## Nom de l'entreprise et slogan

En haut de l'onglet Image de marque, vous trouverez deux champs sous **Informations sur l'entreprise** :

**Nom de l'entreprise** — Le nom de votre organisation. Il est utilisé sur :

- Tous les badges des employés (dans la position du nom de l'entreprise, si activé dans le modèle de badge)
- L'en-tête de la barre latérale du panneau d'administration
- Les pages de profil public
- Les notifications par e-mail

**Slogan** — Une courte phrase optionnelle affichée sur les badges sous le nom de l'entreprise (p. ex. _« Sécuriser votre lieu de travail »_, _« Bâtiment 3 — Aile Nord »_). Laissez-le vide si vous n'en avez pas besoin.

> **Conseil** : Les champs Nom de l'entreprise et Slogan sont liés au modèle de badge. Enregistrer un nouveau nom ou slogan met immédiatement à jour ce qui apparaît sur tous les badges des employés — pas besoin de rouvrir le Badge Designer.

---

## Logo

Sous la section **Logo**, cliquez sur la zone de téléchargement (ou faites glisser un fichier dessus) pour télécharger votre logo d'entreprise.

**Formats pris en charge** : PNG, JPG, SVG, WEBP
**Taille maximale** : 5 Mo
**Recommandé** : PNG ou SVG avec fond transparent pour un rendu propre sur toute couleur de badge

Une fois téléchargé, le logo apparaît :

- Dans la barre latérale du panneau d'administration
- Sur les badges des employés (si **Afficher le logo** est activé dans le Badge Designer)
- Sur les pages de profil public et de vérification
- Dans l'Employee Portal

Pour remplacer le logo, cliquez à nouveau sur la zone de téléchargement et sélectionnez un nouveau fichier. Pour le supprimer entièrement, cliquez sur le lien **Supprimer le logo** qui apparaît sous la zone de téléchargement après qu'un logo est défini.

> **Logo non affiché sur les badges ?** Ouvrez le Badge Designer et vérifiez que **Afficher le logo** est activé dans le panneau de configuration du recto ou du verso. Les paramètres d'image de marque téléchargent le fichier logo — le modèle de badge contrôle si et où il apparaît.

---

## Couleurs de marque

Sous **Couleurs de marque**, vous pouvez définir deux couleurs :

**Couleur principale** — La principale couleur d'accent utilisée dans tout le panneau d'administration, l'Employee Portal et l'application de pointage. Elle devient également la couleur principale par défaut du badge pour les nouveaux modèles. Cliquez sur la palette de couleurs pour ouvrir un sélecteur de couleur, ou saisissez directement un code hexadécimal (p. ex. `#2563eb`).

**Couleur secondaire** — Une couleur complémentaire plus claire utilisée pour les arrière-plans et les surlignages dans l'interface. Généralement une teinte plus claire de la couleur principale (p. ex. `#eff6ff` pour un principal bleu).

Les modifications des couleurs de marque s'appliquent immédiatement dans l'interface dès que vous enregistrez. Les deux couleurs s'intègrent également dans le modèle de badge par défaut — vous pouvez toujours les remplacer indépendamment dans le Badge Designer.

---

## BrandFetch — Importer automatiquement votre marque

Si votre entreprise a un site web public, la fonctionnalité **BrandFetch** peut automatiquement importer le nom, le logo et la palette de couleurs de votre entreprise en une seule étape.

1. Saisissez l'URL du site web de votre entreprise dans le champ **URL du site web** (p. ex. `essal.cloud`)
2. Cliquez sur **Import de marque**
3. Essal Access interroge la base de données BrandFetch et remplit automatiquement le nom, le logo et les couleurs de marque de votre entreprise
4. Vérifiez les valeurs importées et cliquez sur **Enregistrer**

BrandFetch fonctionne pour la plupart des entreprises avec une présence web établie. Si votre domaine n'est pas trouvé, vous verrez une erreur — téléchargez votre logo et définissez les couleurs manuellement dans ce cas.

> Les imports BrandFetch sont un point de départ — vous pouvez librement modifier les valeurs importées après la récupération.

---

## Enregistrer les modifications

Cliquez sur **Enregistrer** dans la zone supérieure droite du panneau Paramètres pour valider vos modifications. Les mises à jour du nom de l'entreprise et du slogan s'appliquent aux badges immédiatement. Les modifications du logo et des couleurs sont visibles dans toute l'interface dès que l'enregistrement est terminé.
