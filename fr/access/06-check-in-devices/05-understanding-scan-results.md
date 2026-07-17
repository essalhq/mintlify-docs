---
title: "Comprendre les Résultats de Scan"
---

{/* keywords: résultat de scan, accès accordé, accès refusé, badge expiré, badge révoqué, non trouvé, carte de résultat */}
{/* category: Check-In Devices */}
{/* audience: Security, Operators, Admins */}

Après chaque scan, l'application d'enregistrement affiche une carte de résultat qui indique à l'opérateur s'il doit autoriser ou refuser l'entrée. Chaque résultat possède une couleur et un libellé distincts pour que la décision puisse être prise en un coup d'œil.

---

## Types de Résultats

### Accès Accordé — Vert

Le badge de la personne est valide et elle est autorisée à passer.

Ce résultat apparaît lorsque :

- Le statut de l'employé est **actif** et l'heure actuelle se situe dans son horaire d'accès configuré.
- Le badge visiteur est **actif** et se trouve dans sa fenêtre "valide du" / "valide jusqu'au".

**Retour :** Un bip unique et une courte vibration (80 ms).

---

### Accès Refusé — Rouge

La personne ne doit pas être autorisée à passer.

Ce résultat apparaît lorsque :

- Le statut de l'employé est `suspendu`, `licencié` ou `badge perdu`.
- Le compte de l'employé est en état `en attente` (pas encore actif).
- L'heure actuelle est en dehors des heures d'accès autorisées de l'employé.
- L'heure "valide du" d'un badge visiteur n'est pas encore atteinte.

La carte de résultat affiche le **motif du refus** afin que l'opérateur comprenne pourquoi l'accès a été refusé (ex: "En dehors des heures d'accès", "Compte suspendu").

**Retour :** Un son de refus et une triple vibration.

---

### Badge Expiré — Ambre

Le badge était valide mais n'est plus à jour.

Ce résultat apparaît lorsque :

- L'heure "valide jusqu'au" d'un badge visiteur est passée.
- Les données des employés mises en cache localement sur l'appareil datent de plus de **24 heures** et l'appareil ne peut pas joindre le serveur pour les actualiser — dans ce cas, le motif du refus affiche "Cache expiré" et l'opérateur doit vérifier la connexion Internet.

**Retour :** Un son de refus et une triple vibration.

---

### Badge Révoqué — Orange

Le badge a été annulé manuellement par un administrateur.

Ce résultat apparaît lorsqu'un badge visiteur a été explicitement révoqué depuis le panneau d'administration. La personne ne doit pas être autorisée à entrer, quelles que soient ses affirmations.

**Retour :** Un son de refus et une triple vibration.

---

### Non Trouvé — Gris

Le code scanné ne correspond à aucun employé ou visiteur dans le système.

Ce résultat apparaît lorsque :

- Le code QR n'est pas un badge Essal (mauvaise application, code corrompu ou badge d'une autre organisation).
- L'ID du badge a été supprimé du système.
- Le scan a été tenté depuis un appareil enregistré auprès d'une autre organisation.

**Retour :** Un son de refus et une triple vibration.

---

## La Carte de Résultat

Après chaque scan, une carte de résultat glisse depuis le bas de l'écran affichant :

- La **photo** de la personne (provenant du cache ou de son profil ; icône de personnage par défaut si indisponible).
- Le **nom complet**, le rôle et le département.
- Le **libellé du résultat** (ACCÈS ACCORDÉ / ACCÈS REFUSÉ / etc.).
- Le **motif du refus** (si refusé).
- Les **zones d'accès** où elle est autorisée à entrer (sous forme de badges/chips).
- Pour les visiteurs : **nom de l'hôte**, **motif** et date/heure de **validité**.
- Un indicateur **"depuis le cache"** si les données proviennent du cache local hors-ligne.

La carte **se ferme automatiquement** après un délai configurable (par défaut : 4 secondes). Appuyez n'importe où sur la carte pour la fermer manuellement. Sur l'application Android, une notification (toast) non bloquante de 2 secondes est affichée à la place, maintenant la caméra active pour un scan continu à haut débit.

---

## Voir le Profil (Employés)

Les cartes de résultat des employés actifs incluent un bouton **Voir le Profil** qui ouvre une fenêtre modale de profil complet avec des détails supplémentaires. Lorsque la fenêtre de profil est ouverte, le minuteur de fermeture automatique est mis en pause afin que l'opérateur ait le temps de consulter les informations.
