---
title: "Calendriers d'Accès"
---
{/* category: Public Profiles & QR Scanning */}


Un calendrier d'accès restreint les moments où le badge d'un employé peut être scanné. Les scans effectués en dehors de la fenêtre temporelle configurée sont bloqués et le visiteur voit les heures autorisées au lieu du profil de l'employé.

---

## Quand utiliser les calendriers d'accès

Utilisez les calendriers d'accès pour les employés dont le badge ne doit être validé que pendant les heures de travail — par exemple, les prestataires ayant des horaires fixes ou le personnel temporaire ayant un accès limité au site.

---

## Configurer un calendrier

1. Ouvrez le dossier de l'employé (**Employés** → cliquez sur l'employé → **Modifier**).
2. Trouvez la section **Calendrier d'Accès** et activez-la.
3. Définissez l'**Heure de début** et l'**Heure de fin** (format 24h).
4. Choisissez les jours où le badge est valide :
   - **Jours autorisés** — sélectionnez les jours individuels de la semaine (du dimanche au samedi)
   - Ou utilisez **Jours de semaine uniquement** pour autoriser automatiquement du lundi au vendredi
5. Enregistrez le dossier de l'employé.

Le calendrier prend effet immédiatement lors du prochain scan.

---

## Que se passe-t-il en dehors du calendrier

Lorsque quelqu'un scanne le badge en dehors des heures ou jours autorisés, il voit un message **En Dehors des Heures de Travail** au lieu du profil. L'écran affiche :

- La fenêtre horaire autorisée (ex : "08:00 – 17:00")
- Les jours autorisés, mis en évidence dans une rangée d'abréviations de jours
- Une note expliquant que l'accès est limité à ces heures

Le scan est enregistré dans le journal d'audit avec un statut `denied` (refusé) et le motif `outside_schedule`.

---

## Désactiver un calendrier

Pour supprimer un calendrier d'un employé :

1. Ouvrez le dossier de l'employé.
2. Trouvez la section **Calendrier d'Accès**.
3. Désactivez (décochez) le calendrier.
4. Enregistrez.

Les scans de badges pour cet employé ne seront plus restreints par l'heure.

---

## Fuseau Horaire

Les calendriers sont évalués côté serveur en utilisant le fuseau horaire configuré pour l'organisation. Assurez-vous que le fuseau horaire de votre organisation est correctement défini dans **Paramètres → Général** pour garantir que les calendriers correspondent aux heures de travail locales.
