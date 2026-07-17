---
title: "Envoyer un Code d'Enregistrement par E-mail"
---

{/* keywords: envoyer e-mail configuration, enregistrement e-mail, inviter appareil, e-mail invitation enregistrement */}
{/* category: Check-In Devices */}
{/* audience: Admins, Managers */}

Au lieu de lire un code à haute voix ou de le copier manuellement, vous pouvez envoyer un e-mail d'invitation à la configuration directement à la personne qui installera l'appareil. L'e-mail contient le code d'enregistrement et un lien direct vers l'application d'enregistrement.

![Panneau d'administration des terminaux d'enregistrement montrant le bouton Envoyer E-mail de Configuration](../screenshots/checkin-devices-list.png)

---

## Quand utiliser les invitations par e-mail

Les invitations par e-mail sont utiles lorsque :

- La personne configurant l'appareil se trouve dans un autre lieu.
- Vous souhaitez planifier la configuration de l'appareil sans être présent.
- Vous envoyez des instructions à un opérateur non technique qui a besoin d'un lien de configuration clair.

Contrairement aux codes générés par le bouton **Générer Code** (qui expirent après 15 minutes), les codes d'invitation par e-mail **n'expirent pas** — ils restent valides jusqu'à leur utilisation.

---

## Envoyer l'E-mail d'Invitation

1. Naviguez vers **Terminaux d'Enregistrement** dans le panneau d'administration.
2. Cliquez sur **Envoyer E-mail de Configuration**.
3. Remplissez le formulaire d'invitation :
   - **Adresse e-mail** (requis) — le destinataire recevra le lien de configuration ici.
   - **Nom du destinataire** (optionnel) — personnalise la salutation de l'e-mail.
4. Cliquez sur **Envoyer**.

Le système génère un code d'enregistrement unique et envoie un e-mail contenant :

- Le nom et le logo de votre organisation (extraits de vos paramètres whitelabel).
- Un lien direct vers **`https://scan.idpage.link`**.
- Le code d'enregistrement à saisir lors de la configuration.
- Les instructions de configuration étape par étape.

L'e-mail est envoyé dans la langue configurée dans les paramètres de votre organisation (anglais, français ou arabe).

---

## Ce que doit faire le destinataire

Lorsque le destinataire reçoit l'e-mail :

1. Ouvrir le lien vers `https://scan.idpage.link` sur l'appareil.
2. Suivre l'assistant de configuration (comme décrit dans Enregistrer un Nouvel Appareil).
3. Saisir le code figurant dans l'e-mail lorsque cela est demandé.

---

## Détection d'échec d'envoi (Bounce)

Si l'adresse e-mail du destinataire est invalide et que l'e-mail ne peut être délivré, le panneau d'administration affichera une notification d'erreur. Vérifiez l'adresse e-mail et réessayez.

---

## Note sur la Sécurité

Chaque code d'enregistrement ne peut être utilisé qu'**une seule fois**. Après avoir été utilisé pour enregistrer un appareil, le code est invalidé et ne peut plus être réutilisé. Si le code est utilisé par erreur par le mauvais appareil, vous pouvez **révoquer** l'appareil depuis le panneau d'administration et générer un nouveau code.
