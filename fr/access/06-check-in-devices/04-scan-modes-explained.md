---
title: "Explication des Modes de Scan"
---

{/* keywords: mode de scan, scanner QR, capture photo, reconnaissance faciale IA, mode badge, mode caméra */}
{/* category: Check-In Devices */}
{/* audience: Admins, Security, Operators */}

L'application d'enregistrement prend en charge trois modes de scan. Vous pouvez basculer entre eux à l'aide du sélecteur de mode en haut de l'onglet **Scan**. Le dernier mode utilisé est mémorisé.

---

## Mode Badge (Scanner QR)

Le **mode Badge** est le mode principal et le plus couramment utilisé. Il active la caméra de l'appareil en tant que lecteur de codes QR en direct.

**Fonctionnement :**

- La caméra s'ouvre avec un viseur plein écran.
- Une fenêtre de scan transparente se trouve au centre de l'écran avec des crochets d'angle et une ligne de balayage animée.
- Pointez la caméra sur n'importe quel code QR de badge Essal et le scan s'effectue automatiquement — aucune pression sur un bouton n'est nécessaire.
- Les résultats apparaissent immédiatement à l'écran.

**Ce qu'il peut scanner :**

- Les codes QR sur les badges d'employés imprimés.
- Les codes QR sur les badges numériques affichés sur le téléphone d'un employé.
- Les liens de badges visiteurs sur l'écran du téléphone d'un visiteur.
- Les IDs de badges bruts (ex: `B-XXXXX`) saisis via l'onglet Manuel.

**Idéal pour :** Le contrôle d'accès standard aux entrées, tourniquets et points de contrôle où les employés ou les visiteurs présentent un badge.

**Application Android uniquement :** La version Android prend également en charge les **scanners de codes-barres USB et Bluetooth** (mode émulation de clavier HID). L'application intercepte les séquences rapides de saisie de touches et les traite comme des codes scannés, ce qui signifie qu'un scanner physique peut être utilisé à un poste fixe sans pointer de caméra.

---

## Mode Photo (Capture Caméra)

Le **mode Photo** permet à l'opérateur de prendre une photo du visiteur à l'aide de la caméra de l'appareil. Ceci est utilisé pour l'enregistrement des visiteurs et les situations où un badge peut ne pas être présent.

**Fonctionnement :**

1. La caméra s'ouvre pour la capture.
2. L'opérateur prend la photo.
3. Un écran d'aperçu apparaît — saisissez éventuellement un ID de référence (ID de badge ou d'employé) et une note.
4. Appuyez sur **Confirmer** pour enregistrer l'entrée.

**Ce qu'il enregistre :**

- La photo capturée (stockée localement et synchronisée sur le cloud une fois en ligne).
- Si un ID de référence a été fourni, le résultat complet de la vérification (accordé/refusé/etc.) est enregistré à côté de la photo.
- Si aucun ID de référence n'est fourni, l'entrée est enregistrée comme `photo_capture` avec le résultat `accordé`.

**Idéal pour :** Les bureaux de réception des visiteurs, les situations où les visiteurs n'ont pas de badge numérique, ou lorsque la vérification de l'identité visuelle est requise en plus du scan du badge.

---

## Mode IA Visage

Le **mode IA Visage** utilise l'intelligence artificielle pour reconnaître les visages à partir de la caméra de l'appareil et les comparer aux photos de profil des employés enregistrés.

- Seuil de confiance configurable (par défaut : 85 %).
- Approbation automatique optionnelle lorsqu'une correspondance est trouvée au-dessus du seuil.
- Nécessite que les employés aient téléchargé une photo de profil.

> **Note :** La reconnaissance faciale par IA est une fonctionnalité premium. La disponibilité dépend de l'abonnement de votre organisation.

---

## Basculer entre les Modes de Scan

Appuyez sur la barre de sélection de mode en haut de l'onglet **Scan** pour basculer entre les modes. Le mode sélectionné est mis en surbrillance et le scanner correspondant s'ouvre immédiatement. L'application mémorise votre dernier mode utilisé et le restaure au prochain lancement.
