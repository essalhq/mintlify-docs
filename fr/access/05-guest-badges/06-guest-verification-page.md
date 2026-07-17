---
title: "La Page de Vérification Visiteur"
---

{/* keywords: page de vérification visiteur, page de scan de badge, vue agent de sécurité, page badge visiteur, résultat scan QR, page publique badge */}
{/* category: Guest Badges */}
{/* audience: Admins, Managers, Security, Reception */}

La page de vérification visiteur est la page publique que les visiteurs et les agents de sécurité voient lorsqu'ils ouvrent le lien d'un badge. Aucune connexion n'est requise.

---

## Ce que la Page Affiche

La page de vérification est conçue pour donner à un agent de sécurité toutes les informations dont il a besoin en un seul coup d'œil.

### Éléments Visuels (de haut en bas)

1. **Logo de l'organisation** — extrait de vos paramètres whitelabel.
2. **Barre de statut** — une barre de couleur sur toute la largeur en haut indiquant le statut du badge au premier coup d'œil.
3. **Pastille de statut** — libellé texte ("Badge Valide", "Badge Expiré" ou "Badge Révoqué").
4. **Nom du visiteur** — affiché comme titre principal.
5. **Entreprise du visiteur** — affiché sous le nom (si renseigné), avec une icône de bâtiment.

### Lignes de Détails

| Icône       | Champ                | Affiché quand                                                                    |
| ----------- | -------------------- | -------------------------------------------------------------------------------- |
| Étiquette   | **Motif**            | Toujours                                                                         |
| Utilisateur | **Hôte**             | Toujours (affiche le nom de l'hôte)                                              |
| Calendrier  | **Valide jusqu'au**  | Toujours                                                                         |
| Épingle     | **Zones Autorisées** | Uniquement si des zones d'accès ont été assignées                                |
| Épingle     | **Adresse / Lieu**   | Uniquement si une adresse a été ajoutée ; les liens sont cliquables (ouvre Maps) |

> **Note :** Les adresses e-mail des visiteurs ne sont jamais affichées sur la page de vérification publique. Seules les informations dont un agent a besoin sont visibles.

---

## Couleurs de Statut

La couleur de la barre supérieure et le texte de la pastille de statut changent en fonction de l'état du badge :

| Statut                              | Couleur barre | Texte pastille  |
| ----------------------------------- | ------------- | --------------- |
| Actif (dans la fenêtre de validité) | Bleu          | "Badge Valide"  |
| Expiré (après "valide jusqu'au")    | Ambre         | "Badge Expiré"  |
| Révoqué (annulé par admin)          | Rouge         | "Badge Révoqué" |

Le personnel de sécurité ne doit **accorder l'accès que lorsque** la barre est **bleue** (Badge Valide).

---

## Support de Langue

La page détecte automatiquement la langue du navigateur du visiteur et affiche le contenu dans la langue correspondante. Langues supportées :

- Anglais
- Arabe (mise en page de droite à gauche)
- Français
- Espagnol
- Allemand

Un **sélecteur de langue** est disponible au bas de la page si le visiteur ou l'agent souhaite changer manuellement.

---

## Badges Invalides ou Supprimés

Si l'URL du badge contient un jeton qui n'existe pas (ex: le badge a été supprimé ou le lien a été modifié), la page affiche un état d'erreur :

- Une icône X entourée d'un cercle avec un message d'erreur.
- Aucune information sur le badge n'est affichée.

Les agents doivent traiter ce résultat comme un badge **Révoqué** — l'accès ne doit pas être accordé.

---

## Identité Visuelle (Branding)

La page de vérification utilise l'identité visuelle de votre organisation définie dans les **Paramètres Whitelabel** :

- Logo de l'entreprise.
- Nom de l'entreprise (également utilisé dans le titre SEO de la page : _"\{Statut\} — \{Nom Visiteur\} — \{Nom Entreprise\}"_).

Cela garantit que la page paraît professionnelle et digne de confiance pour les visiteurs et le personnel de sécurité.

---

## Ce que voit le Visiteur vs ce que voit l'Agent

Les visiteurs et les agents de sécurité ouvrent la même URL. La page est conçue pour les deux publics :

- **Les visiteurs** peuvent voir les détails de leur visite pour confirmer que le badge est correct.
- **Les agents** peuvent confirmer que le badge est valide, vérifier les zones d'accès et s'assurer que le nom du visiteur correspond à sa pièce d'identité.

Ni les visiteurs ni les agents ne peuvent modifier le badge à partir de cette page.
