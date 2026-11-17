---
Date: '20260224'
tags: [ia/neuro-symbolique, uqam, dic9411, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-24 - Mao2019NSCLCorrected'
---

# Mao2019NSCLCorrected
- **Titre:** The Neuro-Symbolic Concept Learner: Interpreting Scenes Words and Sentences From Natural Supervision
- **Auteurs:** Mao, Jiayuan and Gan, Chuang and Kohli, Pushmeet and Tenenbaum, Joshua B and Wu, Jiajun
- **Année:** 2019
- **PDF:** ![[Mao_2019_The_Neuro_Symbolic.pdf]]
- **DOI:** 

---
## Abstract
Le Neuro-Symbolic Concept Learner (NS-CL) est un modèle qui apprend les concepts visuels, les mots et l'analyse sémantique de phrases sans supervision explicite, en s'appuyant uniquement sur des images et des paires questions-réponses. Il construit une représentation de scène basée sur les objets et traduit les phrases en programmes symboliques exécutables, utilisant un module de raisonnement neuro-symbolique pour les exécuter sur la représentation latente.

## Contribution principale
- Apprentissage conjoint de la perception visuelle, des représentations de mots et de l'analyse sémantique de phrases à partir de supervision naturelle (paires image-question-réponse).
- Proposition d'une architecture neuro-symbolique qui combine un module de perception neural, un parseur sémantique visuellement ancré et un exécuteur de programme symbolique.
- Capacité à généraliser facilement à de nouveaux attributs d'objets, compositions, concepts linguistiques, scènes et questions, et même à de nouveaux domaines de programme.

## Méthodologie
Le NS-CL est composé de trois modules principaux. Un module de perception basé sur les réseaux neuronaux extrait des représentations au niveau des objets à partir des scènes. Un parseur sémantique ancré visuellement traduit les questions en programmes symboliques exécutables. Enfin, un module de raisonnement neuro-symbolique exécute ces programmes sur la représentation latente de la scène, classifiant les attributs/relations des objets pour obtenir une réponse. L'apprentissage des concepts visuels et linguistiques s'effectue de manière interdépendante, guidé par une approche de curriculum learning.

## Résultats clés
- Démonstration de l'exactitude et de l'efficacité du modèle pour l'apprentissage des concepts visuels, des représentations de mots et de l'analyse sémantique des phrases.
- Grande capacité de généralisation à de nouveaux attributs d'objets, compositions, concepts linguistiques, scènes, questions et domaines de programme.
- Habilitation d'applications telles que la réponse visuelle aux questions (VQA) et la récupération bidirectionnelle image-texte.

## Pertinence SysCRED
Cet article est hautement pertinent pour SysCRED car il incarne une approche fondamentale de l'**IA neuro-symbolique**, en combinant la robustesse des systèmes neuronaux pour la perception avec la capacité de raisonnement structuré des systèmes symboliques. Le modèle apprend des concepts et des relations, ce qui peut être vu comme la construction implicite d'**ontologies** ou de schémas de connaissances du monde, essentiels pour des systèmes d'IA crédibles et interprétables. La capacité à interpréter des scènes et des phrases de manière compositionnelle et à généraliser fournit une base pour des systèmes plus transparents, contribuant ainsi à la **crédibilité** de l'IA. En permettant une interprétation plus riche et structurée du langage et des images, cela pourrait informer le développement de systèmes pour la **bureaucratie algorithmique** capables de comprendre des requêtes complexes et de justifier leurs "décisions" en se référant à des concepts et des règles identifiables.

*(Généré par Gemini 2.5)*

