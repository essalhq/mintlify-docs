---
title: "Télécharger et gérer les photos des employés"
---

{/* keywords: photo d'employé, télécharger une photo, photo de profil, webcam, prendre une photo, suppression de fond IA, Claid, téléchargement de photo, photo de badge */}
{/* category: Employee Management */}
{/* audience: Admins, Managers */}

Les photos des employés apparaissent sur leur badge, leur profil public et le portail employé. Cet article couvre les trois méthodes pour ajouter une photo et comment la gérer après le téléchargement.

Accédez aux **Employés**, ouvrez l'enregistrement de l'employé et assurez-vous d'être sur l'onglet **Profil**. La section photo se trouve sur le côté gauche du formulaire.

![Onglet Profil de la modale d'employé affichant la zone de téléchargement de photo sur le côté gauche](../screenshots/employee-modal-profile.png)

---

## Méthode 1 — Télécharger depuis un fichier

1. Cliquez sur le bouton **Télécharger une photo** sous le cercle de photo, ou cliquez directement sur le cercle de photo
2. Un sélecteur de fichiers s'ouvre — sélectionnez n'importe quel fichier image (JPG, PNG, WEBP, GIF, etc.)
3. La photo est téléchargée et le cercle se met à jour immédiatement

**Limite de taille de fichier** : 2 Mo. Si le fichier sélectionné est plus grand, un message d'erreur apparaît et le téléchargement est rejeté.

**Spécifications recommandées** :

- Minimum 400 × 400 px pour une impression de badge nette
- Un recadrage carré convient le mieux — le badge affiche la photo en cercle
- PNG ou JPG pour le web ; évitez les GIF animés

> **Suppression de fond par IA** : Si votre locataire a l'API d'amélioration photo Claid configurée, l'arrière-plan est automatiquement supprimé des photos téléchargées avant leur stockage. Cela donne aux badges une apparence propre et professionnelle. L'amélioration se fait silencieusement — vous n'avez pas besoin d'effectuer d'étapes supplémentaires.

---

## Méthode 2 — Capturer depuis la webcam

1. Cliquez sur **Prendre une photo** sous le cercle de photo
2. Une vue de caméra plein écran s'ouvre avec un guide ovale pour le visage
3. Positionnez le visage de l'employé dans l'ovale
4. Cliquez sur **Capturer** (le grand bouton cercle bleu) — la vidéo se met en pause et affiche un aperçu
5. Cliquez sur **Utiliser la photo** pour l'accepter, ou **Reprendre** pour réessayer
6. La photo est téléchargée et sauvegardée

> **Conseil** : Utilisez la méthode webcam lorsque les employés sont présents au bureau — c'est plus rapide que de demander aux gens d'envoyer des photos et assure un cadrage cohérent.

---

## Méthode 3 — Aucune photo (espace réservé)

Si aucune photo n'est téléchargée, le badge et le profil affichent un avatar de remplacement générique. Les initiales de l'employé ou une icône de silhouette sont affichées à la place.

Vous pouvez ajouter une photo à tout moment en modifiant l'enregistrement de l'employé — le badge se met à jour immédiatement lorsque l'enregistrement est sauvegardé.

---

## Supprimer une photo

Lorsqu'une photo est déjà téléchargée, un lien **Supprimer la photo** apparaît en rouge sous le bouton de téléchargement.

Cliquez sur **Supprimer la photo** pour effacer l'image. Le badge reviendra à l'affichage de l'avatar de remplacement. Cette action prend effet lorsque vous cliquez sur **Enregistrer**.

---

## Affichage de la photo sur le badge

Le modèle de badge contrôle si la photo est affichée et sa taille d'affichage :

- Si la **photo est activée** dans le Badge Designer, elle apparaît dans la position et la taille configurées sur le badge
- La photo est recadrée en cercle sur le badge par défaut (configurable dans le designer)
- Si la **photo est désactivée** dans le modèle du Badge Designer, la photo est toujours stockée dans l'enregistrement mais n'est pas affichée sur le badge imprimé
