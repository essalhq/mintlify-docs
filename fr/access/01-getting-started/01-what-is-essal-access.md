---
title: "Qu'est-ce qu'Essal Access ?"
---

{/* keywords: essal access, présentation, introduction, gestion de badges, badges employés, contrôle d'accès */}
{/* category: Getting Started */}
{/* audience: Admins, Managers */}

Essal Access est une plateforme cloud de gestion de badges d'employés et de contrôle d'accès physique. Elle permet aux organisations de concevoir, d'émettre et de gérer des badges d'identification intelligents pour leurs effectifs — et de contrôler qui accède à quoi, grâce à la lecture de QR codes, la reconnaissance faciale ou la vérification manuelle.

![Tableau de bord Essal Access affichant les badges actifs, les alertes de sécurité et l'activité récente](../screenshots/dashboard.png)

---

## Que peut faire Essal Access ?

Essal Access relie quatre éléments essentiels :

| Composant                    | Description                                                                                                    |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **Panneau d'administration** | L'endroit où votre équipe gère les employés, conçoit les badges et surveille les accès                         |
| **Badges employés**          | Des cartes d'identification numériques avec un QR code unique, accessibles en impression physique ou à l'écran |
| **Dispositifs de pointage**  | Tablettes ou bornes exécutant l'application de pointage Essal, placées aux points d'entrée                     |
| **Portail employé**          | Une application web en libre-service où les employés consultent leur propre badge et profil                    |

---

## Concepts clés

### Locataires (Tenants)

Votre organisation est un **locataire** — un environnement isolé avec ses propres employés, son design de badge, ses paramètres et ses données. Toutes les données sont limitées à votre locataire et ne sont jamais partagées avec d'autres.

### Employés

Un **enregistrement d'employé** est l'identité au cœur d'Essal Access. Chaque employé possède un profil (nom, photo, rôle, département, coordonnées), un identifiant employé unique et un identifiant de badge généré automatiquement. Depuis l'enregistrement d'un employé, vous pouvez gérer ses autorisations d'accès, lui attribuer des tickets et configurer son profil public.

![Liste d'employés affichant les enregistrements avec photos, départements et badges de statut](../screenshots/employees-list.png)

### Badges

Un **badge** est la représentation visuelle de l'identité d'un employé. Votre organisation dispose d'un modèle de badge partagé (conçu dans le Badge Designer), qui est automatiquement appliqué à chaque enregistrement d'employé en utilisant ses données personnelles et sa photo. Les badges peuvent être :

- **Imprimés** comme cartes d'identification physiques (format carte CR80 ou personnalisé)
- **Affichés numériquement** dans l'Employee Portal sur n'importe quel appareil
- **Scannés via QR code** aux points de pointage ou par n'importe quel smartphone

Chaque badge contient un QR code unique qui renvoie au **profil de vérification public** de l'employé — une page sécurisée affichant ses informations d'identité, ses autorisations d'accès et son statut actuel en temps réel.

### Dispositifs de pointage

Un **dispositif de pointage** est toute tablette, borne ou ordinateur exécutant l'application de pointage Essal Access (une Progressive Web App). Les dispositifs sont enregistrés dans votre locataire via un code d'appairage à 6 caractères. Une fois enregistrés, ils peuvent :

- Scanner les QR codes des employés et retourner instantanément un résultat **Accordé / Refusé**
- Effectuer des scans de **reconnaissance faciale**
- Accepter la **saisie manuelle** d'un identifiant employé
- Fonctionner **hors ligne** en cas de perte de connectivité, en mettant les scans en file d'attente jusqu'à la reconnexion

### Utilisateurs système

Les **utilisateurs système** sont les comptes administrateurs pouvant se connecter au panneau d'administration. Il existe quatre rôles — **Admin**, **Manager**, **Sécurité** et **Employé** — chacun avec des niveaux d'accès différents. Un utilisateur système peut être lié à un enregistrement d'employé, lui conférant à la fois les droits d'un utilisateur du portail et d'un administrateur.

### Portail employé

L'**Employee Portal** est une interface séparée, destinée aux employés, où le personnel peut :

- Consulter et afficher son propre badge et QR code
- Mettre à jour sa photo de profil et ses coordonnées (si autorisé par son administrateur)
- Télécharger sa carte de visite numérique
- Signaler un badge perdu ou volé

Les employés se connectent avec leurs propres identifiants et ne voient que leurs propres données.

---

## Comment tout s'articule

Un flux de travail typique avec Essal Access ressemble à ceci :

1. L'administrateur conçoit le modèle de badge dans le Badge Designer
2. L'administrateur ajoute des employés — manuellement ou via import CSV
3. Les badges sont automatiquement générés pour chaque employé
4. Les badges physiques sont imprimés **ou** les employés utilisent des badges numériques dans l'Employee Portal
5. Les dispositifs de pointage sont enregistrés aux points d'entrée via un code d'appairage
6. L'employé arrive → scanne son QR code sur le dispositif → résultat **Accordé** ou **Refusé** en temps réel
7. Tous les scans sont enregistrés → L'administrateur consulte l'historique dans le tableau de bord

---

## Ce qu'Essal Access n'est pas

- **Pas un système de suivi du temps** — Essal Access enregistre les scans de badges mais ne calcule pas les heures de présence ni ne s'intègre à la paie
- **Pas un système RH** — les enregistrements d'employés stockent des données de contact et d'accès, pas des contrats, des évaluations de performance ou des congés
- **Pas un contrôleur de serrures physiques** — Essal Access gère la couche d'identité numérique et de vérification ; l'intégration du matériel de contrôle des portes est gérée séparément
