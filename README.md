# Quiz civique — Examen de naturalisation française

Ce dépôt contient une application web permettant de s'entraîner à l'examen civique officiel requis pour l'obtention de la carte de séjour pluriannuelle, la carte de résident ou la naturalisation.

Le contenu est conforme à l'arrêté officiel du 10 octobre 2025 et regroupe les 368 questions de connaissances.

L'application est accessible en ligne à cette adresse : [https://matthieubillard.github.io/quiz-citoyen/](https://matthieubillard.github.io/quiz-citoyen/)

---

## Fonctionnalités

* **Examen blanc** : simulation de l'épreuve officielle avec 40 questions aléatoires en 45 minutes (seuil d'admission fixé à 32 bonnes réponses).
* **Entraînement libre** : révisions par thématique avec correction immédiate et explications officielles pour chaque question.
* **Flashcards** : cartes d'auto-évaluation pour travailler la mémorisation active.
* **Fichiers de révision** : téléchargement du guide complet des 368 questions-réponses au format PDF ou Word (DOCX) directement sur la page d'accueil.
* **Interface adaptative** : le site est adapté aux smartphones et gère automatiquement les modes sombre et clair selon les préférences du système.

---

## Fichiers du projet

* `index.html` : page unique contenant le code de l'application et les données du QCM.
* `guide_revision_examen_civique.pdf` : guide de révision au format PDF.
* `guide_revision_examen_civique.docx` : guide de révision au format Word.
* `arrêté_examen_civique.md` : texte brut de l'arrêté du 10 octobre 2025.
* `build_doc.py` et `cat_*.py` : scripts Python de génération et de mise en page des documents.
* `thumbnail.png` : image d'aperçu pour le partage du lien.

---

## Utilisation hors-ligne

L'application est entièrement contenue dans le fichier `index.html`. Pour l'utiliser hors-ligne, il suffit de télécharger ce fichier et de l'ouvrir dans un navigateur. Aucune connexion ni serveur ne sont nécessaires.

---

## Méthode de création

Les questions et les réponses officielles ont été extraites du site officiel du ministère de l'Intérieur à l'aide d'un script d'automatisation de navigateur (Edge via le protocole Chrome DevTools).
Le livret de révision a été compilé à l'aide d'un script Python (librairie `python-docx`) puis exporté en PDF.

---

## Avertissement

Ce site est un outil d'entraînement personnel indépendant et n'est pas affilié au gouvernement français.
