---
Date: '20260304'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-03-04 - Bahdanau2021Neural'
---
# Bahdanau2021Neural
- **Titre:** Neural Machine Translation by Jointly Learning to Align and Translate
- **Auteurs:** Bahdanau, Dzmitry and Cho, Kyunghyun and Bengio, Yoshua
- **Année:** 2021
- **DOI:** 10.18653/v1/2021.emnlp-main.1
- **PDF:** ![[Bahdanau_2021_Neural_Machine_Translation.pdf]]

---
## Abstract
L'article présente une approche de traduction automatique neuronale qui apprend à aligner et à traduire conjointement, améliorant ainsi la performance de la traduction. Cette approche s'écarte de la méthode traditionnelle d'encodage d'une phrase source dans un vecteur de longueur fixe, mais plutôt encode la phrase source dans une séquence de vecteurs et choisit un sous-ensemble de ces vecteurs de manière adaptative pendant la décodage de la traduction.

## Contribution principale
La contribution principale de cet article est l'introduction d'une extension au modèle encodeur-décodeur qui apprend à aligner et à traduire conjointement, permettant ainsi au modèle de (re)chercher de manière douce les parties d'une phrase source pertinentes pour prédire un mot cible, sans avoir à former ces parties en segments explicites.

## Méthodologie
La méthodologie utilisée dans cet article consiste à étendre le modèle encodeur-décodeur de base en permettant au modèle de (re)chercher de manière douce les parties d'une phrase source pertinentes pour prédire un mot cible. Cela se fait en encodant la phrase source dans une séquence de vecteurs et en choisissant un sous-ensemble de ces vecteurs de manière adaptative pendant la décodage de la traduction.

## Résultats clés
Les résultats clés de cet article sont que l'approche proposée atteint une performance de traduction comparable à celle des systèmes de traduction basés sur des phrases existants pour la tâche de traduction anglais-français. De plus, l'analyse qualitative révèle que les alignements (doux) trouvés par le modèle sont en accord avec notre intuition.

## Pertinence SysCRED
Cette recherche est pertinente pour le domaine du SysCRED car elle explore les applications des réseaux de neurones pour la traduction automatique, ce qui est un domaine clé dans le traitement automatique des langues. Les résultats de cette recherche pourraient être utilisés pour améliorer les systèmes de traduction automatique, ce qui est essentiel pour la communication internationale et la diffusion de l'information. De plus, les méthodes proposées dans cet article pourraient être appliquées à d'autres tâches de traitement automatique des langues, telles que la reconnaissance de la parole ou la classification de texte.

*(Généré par Groq)*

