# Contexte de Développement - Quiz Civique

Ce document sert de trace écrite pour assurer la transition du développement du site **Quiz Civique** sur un nouvel ordinateur avec Antigravity.

## Présentation du Projet
* **Description** : Une application web monopage (SPA) d'entraînement à l'examen civique pour l'obtention de la nationalité française.
* **Architecture** : L'intégralité de l'application est contenue dans un unique fichier portable `index.html` (HTML/CSS/JS natif) pour un fonctionnement 100% hors-ligne.
* **Design** : Charte graphique premium de style Obsidian (thème sombre/clair automatique, boutons vitrés, typographies soignées).
* **Illustration** : Favicon et logo épurés avec l'icône du coq républicain.

---

## Dernières Modifications Effectuées (Juin 2026)

### 1. Amélioration des Distracteurs (Mauvaises Réponses)
* **Problème** : Les fausses options des QCM de connaissances étaient piochées au hasard dans la base globale, rendant les réponses évidentes (ex: questions historiques avec des fausses options concernant le droit du travail).
* **Solution** : Régénération complète de la base de questions dans `index.html` avec des règles de cohérence :
  * **Dates** : Les mauvaises options proposent des années historiques proches.
  * **Chiffres/Montants** : Les options conservent les mêmes unités (ex: euros, ans) avec d'autres ordres de grandeur.
  * **Noms propres** : Remplacement par d'autres noms du même domaine (ex: personnages célèbres, fleuves, villes).
  * **Textes longs** : Pioche uniquement au sein de la même catégorie et de longueur similaire (±45%) pour éviter les indices visuels.
* *Note : Les questions de mise en situation (cas pratiques) conservent leurs options rédigées sur mesure.*

### 2. Correction du Nombre de Questions en Mode Examen (38 → 40)
* **Problème** : L'examen blanc piochait 28 questions de connaissances et jusqu'à 12 questions de mise en situation. Le pool n'en contenant que 10, le test ne faisait que 38 questions.
* **Solution** :
  * Ajout de **5 nouvelles questions de mise en situation** rédigées de manière réaliste (portant le pool à 15).
  * Modification de la fonction `startExamMode()` dans `index.html` pour calculer dynamiquement les proportions : si le pool de mises en situation est trop restreint, le script compense en prenant plus de questions de connaissances pour garantir **toujours exactement 40 questions**.

---

## État des Fichiers et Synchronisation
* **`index.html`** : Contient le code de l'application mis à jour (base de questions + logique dynamic-slice de l'examen).
* **`CONTEXTE.md`** : Ce fichier de transition.
* **`README.md`** : Guide général d'installation et d'utilisation (sans emojis, conforme aux règles d'attribution de l'IA).
* **`.gitignore`** : Exclut les fichiers temporaires et les documents PDF/Docx lourds.

---

## Étapes de Validation (sur la nouvelle machine)
1. Cloner le dépôt depuis GitHub.
2. Ouvrir `index.html` dans n'importe quel navigateur moderne.
3. Lancer une **Simulation d'Examen Officiel** (mode examen) et vérifier :
   * Que le compteur indique bien un total de 40 questions (ex: `1 / 40`).
   * Que les distracteurs des questions de connaissances (ex: dates) sont cohérents et crédibles.
