---
title: "Mode Hors-Ligne"
---

{/* keywords: mode hors-ligne, scan hors-ligne, cache, pas d'internet, déconnecté, verrouillage hors-ligne */}
{/* category: Check-In Devices */}
{/* audience: Admins, Security, Operators */}

L'application d'enregistrement Essal est conçue pour continuer à fonctionner même lorsque l'appareil perd sa connexion Internet. Les données des employés et des visiteurs sont mises en cache localement afin que les scans puissent être vérifiés sans connexion active.

---

## Fonctionnement du Mode Hors-Ligne

Lorsque l'appareil est en ligne, il synchronise en continu les données avec une base de données locale stockée sur l'appareil :

- **Au démarrage :** une synchronisation complète télécharge tous les employés et les badges visiteurs pour votre organisation.
- **Toutes les 5 minutes :** une synchronisation incrémentielle récupère tous les enregistrements mis à jour depuis la dernière synchronisation.
- **Les photos des employés** sont pré-chargées en arrière-plan afin qu'elles apparaissent sur les cartes de résultat même hors-ligne.
- **Les mises à jour en temps réel** sont reçues via un abonnement à la base de données en direct lorsqu'il est en ligne.

Toutes les données de synchronisation sont stockées dans une base de données sur l'appareil (IndexedDB), liée à votre organisation. Les données d'autres organisations ne sont jamais mélangées.

---

## Fraîcheur du Cache

| Seuil                                                | Comportement                                                                                                                                                     |
| ---------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Données de moins de **10 minutes**                   | Utilisées directement ; aucune tentative de récupération.                                                                                                        |
| Données de **plus de 10 minutes** mais moins de 24 h | L'application tente de rafraîchir depuis le serveur ; si hors-ligne, utilise les données en cache avec un indicateur "depuis le cache" sur la carte de résultat. |
| Données de **plus de 24 heures**                     | Renvoie un résultat **Expiré** avec le motif "Cache expiré" — l'appareil doit se reconnecter pour s'actualiser.                                                  |

---

## Logs d'Enregistrement Hors-Ligne

Les événements de scan sont **toujours enregistrés**, que l'appareil soit en ligne ou hors-ligne :

- Chaque scan est sauvegardé immédiatement dans la base de données locale.
- Lorsque l'appareil revient en ligne, les événements en attente sont automatiquement envoyés au serveur.
- Les captures de photos sont également téléchargées lorsque la connectivité est rétablie.

Aucune donnée de scan n'est perdue à cause de problèmes de connectivité.

---

## Signal ("Heartbeat") et Statut en Ligne

L'appareil envoie un **signal de présence toutes les 2 minutes** au serveur lorsqu'il est en ligne. Cela met à jour l'horodatage `dernière activité` visible dans le panneau d'administration.

L'appareil utilise également la réponse du signal pour vérifier son état d'activation :

- Si le serveur signale que l'appareil a été **désactivé** par un administrateur, l'application affiche immédiatement un écran de verrouillage.
- L'heure du dernier signal est stockée localement afin que l'application puisse calculer depuis combien de temps elle est hors-ligne.

---

## Avertissement et Verrouillage Hors-Ligne

L'application surveille le temps écoulé depuis la dernière connexion réussie au serveur :

**Avertissement (bandeau ambre) :** S'affiche lorsque l'appareil a été hors-ligne pendant une durée supérieure à **2 heures avant le maximum configuré** (ex: avertit à 22h si la limite est de 24h). L'application reste pleinement fonctionnelle.

**Verrouillage hors-ligne (📡) :** S'affiche lorsque l'appareil dépasse la durée maximale hors-ligne (par défaut : **24 heures**). Le scan est désactivé jusqu'à ce que l'appareil se reconnecte. L'écran indique quand l'appareil a été en ligne pour la dernière fois et propose un bouton **Se Reconnecter**.

**Verrouillage révoqué (🚫) :** S'affiche lorsque l'administrateur a désactivé l'appareil depuis le panneau d'administration. Ce verrouillage ne peut pas être ignoré — l'opérateur doit se déconnecter. Pour rétablir l'accès, un administrateur doit réactiver l'appareil depuis le panneau d'administration et le ré-enregistrer si nécessaire.

---

## Ajuster la Limite Hors-Ligne

La durée maximale hors-ligne est configurable par appareil. Par défaut, elle est de **24 heures**. Pour la modifier, éditez le réglage `Heures max. hors-ligne` dans l'onglet **Settings** de l'application d'enregistrement. Des valeurs plus basses sont recommandées pour les environnements de haute sécurité.
