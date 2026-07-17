---
title: "Enregistrements de santé et sécurité"
---

{/* keywords: santé sécurité, contact urgence, allergies, conditions médicales, EPI, certifications sécurité, dossier médical employé */}
{/* category: Employee Management */}
{/* audience: Admins, Managers */}

L'onglet Santé & Sécurité de chaque fiche employé vous permet de stocker des informations médicales et de sécurité sensibles — contacts d'urgence, allergies, certifications de sécurité, et plus encore.

![Fiche employé — onglet Santé & Sécurité](../screenshots/employee-modal-health.png)

---

## Accéder aux enregistrements de santé et sécurité

1. Ouvrez la fiche d'un employé (cliquez sur son nom dans la liste)
2. Cliquez sur l'onglet **Santé & Sécurité** (ou appuyez sur **Ctrl+4**)

---

## Contact d'urgence

Saisissez les informations de contact de la personne à prévenir en cas d'urgence :

- **Nom** du contact d'urgence
- **Numéro de téléphone**
- **Relation** (ex. : conjoint(e), parent, ami(e))

Les employés peuvent mettre à jour leurs propres informations de contact d'urgence depuis le Portail Employé.

---

## Allergies

Ajoutez les allergies connues sous forme de tags. Saisissez chaque allergie et appuyez sur Entrée ou virgule pour l'ajouter. Exemple : `Pénicilline`, `Noix`, `Latex`.

---

## Conditions médicales

Ajoutez les conditions médicales pertinentes sous forme de tags. Utilisez la même interface que pour les allergies.

---

## Handicaps et notes

Champ de texte libre pour toute note sur les besoins en accessibilité, adaptations ou autres informations médicales importantes qui ne correspondent pas aux autres catégories.

---

## Équipements de protection individuelle (EPI)

Ajoutez les types d'EPI requis pour ce poste sous forme de tags. Exemple : `Casque`, `Gilet haute visibilité`, `Bottes de sécurité`.

> Seuls les Admins et Managers peuvent modifier les exigences EPI — les employés ne peuvent pas auto-modifier cette section.

---

## Certifications de sécurité

Ajoutez les certifications individuelles avec les détails suivants :

- **Nom de la certification** (ex. : Premiers secours, Élévateur, H2S en ligne)
- **Numéro de certification**
- **Date d'émission**
- **Date d'expiration**

### Alertes d'expiration

Le système surveille automatiquement les dates d'expiration :

- **Expire bientôt** (ambre) — Expiration dans les 30 prochains jours
- **Expiré** (rouge) — La date d'expiration est dépassée

Ces alertes sont visibles dans la fiche employé et peuvent apparaître dans les tableaux de bord selon votre configuration.

---

## Qui peut voir les données de santé et sécurité

| Rôle | Accès |
|---|---|
| Admin | Accès complet en lecture et écriture |
| Manager | Accès en lecture et écriture pour les employés de son équipe |
| Sécurité | Dépend de la configuration de l'Éditeur de page publique |
| Employé | Peut auto-modifier : contact d'urgence, allergies, conditions médicales, handicaps/notes — PAS les EPI ni les certifications |

> Les données de santé et sécurité ne sont jamais affichées sur le badge ou la page de profil public, quelle que soit la configuration.
