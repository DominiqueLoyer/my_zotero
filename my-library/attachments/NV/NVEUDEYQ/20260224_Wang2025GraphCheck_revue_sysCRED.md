---
Date: '20260224'
tags: [ia/neuro-symbolique, uqam, dic9411, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-24 - Wang2025GraphCheck'
---

# RHO (ρ): Reducing Hallucination in Open-domain Dialogues with Knowledge Grounding" par Ji et al. (2023),
- **Titre:** Integrating Knowledge Graphs with Large Language Models for Hallucination Reduction
- **Auteurs:** Wang, Y. and Cohen, W. W.
- **Année:** 2025
- **PDF:** ![[Wang_2025_Integrating_Knowledge_Graphs.pdf]]
- **DOI:** 

---
En tant qu'assistant de recherche doctoral (UQAM, Informatique cognitive, SysCRED), voici l'analyse de l'extrait fourni, qui provient de l'article "RHO (ρ): Reducing Hallucination in Open-domain Dialogues with Knowledge Grounding" par Ji et al. (2023), plutôt que celui de Wang et Cohen (2025).

## Abstract
L'article "RHO (ρ): Reducing Hallucination in Open-domain Dialogues with Knowledge Grounding" de Ji et al. (2023) s'attaque au problème des hallucinations dans les systèmes de dialogue ouverts utilisant des modèles de langage et des graphes de connaissances (KG). Il propose RHO, une approche qui combine des embeddings textuels et de KG via des mécanismes de "grounding" local et global, et introduit une technique de re-classement des réponses. Cette méthode vise à générer des réponses plus fidèles en réduisant les hallucinations intrinsèques et extrinsèques.
	
## Contribution principale
- Introduction de RHO, un cadre qui exploite les représentations d'entités et de prédicats de relation issus d'un graphe de connaissances pour réduire les hallucinations.
- Proposition d'un mécanisme de "grounding" de connaissances local combinant les embeddings textuels avec les embeddings correspondants du KG.
- Développement d'un "grounding" de connaissances global pour doter le modèle de capacités de raisonnement multi-sauts via le mécanisme d'attention.
- Conception d'une technique de re-classement des réponses basée sur des parcours de sous-graphes du KG pour améliorer le raisonnement conversationnel et la fidélité.

## Méthodologie
RHO intègre les graphes de connaissances à travers deux mécanismes de "grounding" principaux. Le "grounding" local fusionne les embeddings textuels avec les embeddings correspondants des entités et prédicats de relation extraits du KG. Le "grounding" global, via un mécanisme d'attention, permet d'équiper le modèle de capacités de raisonnement multi-sauts sur le KG, enrichissant ainsi la compréhension du contexte et la pertinence des connaissances. En complément, une technique de re-classement des réponses est employée, analysant des parcours sur des sous-graphes du KG pour sélectionner la réponse la plus cohérente et fidèle, réduisant ainsi les risques d'hallucination.

## Résultats clés
- Surpasse significativement les méthodes de pointe existantes sur les évaluations automatiques et humaines sur le jeu de données OpenDialKG.
- Démontre une réduction substantielle des hallucinations, avec une amélioration notable de 17.54% sur l'indicateur FeQA.
- Améliore la fidélité et la cohérence des réponses générées par les systèmes de dialogue basés sur la connaissance.

## Pertinence SysCRED
Ce travail est hautement pertinent pour SysCRED en ce qu'il incarne une approche prometteuse d'IA neuro-symbolique, en intégrant des connaissances symboliques structurées (graphes de connaissances/ontologies) dans des modèles neuronaux pour améliorer leur performance. La réduction des hallucinations est cruciale pour la crédibilité des systèmes d'IA : en garantissant que les réponses générées sont fidèles et vérifiables, cette recherche contribue directement à bâtir des systèmes plus fiables et dignes de confiance. Dans le contexte de la bureaucratie algorithmique, où la précision et la traçabilité sont primordiales, des systèmes de dialogue moins sujets aux hallucinations sont essentiels pour prévenir la désinformation, assurer l'intégrité des processus automatisés et maintenir la confiance du public dans les décisions prises par les algorithmes.

*(Généré par Gemini 2.5)*

