---
Date: '20260303'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-03-03 - Devlin2021Bert'
---
# Devlin2021Bert
- **Titre:** BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding
- **Auteurs:** Devlin, Jacob and Chang, Ming-Wei and Lee, Kenton and Toutanova, Kristina
- **Année:** 2021
- **DOI:** 10.1016/j.compbiomed.2021.104258
- **PDF:** ![[Devlin_2021_BERT_Pre_training.pdf]]

---
## Abstract
L'article présente BERT, un nouveau modèle de représentation de langage appelé Bidirectional Encoder Representations from Transformers. BERT est conçu pour pré-entraîner des représentations bidirectionnelles profondes à partir de texte non étiqueté en conditionnant conjointement à la fois le contexte gauche et droit dans toutes les couches.

## Contribution principale
La contribution principale de cet article est l'introduction de BERT, qui permet de pré-entraîner des représentations de langage bidirectionnelles en utilisant un objectif de pré-entraînement appelé "masked language model" (MLM). Cela permet à BERT de capturer le contexte à la fois gauche et droit pour chaque token, ce qui est particulièrement utile pour les tâches de traitement de langage naturel qui nécessitent une compréhension fine-graine du contexte.

## Méthodologie
La méthodologie utilisée pour développer BERT consiste à pré-entraîner un modèle de représentation de langage en utilisant un objectif de pré-entraînement MLM. Cela implique de masquer aléatoirement certains tokens du texte d'entrée et de demander au modèle de prédire le token original en fonction de son contexte. Le modèle est ensuite affiné pour des tâches spécifiques en ajoutant une couche de sortie supplémentaire.

## Résultats clés
Les résultats clés de l'article montrent que BERT obtient de nouveaux résultats de référence sur onze tâches de traitement de langage naturel, notamment en améliorant le score GLUE de 7,7 points absolus, la précision de MultiNLI de 4,6 points absolus et le score F1 de SQuAD v1.1 de 1,5 point absolu.

## Pertinence SysCRED
La pertinence de cet article pour le SysCRED est élevée, car il présente une nouvelle approche pour améliorer les performances des modèles de langage en utilisant des représentations bidirectionnelles. Cela peut avoir des implications importantes pour les applications de traitement de langage naturel dans le domaine de la santé, tels que la reconnaissance d'entités nommées, la classification de textes et la recherche d'information. Les résultats de cet article peuvent également être utilisés pour améliorer les performances des modèles de langage utilisés dans les systèmes de recommandation et de décision pour la santé.

*(Généré par Groq)*

