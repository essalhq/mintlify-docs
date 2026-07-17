---
title: "Ajouter un nouvel employé"
---

{/* keywords: ajouter un employé, nouvel employé, créer un employé, formulaire employé, enregistrement d'employé, profil, département, photo */}
{/* category: Employee Management */}
{/* audience: Admins, Managers */}

Cet article explique comment ajouter un seul enregistrement d'employé manuellement. Pour ajouter de nombreux employés à la fois, consultez Importer des employés depuis CSV.

Accédez aux **Employés** dans la barre latérale, puis cliquez sur **Ajouter un employé** en haut à droite.

![Liste des employés avec le bouton Ajouter un employé en haut à droite](../screenshots/employees-list.png)

La modale d'employé s'ouvre sur l'onglet **Profil**, prête à être remplie.

![Onglet Profil de la modale d'employé affichant la zone de téléchargement de photo, le nom, l'e-mail et les champs de département](../screenshots/employee-modal-profile.png)

---

## Champs obligatoires

Seuls deux champs sont obligatoires pour enregistrer un employé :

- **Prénom**
- **Nom**

Tout le reste est facultatif — vous pouvez remplir des détails supplémentaires maintenant ou revenir plus tard pour modifier l'enregistrement.

---

## Onglet Profil — Référence des champs

L'onglet Profil est divisé en deux sections : **Informations personnelles** et **Détails organisationnels**.

### Informations personnelles

| Champ                          | Remarques                                                                                                                                                     |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Prénom**                     | Obligatoire                                                                                                                                                   |
| **Nom**                        | Obligatoire                                                                                                                                                   |
| **Identifiant employé**        | Généré automatiquement (p. ex. `EMP-A3F7K2`). Modifiable uniquement lors de la création d'un nouvel enregistrement — en lecture seule après l'enregistrement. |
| **E-mail**                     | Adresse e-mail professionnelle. Utilisée pour la connexion au portail et les notifications.                                                                   |
| **Téléphone**                  | Numéro de téléphone professionnel ou mobile                                                                                                                   |
| **Date de naissance**          | Facultatif — non affiché sur le badge par défaut                                                                                                              |
| **Groupe sanguin**             | Facultatif — A+, A−, B+, B−, AB+, AB−, O+, O−. Peut apparaître sur le badge si activé dans le designer.                                                       |
| **Adresse**                    | Adresse postale                                                                                                                                               |
| **Ville / État / Code postal** | Champs de localisation                                                                                                                                        |
| **Nationalité**                | Facultatif                                                                                                                                                    |
| **Bio**                        | Biographie en texte libre — affichée sur les profils publics et l'Employee Portal si activée                                                                  |

### Détails organisationnels

| Champ           | Remarques                                                                                                                                                                                               |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Rôle**        | Le titre ou poste de la personne (p. ex. _Agent de sécurité_, _Responsable RH_). Affiché sur le badge si activé.                                                                                        |
| **Département** | Sélectionnez parmi les départements définis dans les Paramètres. Les départements doivent exister avant de pouvoir être sélectionnés ici — voir Gérer les départements. |

### Champs personnalisés

Si votre admin a défini des champs d'attributs personnalisés (Paramètres → Champs personnalisés), ils apparaissent sous les champs standard. Les champs marqués d'un astérisque rouge sont obligatoires.

---

## Ajouter une photo

La photo de profil apparaît sur le badge, le profil public et le portail employé. Trois méthodes sont disponibles :

**Télécharger depuis un fichier** — Cliquez sur le cercle de photo ou le bouton **Télécharger une photo**. Formats pris en charge : tout fichier image. Taille maximale : **2 Mo**. La photo est recadrée en cercle sur le badge.

**Capturer depuis la webcam** — Cliquez sur **Prendre une photo** pour ouvrir la caméra. Vérifiez l'image capturée, puis cliquez sur **Accepter** pour l'utiliser ou **Reprendre** pour réessayer.

**Aucune photo** — Si aucune photo n'est téléchargée, un avatar de remplacement est affiché sur le badge. Vous pouvez ajouter une photo plus tard en modifiant l'enregistrement de l'employé.

> **Amélioration de photo par IA** (intégration Claid) : Si votre locataire a l'API photo Claid configurée, l'arrière-plan est automatiquement supprimé des photos téléchargées.

---

## Enregistrer l'enregistrement

Cliquez sur **Enregistrer** en bas à droite de la modale (ou appuyez sur **Alt+S**). L'employé est ajouté à la liste avec le statut **Actif**, et un badge est généré automatiquement en utilisant votre modèle de badge.

Si l'un des champs Prénom ou Nom est vide, le bouton Enregistrer est désactivé.

---

## Onglets de l'employé après l'enregistrement

Une fois un enregistrement sauvegardé, la modale comporte quatre onglets :

| Onglet               | Contenu                                                                                                              |
| -------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Profil**           | Tous les champs ci-dessus — modifiables à tout moment                                                                |
| **Sécurité**         | Statut du badge, PIN 2FA, planning d'accès, zones d'accès, paramètre scanner authentifié uniquement                  |
| **Badges**           | Historique des badges — émettre un nouveau badge, voir ou révoquer les badges précédents                             |
| **Santé & Sécurité** | Contact d'urgence, allergies, conditions médicales, handicaps, certifications de sécurité, équipements de protection |

---

## Workflow d'approbation

Lorsque le **workflow d'approbation des employés** est activé sur votre locataire, les employés nouvellement ajoutés sont placés dans un statut **En attente** au lieu d'Actif. Un admin ou manager doit les examiner et les approuver avant que leur badge devienne actif et scannable.

---

## Raccourcis clavier

| Raccourci    | Action                                                                   |
| ------------ | ------------------------------------------------------------------------ |
| `Alt + N`    | Ouvrir la modale Ajouter un employé depuis la liste des employés         |
| `Alt + S`    | Enregistrer l'enregistrement d'employé actuel (dans la modale)           |
| `Ctrl + 1–4` | Basculer entre les onglets Profil, Sécurité, Badges, Santé & Sécurité    |
| `Échap`      | Fermer la modale (invite si des modifications non enregistrées existent) |
