---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, dic9411, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Hagag2023'
---

# Hagag2023
- **Titre:** The Truth, The Whole Truth, and Nothing but the Truth: A New Benchmark Dataset for Hebrew Text Credibility Assessment
- **Auteurs:** Hagag, Ben and Tsarfaty, Reut
- **Année:** 2023
- **PDF:** ![[Hagag_2023_The_Truth_The.pdf]]
- **DOI:** 

---
## Abstract
Cet article présente HeTrue, un nouveau dataset public de 1021 déclarations en hébreu de personnalités publiques israéliennes, manuellement annotées pour leur crédibilité par des journalistes professionnels. Les auteurs évaluent la prédiction automatique de la crédibilité, comparant des méthodes textuelles pures à celles intégrant contexte et preuves. Les résultats montrent que l'intégration du contexte et des preuves améliore la performance, bien que la tâche reste un défi avec un score F1 maximal de 48.3.

## Contribution principale
- Introduction de HeTrue, un nouveau dataset public pour l'évaluation de la crédibilité de textes en hébreu, spécifiquement des déclarations de personnalités publiques et politiques israéliennes.
- Le dataset est composé de 1021 déclarations, manuellement annotées pour leur statut de crédibilité par des journalistes professionnels israéliens.
- Établissement d'une base de référence pour l'évaluation de la crédibilité, comparant les méthodes basées uniquement sur le texte avec celles intégrant des données additionnelles (métadonnées, contexte, preuves).
- Développement de plusieurs modèles d'évaluation de la crédibilité, y compris des modèles basés sur des caractéristiques linguistiques et des transformeurs de pointe.

## Méthodologie
La méthodologie s'appuie sur le dataset HeTrue pour évaluer si la crédibilité des déclarations peut être prédite à partir du texte seul ou en intégrant des informations additionnelles. Pour ce faire, les auteurs comparent des méthodes basées uniquement sur le texte avec d'autres qui utilisent des données supplémentaires comme les métadonnées, le contexte et les preuves. Plusieurs modèles d'évaluation de la crédibilité sont développés, notamment un modèle basé sur des caractéristiques linguistiques et des modèles transformeurs de pointe utilisant des embeddings contextualisés.

## Résultats clés
- Les résultats empiriques démontrent une performance améliorée lorsque les modèles intègrent à la fois la déclaration et son contexte, surpassant ceux qui se basent uniquement sur le texte de la déclaration.
- Le meilleur modèle développé, qui intègre également des preuves, atteint un score F1 de 48.3.
- Le dataset HeTrue est identifié comme un benchmark exigeant, indiquant la nécessité de travaux supplémentaires pour améliorer la performance sur cette tâche d'évaluation de la crédibilité.

## Pertinence SysCRED
Ce travail est directement pertinent pour SysCRED, car il adresse le défi fondamental de l'évaluation automatique de la crédibilité de l'information, un axe de recherche clé du laboratoire en Informatique cognitive. L'intégration du "contexte" et des "preuves" pour améliorer la performance souligne la nécessité de capacités de raisonnement sophistiquées, suggérant un rôle important pour l'IA neuro-symbolique. Cette approche pourrait combiner la robustesse des modèles neuronaux (comme les transformeurs) avec des représentations symboliques (potentiellement via des ontologies) pour structurer et interpréter les preuves et le contexte, permettant ainsi aux systèmes de mieux comprendre la sémantique et la provenance des informations pour une évaluation de crédibilité plus fiable et explicable.

*(Généré par Gemini)*

