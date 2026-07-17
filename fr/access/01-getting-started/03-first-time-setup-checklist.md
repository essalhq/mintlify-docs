---
title: "Liste de contrôle de la configuration initiale"
---

{/* keywords: configuration, liste de contrôle, intégration, premiers pas, première fois, configuration initiale */}
{/* category: Getting Started */}
{/* audience: Admins */}

Cette liste de contrôle vous guide à travers chaque étape nécessaire pour passer d'un nouveau locataire Essal Access à un système entièrement opérationnel — avec des employés, des badges et un dispositif de pointage fonctionnel. Chaque étape renvoie au guide complet pour ce sujet.

---

## Avant de commencer

Vous aurez besoin de :

- Vos identifiants d'administration Essal Access (vous devriez les avoir reçus par e-mail)
- Votre fichier de logo d'entreprise (PNG ou SVG recommandé, fond transparent)
- Une liste d'employés à ajouter — saisie manuelle ou export CSV depuis votre système RH
- Au moins un appareil à utiliser comme point de pointage (tablette Android, iPad ou navigateur de bureau)

Temps estimé total : **30 à 60 minutes** pour une petite équipe (moins de 50 employés).

---

## La liste de contrôle

| Étape | Tâche                                               | Où                         |
| ----- | --------------------------------------------------- | -------------------------- |
| 1     | Définir le nom de l'entreprise et l'image de marque | Paramètres → Général       |
| 2     | Créer vos départements                              | Paramètres → Départements  |
| 3     | Créer vos zones d'accès                             | Paramètres → Zones d'accès |
| 4     | Concevoir votre modèle de badge                     | Badge Designer             |
| 5     | Ajouter vos employés                                | Employés                   |
| 6     | Enregistrer un dispositif de pointage               | Dispositifs de pointage    |
| 7     | Effectuer un scan de test                           | Application de pointage    |

Travaillez les étapes dans l'ordre — les étapes ultérieures s'appuient sur les précédentes (par exemple, les départements doivent exister avant de pouvoir y affecter des employés).

---

## Étape 1 — Définir le nom de l'entreprise et l'image de marque

Accédez à **Paramètres** (barre latérale → Paramètres) et ouvrez l'onglet **Général**.

![Panneau de paramètres affichant le nom de l'entreprise, le téléchargement du logo et les options d'image de marque](../screenshots/settings-general.png)

Définissez les éléments suivants :

- **Nom de l'entreprise** — apparaît sur les badges, les profils publics et le portail employé
- **Logo de l'entreprise** — téléchargez votre fichier logo, ou utilisez **BrandFetch** pour l'importer automatiquement en saisissant l'URL de votre site web
- **Couleur principale de la marque** — utilisée comme couleur d'accent par défaut dans les modèles de badges et l'application de pointage

Sauvegardez vos modifications avant de passer à la suite.

> **Raccourci BrandFetch** : Si votre entreprise a un site web public, cliquez sur **Importer depuis BrandFetch**, saisissez votre domaine (p. ex. `essal.cloud`), et Essal Access importera automatiquement votre nom, logo et palette de couleurs.

**Guide complet** : Configurer l'image de marque de votre entreprise

---

## Étape 2 — Créer vos départements

Les départements regroupent les employés pour le filtrage, les rapports et l'affichage sur les badges. Vous avez besoin d'au moins un département avant d'ajouter des employés.

Accédez à **Paramètres → Départements** et créez votre structure de départements.

Pour chaque département, définissez :

- **Nom** (p. ex. _Ingénierie_, _Opérations_, _Accueil_)
- **Code couleur** — pour distinguer visuellement les départements dans la liste des employés et sur les badges
- **Département parent** (facultatif) — pour les structures imbriquées comme _Ingénierie > Backend_

Vous pouvez toujours ajouter des départements plus tard. Un bon point de départ sont les divisions de premier niveau de votre organigramme.

**Guide complet** : Gérer les départements

---

## Étape 3 — Créer vos zones d'accès

Les zones d'accès définissent les zones physiques de vos locaux (ou groupes logiques) que les employés sont autorisés à entrer. Lorsqu'un badge est scanné, le résultat dépend de si l'employé est affecté à la zone du dispositif.

Accédez à **Paramètres → Zones d'accès** et créez au moins une zone pour chaque porte ou zone qui aura un dispositif de pointage.

Pour chaque zone, définissez :

- **Nom de la zone** (p. ex. _Entrée principale_, _Salle des serveurs_, _Entrepôt_)
- **Description** (facultatif) — pour référence interne

Si vos locaux n'ont qu'un seul point d'entrée, une seule zone nommée _Entrée principale_ suffit pour commencer.

---

## Étape 4 — Concevoir votre modèle de badge

Essal Access utilise un modèle de badge partagé unique — un design appliqué automatiquement à chaque enregistrement d'employé en utilisant ses données individuelles.

Accédez au **Badge Designer** (barre latérale → Badge Designer).

![Canevas du Badge Designer avec les contrôles de modèle et l'aperçu en direct](../screenshots/badge-designer.png)

Pour une première configuration, travaillez dans cet ordre :

1. **Choisir une mise en page** — sélectionnez parmi les 7 mises en page intégrées (Modern, Corporate, Tech, Conference, Minimal, Gradient, Executive)
2. **Définir l'orientation** — Portrait (carte CR80 verticale) ou Paysage
3. **Configurer les couleurs et polices** — couleur principale, couleur d'accent, famille de polices
4. **Recto du badge** — choisissez ce qui s'affiche : photo de l'employé, QR code, nom, rôle, département, identifiant employé, identifiant badge, logo de l'entreprise, etc.
5. **Verso du badge** (facultatif) — activez le verso pour les coordonnées, le texte légal ou une image de marque supplémentaire

Utilisez le sélecteur **Aperçu** pour voir le badge rendu avec de vraies données d'employés avant de sauvegarder.

**Guide complet** : Présentation du Badge Designer

---

## Étape 5 — Ajouter vos employés

Avec les départements et votre modèle de badge prêts, vous pouvez maintenant ajouter votre personnel.

Accédez aux **Employés** (barre latérale → Employés).

![Liste des employés avec le bouton Ajouter visible en haut à droite](../screenshots/employees-list.png)

Vous avez deux options :

### Ajouter les employés un par un

Cliquez sur **Ajouter un employé**, remplissez les champs du profil (nom, rôle, département, e-mail, coordonnées) et sauvegardez. Répétez pour chaque personne.

Idéal pour les petites équipes ou les ajouts individuels.

**Guide complet** : Ajouter un nouvel employé

### Importer depuis CSV

Cliquez sur **Importer** → **Importer depuis CSV** pour ouvrir l'assistant d'importation. Téléchargez le modèle, remplissez vos données d'employés, téléchargez le fichier et associez les colonnes aux champs. Essal Access valide vos données avant de valider l'importation.

Idéal pour les équipes de 10 personnes ou plus.

**Guide complet** : Importer des employés depuis CSV

---

## Étape 6 — Enregistrer un dispositif de pointage

Un dispositif de pointage est toute tablette, borne ou navigateur exécutant l'application de pointage Essal Access. Vous l'associez à votre locataire à l'aide d'un code d'enregistrement à usage unique.

### Côté administration

1. Accédez aux **Dispositifs de pointage** (barre latérale → Dispositifs de pointage)

   ![Liste des dispositifs de pointage avec le bouton Générer un code](../screenshots/checkin-devices-list.png)

2. Cliquez sur **Ajouter un dispositif** (ou **Générer un code**)
3. Donnez un nom au dispositif (p. ex. _Tablette Entrée Principale_) et affectez-le à la zone d'accès créée à l'étape 3
4. Un **code d'enregistrement à 6 caractères** s'affiche — valable 15 minutes

### Sur l'appareil

1. Ouvrez [https://checkin.access.essal.cloud](https://checkin.access.essal.cloud) dans le navigateur de l'appareil
2. Saisissez le code à 6 caractères lorsque demandé
3. L'appareil est enregistré et prêt à l'emploi — il apparaîtra comme **Actif** dans votre liste de dispositifs de pointage

---

## Étape 7 — Effectuer un scan de test

Avec au moins un employé ajouté et un dispositif enregistré, effectuez un test rapide de bout en bout avant de démarrer.

1. Ouvrez l'**Employee Portal** sur [https://portal.access.essal.cloud](https://portal.access.essal.cloud) et connectez-vous en tant qu'un de vos employés
2. Le portail affiche le badge de l'employé avec un QR code — appuyez dessus pour l'afficher en plein écran
3. Sur le dispositif de pointage, pointez la caméra vers le QR code
4. L'appareil devrait afficher un **écran vert Accordé** avec le nom, la photo et le département de l'employé

Si vous voyez un résultat **Refusé**, vérifiez que :

- Le statut de l'employé est **Actif** (non suspendu, en attente ou résilié)
- L'employé est affecté à la zone d'accès configurée sur le dispositif
- Le dispositif est toujours connecté à internet
