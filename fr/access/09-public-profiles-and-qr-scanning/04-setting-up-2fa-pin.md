---
title: "Configurer un Code PIN 2FA pour un Badge"
---
{/* category: Public Profiles & QR Scanning */}


Un code PIN 2FA ajoute une seconde couche de vérification au badge d'un employé. Lorsqu'il est activé, toute personne scannant le badge doit saisir un code PIN à 4 chiffres avant que le profil public ne soit affiché. Ceci est utile pour les rôles à haute sécurité ou les zones sensibles.

---

## Fonctionnement

Lorsqu'un badge nécessitant un code PIN est scanné :

1. Le scanner voit un **écran de saisie de code PIN** au lieu du profil public.
2. Il saisit le code à 4 chiffres.
3. Si le code est correct, le système enregistre un événement de scan vérifié et le profil est affiché.
4. Si le code est erroné, la tentative est journalisée. Après 5 tentatives incorrectes, le code PIN est verrouillé et toute nouvelle tentative est bloquée.

Toutes les tentatives de vérification — réussies ou échouées — sont enregistrées dans le journal d'audit avec les informations sur l'appareil et l'horodatage.

---

## Activer un code PIN pour un employé

1. Ouvrez le dossier de l'employé (**Employés** → cliquez sur l'employé → **Modifier**).
2. Cochez l'option **Exiger un code PIN (2FA)**.
3. Saisissez un code PIN à 4 chiffres dans le champ **Code PIN**.
4. Enregistrez le dossier de l'employé.

À partir du prochain scan, l'écran du code PIN apparaîtra avant que le profil ne soit affiché.

---

## L'Écran de Saisie du Code PIN

Le visiteur saisissant le code PIN voit quatre cases de chiffres individuelles. L'écran prend en charge :

- **Avance automatique** — le focus passe à la case suivante au fur et à mesure que chaque chiffre est tapé.
- **Navigation par touche retour** — la suppression d'un chiffre ramène le focus à la case précédente.
- **Coller** — coller un code à 4 chiffres remplit automatiquement toutes les cases et valide immédiatement.
- **Touche Entrée** — appuyer sur Entrée après le dernier chiffre valide la saisie.

L'écran utilise la couleur de marque principale de l'organisation.

---

## Comportement en cas de verrouillage

Après **5 tentatives incorrectes**, le code PIN est verrouillé. Un code PIN verrouillé affiche une erreur "Trop de tentatives" et n'acceptera plus de saisies. Contactez un administrateur pour réinitialiser ou changer le code PIN.

---

## Désactiver ou Changer un Code PIN

Pour supprimer l'exigence du code PIN :

1. Ouvrez le dossier de l'employé.
2. Décochez l'option **Exiger un code PIN (2FA)**.
3. Enregistrez.

Pour changer le code PIN, mettez à jour le champ **Code PIN** avec la nouvelle valeur à 4 chiffres et enregistrez.
