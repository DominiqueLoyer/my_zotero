---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, dic9411, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Nabozny2021'
---

# Nabozny2021
- **Titre:** Active Annotation in Evaluating the Credibility of Web-Based Medical Information: Guidelines for Creating Training Data Sets for Machine Learning
- **Auteurs:** Nabozny, Aleksandra and Marcinkiewicz, Michal and Nielek, Radoslaw and Wierzbicki, Adam
- **Année:** 2021
- **PDF:** ![[Nabozny_2021_Active_Annotation_in.pdf]]
- **DOI:** 10.2196/26065

---
## Abstract
Cet article présente un cadre complet pour la conception et la curation d'ensembles de données d'entraînement pour l'apprentissage automatique, spécifiquement pour l'évaluation de la crédibilité de l'information médicale en ligne. Face à la prolifération rapide de la désinformation médicale, l'étude propose des lignes directrices pour construire des processus d'annotation efficaces. Son objectif principal est de soutenir les chercheurs en médecine et en informatique dans la lutte contre la désinformation.

## Contribution principale
-   Présentation d'un cadre complet pour la conception et la curation d'ensembles de données d'entraînement en apprentissage automatique pour l'évaluation de la crédibilité de l'information médicale en ligne.
-   Proposition de lignes directrices pour la préparation de jeux de données, notamment un protocole d'annotation pour les experts médicaux.
-   Développement d'un processus d'annotation active combinant l'apprentissage de représentations, le regroupement (clustering) et le ré-ordonnancement (reranking) pour une annotation plus efficace.

## Méthodologie
La méthode débute par la fourniture d'un protocole d'annotation destiné aux experts médicaux pour l'évaluation de la crédibilité de phrases médicales, basé sur une étude qualitative de données expérimentales. Pour pallier le problème du manque d'étiquettes initiales, les auteurs proposent un pipeline de prétraitement pour les lots de phrases à évaluer, appelé annotation active, qui inclut l'apprentissage de représentations, le regroupement et le ré-ordonnancement.

## Résultats clés
-   Collecte de plus de 10 000 annotations de déclarations liées à huit sujets médicaux spécifiques (psychiatrie, cholestérol, autisme, antibiotiques, vaccins, stéroïdes, méthodes d'accouchement, tests d'allergies alimentaires).
-   Coût de la collecte des annotations inférieur à 7 000 USD, réalisées par 9 annotateurs hautement qualifiés (professionnels de la santé certifiés).
-   Libération de l'ensemble de données collecté au grand public.
-   Développement d'un cadre d'annotation active pour une annotation plus efficace des déclarations médicales non crédibles.
-   L'application de l'analyse qualitative a permis d'améliorer le protocole d'annotation pour les efforts futurs.

## Pertinence SysCRED
Cet article est hautement pertinent pour SysCRED car il aborde directement l'évaluation de la crédibilité de l'information, un pilier central de nos recherches. Le protocole d'annotation détaillé, basé sur l'expertise humaine, fournit une base pour l'intégration de connaissances symboliques, ce qui est crucial pour l'IA neuro-symbolique. Bien que les ontologies ne soient pas explicitement mentionnées, la structuration des annotations par sujets médicaux et l'implication d'experts suggèrent l'importance d'une représentation formelle du domaine, que les ontologies pourraient fournir pour enrichir les modèles d'apprentissage automatique et améliorer l'explicabilité des décisions de crédibilité. Le processus d'annotation active, combinant des méthodes ML et l'intervention humaine, peut inspirer des architectures neuro-symboliques itératives pour l'amélioration continue de la détection de la désinformation.

*(Généré par Gemini)*

