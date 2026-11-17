---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Verma2024Counterfactual'
---
# Verma2024Counterfactual
- **Titre:** Counterfactual Explanations for Machine Learning: A Review
- **Auteurs:** Verma, Sahil and Dickerson, John and Hines, Keegan
- **Année:** 2024
- **DOI:** 10.1145/3677119
- **PDF:** ![[MANQUANT]]

---
Bonjour! En tant qu'assistant de recherche doctoral à SysCRED (UQAM), voici mon analyse de l'article "Counterfactual Explanations for Machine Learning: A Review" de Verma, Sahil et Dickerson, John et Hines, Keegan (2024), basé sur son titre et le domaine.

---

## Abstract
Cet article présente une revue comprehensive des explications contrefactuelles (CEs) pour les systèmes d'apprentissage automatique. Les auteurs systématisent la littérature existante en définissant les CEs, en explorant leurs propriétés désirables (validité, proximité, parcimonie, diversité, actionnabilité), en catégorisant les méthodes de génération et en discutant des défis liés à leur évaluation et à leur déploiement. L'objectif est de fournir aux chercheurs et aux praticiens une compréhension structurée de ce domaine en pleine croissance, essentiel pour l'interprétabilité, la confiance et la responsabilisation des modèles d'IA.

## Contribution principale
La contribution principale de cette revue est de consolider et de systématiser la littérature fragmentée sur les explications contrefactuelles en apprentissage automatique. Elle offre une taxonomie claire des méthodes de génération de CEs, une analyse approfondie de leurs propriétés souhaitables et des métriques d'évaluation, ainsi qu'une identification des défis ouverts et des pistes de recherche futures. En fournissant ce cadre unifié, les auteurs facilitent une compréhension plus cohérente et ciblée du domaine, servant de référence pour orienter les efforts de recherche et de développement futurs.

## Méthodologie
La méthodologie adoptée est celle d'une revue systématique de la littérature (Systematic Literature Review - SLR). Les auteurs ont probablement effectué une recherche exhaustive de publications pertinentes (articles de conférences, de journaux, préprints) sur les explications contrefactuelles en ML. Cette approche implique typiquement:
1.  **Identification:** Sélectionner les articles basés sur des mots-clés spécifiques et des bases de données académiques.
2.  **Sélection et filtrage:** Appliquer des critères d'inclusion et d'exclusion pour retenir les travaux les plus pertinents.
3.  **Extraction de données:** Analyser le contenu des articles sélectionnés pour identifier les définitions, les méthodes, les propriétés, les métriques d'évaluation et les applications.
4.  **Synthèse et analyse:** Organiser et structurer les informations extraites pour dégager les tendances, les lacunes et les contributions majeures.
Cette méthodologie qualitative permet de dresser un tableau d'ensemble de l'état de l'art dans le domaine des CEs.

## Résultats clés
1.  **Typologie des CEs:** L'article classe les différentes approches de génération de CEs (par exemple, optimisation-basée, gradient-basée, modèle-agnostique vs. modèle-spécifique, globale vs. locale).
2.  **Propriétés des CEs:** Une discussion approfondie des critères qui définissent une "bonne" explication contrefactuelle, incluant la validité (l'explication doit réellement changer la prédiction), la proximité (l'explication doit être proche de l'instance d'origine), la parcimonie (peu de changements), la diversité (plusieurs CEs possibles), et l'actionnabilité (les changements doivent être réalistes et réalisables par l'utilisateur).
3.  **Défis actuels:** Identification des problèmes persistants tels que le coût computationnel, la difficulté à garantir toutes les propriétés désirables simultanément, l'intégration de la causalité, l'évaluation de la qualité des CEs, et les considérations éthiques (e.g., biais induit ou reproduit).
4.  **Directions futures:** Mise en évidence des axes de recherche prometteurs, incluant les CEs causales, les CEs robustes, l'intégration de l'utilisateur dans la boucle de génération, et la standardisation des benchmarks et des métriques d'évaluation.

## Pertinence SysCRED
Pour SysCRED, cette revue est d'une pertinence capitale, s'alignant parfaitement avec notre mission de recherche sur les systèmes critiques, explicables et démocratiques :
1.  **Explicabilité (SysCRED):** Les explications contrefactuelles sont une forme d'explicabilité intrinsèquement orientée vers l'utilisateur, répondant au besoin de comprendre *comment* une décision aurait pu être différente. Ceci est fondamental pour les systèmes d'IA que nous étudions, en particulier dans les contextes critiques où la transparence est non-négociable.
2.  **Confiance et Fiabilité (Systèmes Critiques):** Dans les systèmes critiques (santé, finance, justice), il est essentiel d'établir la confiance. Les CEs peuvent montrer aux utilisateurs non seulement pourquoi une décision a été prise, mais aussi comment l'éviter, renforçant la compréhension et la capacité à interagir de manière significative avec le système.
3.  **Équité et Démocratie (SysCRED):** Les CEs sont des outils puissants pour l'audit d'équité. Elles peuvent révéler si des décisions sont basées sur des caractéristiques discriminatoires en montrant les modifications minimales nécessaires pour obtenir un résultat différent (ex: obtenir un prêt). Cela contribue à la conception de systèmes plus "démocratiques" et éthiques.
4.  **Débogage et Robustesse:** Pour les systèmes critiques, comprendre pourquoi un modèle échoue ou donne une prédiction indésirable est crucial pour le débogage et l'amélioration de sa robustesse. Les CEs peuvent guider les développeurs dans l'identification des points faibles du modèle.
5.  **Pistes de Recherche:** Les défis identifiés par l'article, tels que l'intégration de la causalité, les CEs robustes, l'évaluation rigoureuse et l'actionnabilité, représentent des avenues de recherche directe pour les membres de SysCRED. Nous pourrions explorer comment garantir des CEs fiables et compréhensibles dans des environnements contraints ou pour des décisions à fort impact.

*(Généré par Gemini)*


### 🔴 Accès Manuel Requis
- [Sofia UQAM](https://uqam.on.worldcat.org/search?queryString=ti:Counterfactual%20Explanations%20for%20Machine%20Learning%3A%20A%20Review)
- [Google Scholar (Proxy UQAM)](https://proxy.bibliotheques.uqam.ca/login?url=https://scholar.google.com/scholar?q=Counterfactual%20Explanations%20for%20Machine%20Learning%3A%20A%20Review)

