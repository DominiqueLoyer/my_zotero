---
Date: '20260303'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-03-03 - Mikolov2020Efficient'
---
# Mikolov2020Efficient
- **Titre:** Efficient Estimation of Word Representations in Vector Space
- **Auteurs:** Mikolov, Tomas and Chen, Kai and Corrado, Greg S. and Dean, Jeffrey
- **Année:** 2020
- **DOI:** 10.3126/jiee.v3i1.34327
- **PDF:** ![[Mikolov_2020_Efficient_Estimation_of.pdf]]

---
## Abstract
L'article propose deux nouvelles architectures de modèles pour calculer des représentations vectorielles continues de mots à partir de très grands ensembles de données. La qualité de ces représentations est mesurée dans une tâche de similarité de mots et les résultats sont comparés aux techniques précédentes basées sur différents types de réseaux de neurones.

## Contribution principale
La contribution principale de cet article est l'introduction de nouvelles techniques pour apprendre des vecteurs de mots de haute qualité à partir de grands ensembles de données, avec des millions de mots dans le vocabulaire, tout en réduisant les coûts de calcul.

## Méthodologie
Les auteurs proposent deux nouvelles architectures de modèles pour calculer des représentations vectorielles de mots : 
- La première architecture utilise une approche de type "skip-gram" pour prédire les mots contextuels à partir d'un mot cible.
- La deuxième architecture utilise une approche de type "CBOW" (Continuous Bag-of-Words) pour prédire un mot cible à partir de ses mots contextuels.
Les auteurs utilisent également des techniques de mesure de la qualité des représentations vectorielles, telles que la tâche de similarité de mots, pour évaluer les performances de leurs modèles.

## Résultats clés
Les résultats clés de cet article sont :
- Les nouvelles architectures de modèles proposées atteignent de meilleures performances que les techniques précédentes basées sur différents types de réseaux de neurones.
- Les vecteurs de mots appris à l'aide de ces architectures atteignent des performances de pointe sur un ensemble de test pour mesurer les similarités syntaxiques et sémantiques de mots.
- Les auteurs montrent que ces vecteurs peuvent être appris en moins d'une journée à partir d'un ensemble de données de 1,6 milliard de mots.

## Pertinence SysCRED
Cet article est pertinent pour le domaine du traitement automatique des langues (TAL) et de l'apprentissage automatique, qui sont des domaines clés de recherche au sein du laboratoire SysCRED de l'UQAM. Les résultats de cet article pourraient être utilisés pour améliorer les performances de systèmes de TAL tels que les systèmes de reconnaissance de la parole, les systèmes de traduction automatique et les systèmes de recherche d'information. De plus, les techniques proposées dans cet article pourraient être appliquées à d'autres domaines tels que la fouille de textes, la détection de sentiments et l'analyse de réseaux sociaux.

*(Généré par Groq)*

