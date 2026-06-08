# 🐓 Quiz Civique — Examen de Naturalisation Française

[![Pages-deploiement](https://img.shields.io/badge/GitHub%20Pages-Actif-success?style=flat-square&logo=github)](https://matthieubillard.github.io/quiz-citoyen/)
[![HTML5](https://img.shields.io/badge/HTML5-100%25-orange?style=flat-square&logo=html5)](index.html)
[![Licence](https://img.shields.io/badge/Licence-MIT-blue?style=flat-square)](LICENSE)

Une application web interactive, moderne et 100% autonome pour préparer efficacement l'**examen civique obligatoire** requis pour l'obtention de la carte de séjour pluriannuelle, la carte de résident ou la naturalisation française.

Le contenu est entièrement conforme au référentiel officiel défini par l'**Arrêté du 10 octobre 2025** (regroupant l'intégralité des 368 questions de connaissances).

👉 **[Accéder au Quiz en ligne](https://matthieubillard.github.io/quiz-citoyen/)**

---

## 🌟 Fonctionnalités

* **⏱️ Examen Blanc** : Une simulation dans les conditions réelles de l'épreuve officielle (40 questions aléatoires en 45 minutes, avec un seuil de réussite de 80% soit 32 bonnes réponses).
* **🎯 Entraînement Libre** : Révisez à votre rythme en choisissant parmi les 5 thématiques officielles. Cette formule propose une correction immédiate avec des explications détaillées et officielles pour chaque question.
* **🎴 Flashcards** : Un outil de révision active pour mémoriser les réponses et s'auto-évaluer en retournant virtuellement les cartes.
* **📄 Guide de Révision Téléchargeable** : L'intégralité des 368 questions-réponses officielles compilée dans un guide de révision mis en page, téléchargeable directement sur la page d'accueil aux formats **PDF** et **Word (DOCX)**.
* **🌓 Mode Sombre / Clair Automatique** : L'interface s'adapte de manière transparente aux préférences de votre système d'exploitation.
* **📱 100% Responsive & Tactile** : Une conception soignée et mobile-friendly pour pouvoir réviser en déplacement sur smartphone et tablette.

---

## 📂 Structure du Projet

Le dépôt est conçu de façon simple et portable :
* [`index.html`](index.html) : L'application web interactive complète. Elle est entièrement autonome (styles CSS, logique JavaScript et la base de données de 368 questions y sont intégrés).
* [`guide_revision_examen_civique.pdf`](guide_revision_examen_civique.pdf) : Le livret de révision officiel compilé au format PDF.
* [`guide_revision_examen_civique.docx`](guide_revision_examen_civique.docx) : Le guide au format Microsoft Word.
* [`arrêté_examen_civique.md`](arrêté_examen_civique.md) : Le texte intégral brut de l'Arrêté officiel du 10 octobre 2025.
* [`build_doc.py`](build_doc.py) et les scripts `cat_*.py` : Le script Python de compilation de documents utilisé pour générer et styliser le guide Word à partir de la base de données.
* [`thumbnail.png`](thumbnail.png) : L'image d'illustration officielle utilisée pour l'aperçu du lien lors des partages (Open Graph).

---

## 💻 Utilisation en Local / Hors-ligne

L'un des grands avantages de ce projet est sa **portabilité**. Comme l'application est contenue dans un unique fichier statique :
1. Téléchargez le fichier [`index.html`](index.html) (ou clonez ce dépôt).
2. Double-cliquez sur le fichier pour l'ouvrir dans n'importe quel navigateur (Chrome, Firefox, Safari, Edge).
3. **Aucune connexion internet n'est requise** : l'application fonctionne parfaitement hors-ligne, sans base de données externe ni serveur.

---

## 🛠️ Coulisses Techniques & Scraping

Ce projet a été réalisé en plusieurs étapes clés :
1. **Scraping** : Extraction des 368 questions-réponses uniques directement depuis le site officiel ministériel. Pour contourner les protections Cloudflare, un script Node.js automatisé via le protocole Chrome DevTools (CDP) sur Microsoft Edge a été développé.
2. **Compilation Word** : Génération automatisée du livret avec la bibliothèque `python-docx`, en appliquant une charte graphique premium (styles de tableaux alternés, cantSplit pour l'impression, polices institutionnelles).
3. **Conversion PDF** : Export automatisé via le moteur de rendu Word COM (Automation Windows) afin de préserver les polices et marges à 100%.

---

## 📜 Mentions Légales

*Ce projet est un outil d'apprentissage privé indépendant, conçu à des fins éducatives de révision. Il n'est pas affilié, associé ou approuvé officiellement par le ministère de l'Intérieur ou le gouvernement français.*
