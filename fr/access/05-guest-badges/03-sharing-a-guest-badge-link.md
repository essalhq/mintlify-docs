---
title: "Partager le Lien d'un Badge Visiteur"
---

{/* keywords: partager badge visiteur, copier lien badge, URL badge visiteur, envoyer lien badge, code QR visiteur */}
{/* category: Guest Badges */}
{/* audience: Admins, Managers, Reception */}

Chaque badge visiteur possède un lien unique et permanent qui peut être partagé avec le visiteur et scanné par le personnel de sécurité.

![Liste des Badges Visiteurs avec menu d'action montrant les options Copier le lien et Voir le badge](../screenshots/guest-badges-list.png)

---

## Format de l'URL du Badge

Chaque badge visiteur est accessible à l'adresse suivante :

```
https://idpage.link/guest/{token}
```

Où `{token}` est un UUID unique généré au moment de la création. Cette URL est :

- **Publique** — aucune connexion n'est requise pour l'ouvrir.
- **Permanente** — le lien ne change pas et n'expire pas (le statut du badge, oui).
- **Unique** — chaque badge a un jeton (token) différent ; les liens ne peuvent pas être devinés.

---

## Envoi de l'E-mail d'Invitation

Lorsque vous cliquez sur **Envoyer l'Invitation** (ou **Envoyer N Invitations**), Essal Access envoie automatiquement le lien du badge par e-mail à chaque visiteur. L'e-mail comprend :

- Le lien du badge et une image du code QR.
- Les détails de la visite (motif, fenêtre de validité, nom de l'hôte, zones d'accès).
- L'identité visuelle de votre organisation (logo et nom).

Aucune autre action n'est requise de votre part.

---

## Copier le Lien Manuellement

Si vous devez partager à nouveau le lien après l'invitation initiale (ou si l'e-mail n'a pas été reçu), vous pouvez le copier depuis le panneau d'administration :

1. Naviguez vers **Badges Visiteurs**.
2. Trouvez la ligne correspondant au badge dans la liste.
3. Cliquez sur le **menu à trois points (⋮)** à la fin de la ligne.
4. Sélectionnez **Copier le Lien**.

L'URL du badge est copiée dans votre presse-papiers et une notification de confirmation apparaît. Vous pouvez ensuite la coller où vous le souhaitez — SMS, WhatsApp, Slack, e-mail imprimé, etc.

---

## Visualiser la Page du Badge

Pour prévisualiser exactement ce que le visiteur verra en ouvrant le lien :

1. Trouvez la ligne du badge dans la liste des **Badges Visiteurs**.
2. Cliquez sur le **menu à trois points (⋮)**.
3. Sélectionnez **Voir le Badge**.

La page de vérification publique s'ouvre dans un nouvel onglet du navigateur.

---

## Pour les Agents de Sécurité

Les agents n'ont pas besoin de se connecter pour vérifier un badge. Lorsqu'un visiteur arrive et présente son QR code sur l'écran de son téléphone, l'agent peut :

1. Ouvrir n'importe quel scanner de QR code (y compris l'application appareil photo d'un smartphone).
2. Scanner le code QR sur le téléphone du visiteur.
3. La page du badge s'ouvre dans le navigateur, affichant le nom du visiteur, le motif de sa visite, la validité et les zones d'accès.

La barre supérieure de la page utilise un code couleur pour que le statut soit visible au premier coup d'œil :

- **Bleu** → Actif / valide
- **Ambre** → Expiré
- **Rouge** → Révoqué
