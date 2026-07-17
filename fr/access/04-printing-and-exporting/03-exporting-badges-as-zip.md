---
title: "Exportation de Badges en PNG/ZIP"
---

{/* keywords: exporter badge, télécharger badge PNG, badge ZIP, exportation groupée, télécharger tous les badges, exportation d'image de badge, téléchargement zip */}
{/* category: Printing & Exporting Badges */}
{/* audience: Admins, Managers */}

Essal Access peut exporter les images de badges sous forme de fichiers PNG haute résolution — soit individuellement, soit sous forme d'archive ZIP pour plusieurs employés. Cela est utile pour envoyer des badges à une imprimerie, les importer dans un autre système ou les archiver.

![Onglet d'impression groupée montrant le bouton Télécharger le ZIP avec la sélection d'employés](../screenshots/print-bulk.png)

---

## Exportation d'un Seul Badge en PNG

1. Allez dans l'onglet **Centre d'Impression → Individuel**.
2. Sélectionnez un employé dans le panneau de gauche.
3. Cliquez sur **Télécharger en PNG**.
4. Le badge est généré en haute résolution — un indicateur de chargement s'affiche pendant le traitement (2 à 5 secondes).
5. Le fichier se télécharge automatiquement dans le dossier de téléchargement par défaut de votre navigateur.

**Détails du fichier :**

- Format : PNG (sans perte).
- Résolution : env. 1720 × 2720 px avec une densité de pixels de 4x (adapté pour une impression de haute qualité).
- Nom du fichier : `{Prénom}_{Nom}_{IDBadge}.png`

---

## Exportation de Plusieurs Badges dans un ZIP

1. Allez dans l'onglet **Centre d'Impression → Groupé**.
2. Sélectionnez les employés que vous souhaitez exporter (utilisez la recherche et le filtre par département pour affiner la liste).
3. Cliquez sur **Télécharger ZIP (N)** où N est le nombre d'employés sélectionnés.
4. Une boîte de dialogue de **Vérification de Sécurité** apparaît — cliquez sur **Autoriser**.
5. Un indicateur de progression apparaît sur le bouton : `{fait}/{total}` au fur et à mesure que chaque badge est généré.
6. Une fois terminé, un seul fichier ZIP est téléchargé automatiquement.

**Détails du fichier ZIP :**

- Nom du fichier : `badges_export_{AAAA-MM-JJ}.zip`
- Contenu : un PNG par employé sélectionné.
- Noms des fichiers individuels à l'intérieur : `{Prénom}_{Nom}_{IDBadge}.png`
- Compression : DEFLATE (compression ZIP standard).

> **Note sur les performances** : Les badges sont générés un par un pour éviter les problèmes de mémoire. L'exportation de 50 employés prend généralement 60 à 90 secondes. Ne fermez pas l'onglet du navigateur pendant que l'exportation est en cours.

---

## Ce qui est Inclus dans l'Exportation

Chaque PNG de badge exporté inclut tout ce qui est visible sur le recto du badge :

- Photo de l'employé (si activée et téléchargée).
- Nom, rôle, département et autres champs activés.
- QR code (si activé).
- Logo de l'entreprise (si activé).
- Couleurs et mise en page du modèle du Badge Designer.

**Verso** : Le téléchargement PNG individuel et l'exportation ZIP incluent uniquement le **recto** du badge. Pour imprimer le verso, utilisez le flux d'impression du navigateur (Groupé → Tout Imprimer) qui inclut automatiquement les pages du verso.

---

## Images Cross-Origin

Les photos des employés, les logos et les images d'arrière-plan hébergés sur des URL externes sont automatiquement convertis en données intégrées pour l'exportation. Cela garantit que les images apparaissent correctement dans le PNG même si le CDN applique des restrictions d'accès.

Si une photo ne parvient pas à se charger pendant l'exportation, le badge sera généré sans la photo plutôt que d'échouer complètement. Vérifiez que la photo de l'employé est bien téléchargée dans sa fiche.

---

## Cas d'Utilisation

| Scénario                                                        | Méthode recommandée                                                        |
| --------------------------------------------------------------- | -------------------------------------------------------------------------- |
| Envoi de badges à une imprimerie commerciale                    | Exportation ZIP groupée — envoyez le ZIP avec les fichiers PNG individuels |
| Création de cartes d'identité numériques pour un import système | Exportation ZIP groupée                                                    |
| Impression interne sur une imprimante de bureau                 | Impression via navigateur (Individuelle ou Groupée)                        |
| Archivage du badge d'un employé spécifique                      | Téléchargement PNG individuel                                              |
| Envoi numérique d'un badge à un employé                         | Téléchargement PNG individuel, pièce jointe par e-mail                     |
