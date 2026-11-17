---
Date: '20260224'
tags: [ia/neuro-symbolique, uqam, dic9411, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-24 - Mao2019NSCL'
---

# Mao2019NSCL
- **Titre:** The Neuro-Symbolic Concept Learner: Interpreting Scenes, Words, and Sentences
- **Auteurs:** Mao, Jiayuan and others
- **Année:** 2019
- **PDF:** ![[Mao_2019_The_Neuro_Symbolic.pdf]]
- **DOI:** 

---
## Abstract
Le Neuro-Symbolic Concept Learner (NS-CL) est un modèle qui apprend les concepts visuels, les mots et l'analyse sémantique de phrases à partir d'images et de paires de questions-réponses, sans supervision explicite. Il y parvient en construisant une représentation de scène basée sur les objets et en traduisant les phrases en programmes symboliques exécutables, le tout orchestré par un module de raisonnement neuro-symbolique. Ce modèle permet un apprentissage conjoint et une généralisation efficace sur diverses tâches visuelles et linguistiques.

## Contribution principale
- Propose un modèle neuro-symbolique capable d'apprendre des concepts visuels, des représentations de mots et l'analyse sémantique de phrases sans supervision explicite, uniquement à partir d'images et de paires question-réponse.
- Introduit une architecture modulaire combinant la perception neuronale, l'analyse sémantique visuellement ancrée et l'exécution de programmes symboliques pour le raisonnement.
- Démontre une capacité d'apprentissage mutuel où les concepts visuels facilitent l'apprentissage linguistique, et vice-versa, à l'image de l'apprentissage humain.

## Méthodologie
Le NS-CL est composé d'un module de perception neuronale qui extrait des représentations d'objets à partir des scènes, d'un parseur sémantique ancré visuellement qui traduit les questions en programmes symboliques exécutables, et d'un exécuteur de programme symbolique qui interprète ces programmes sur les représentations latentes de la scène pour obtenir une réponse. Un module de raisonnement neuro-symbolique assure la liaison et l'exécution entre ces composants, tandis que l'apprentissage par curriculum est employé pour guider la recherche dans l'espace compositionnel complexe des images et du langage.

## Résultats clés
- Démontre une grande précision et efficacité dans l'apprentissage des concepts visuels, des représentations de mots et de l'analyse sémantique.
- Offre une excellente capacité de généralisation à de nouveaux attributs d'objets, compositions, concepts linguistiques, scènes et questions, et même à de nouveaux domaines de programme.
- Permet des applications pratiques telles que la réponse visuelle aux questions (VQA) et la récupération bidirectionnelle image-texte.

## Pertinence SysCRED
Le NS-CL est fondamentalement pertinent pour SysCRED grâce à son approche neuro-symbolique, fusionnant des modules neuronaux pour la perception et des modules symboliques pour le raisonnement et l'exécution de programmes. Cette architecture permet d'ancrer des connaissances symboliques (similaires à des ontologies) à partir de données visuelles et linguistiques. La traduction des requêtes en programmes exécutables symboliques offre une traçabilité et une interprétabilité cruciales pour la crédibilité des systèmes d'IA, permettant de justifier et d'auditer les décisions. Cette capacité à décomposer des questions complexes en étapes logiques s'aligne directement avec la modélisation et la compréhension de la "bureaucratie algorithmique", où des règles et procédures peuvent être encodées et exécutées de manière transparente et vérifiable.

*(Généré par Gemini 2.5)*

