---
Date: '20260224'
tags: [ia/neuro-symbolique, uqam, dic9411, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-24 - Marconato2025ReasoningShortcuts'
---

# Marconato2025ReasoningShortcuts
- **Titre:** Symbol Grounding in Neuro-Symbolic AI: A Gentle Introduction to Reasoning Shortcuts
- **Auteurs:** Marconato, Emanuele and others
- **Année:** 2025
- **PDF:** ![[Marconato_2025_Symbol_Grounding_in.pdf]]
- **DOI:** 

---
## Abstract
Cet article présente une introduction aux "Reasoning Shortcuts" (RSs) dans l'IA neuro-symbolique (NeSy), un problème émergent où les modèles atteignent une grande précision d'étiquetage en "groundant" incorrectement les concepts. Ces RSs compromettent l'interprétabilité, la performance hors distribution et la fiabilité des modèles NeSy, rendant leur détection et prévention difficiles sans supervision directe des concepts. L'aperçu vise à unifier la littérature fragmentée sur les RSs, en détaillant leurs causes, conséquences, caractérisations théoriques et méthodes d'atténuation.

## Contribution principale
- Fournir une introduction accessible aux "Reasoning Shortcuts" (RSs) dans l'IA neuro-symbolique, en clarifiant leurs causes et conséquences.
- Élucider les caractérisations théoriques existantes des RSs, abordant notamment la non-identifiabilité des extracteurs de concepts.
- Répertorier et analyser les stratégies actuelles de mitigation et de sensibilisation aux RSs, en cartographiant leurs avantages et limites.
- Offrir une perspective unificatrice sur les RSs afin de faciliter l'entrée des chercheurs et praticiens dans la résolution de ce défi.

## Méthodologie
L'article adopte une approche de revue et de synthèse littéraire. Il reformule des concepts avancés de l'IA neuro-symbolique et des "Reasoning Shortcuts" pour les rendre plus digestes. La méthodologie consiste à structurer la littérature existante, à présenter des cadres théoriques pour comprendre ce phénomène, et à détailler les méthodes de gestion des RSs déjà proposées, en identifiant leurs forces et faiblesses.

## Résultats clés
- La confirmation que les "Reasoning Shortcuts" représentent un défi majeur pour la fiabilité et la crédibilité des modèles NeSy, affectant l'interprétabilité et la robustesse hors distribution.
- L'établissement d'un cadre théorique qui caractérise les RSs, notamment via les problèmes de non-identifiabilité des extracteurs de concepts et de distributions de "remapping" de concepts.
- Une vue d'ensemble structurée des différentes approches pour aborder les RSs, incluant des stratégies de prévention, de détection et d'atténuation.
- La mise à disposition d'un document qui sert de point de départ pour les chercheurs et praticiens souhaitant comprendre et résoudre le problème des RSs dans l'IA neuro-symbolique.

## Pertinence SysCRED
Cet article est hautement pertinent pour SysCRED, car il aborde directement la question de la crédibilité et de la fiabilité des systèmes d'IA.
L'**IA neuro-symbolique** est présentée comme une voie prometteuse pour une IA fiable et digne de confiance, cherchant à intégrer des connaissances a priori pour garantir la conformité des prédictions. SysCRED s'intéresse à la robustesse des systèmes d'IA et à leur capacité à respecter des contraintes, ce qui est l'objectif même de NeSy.
Les "Reasoning Shortcuts" (RSs) menacent directement la **crédibilité** des systèmes NeSy en compromettant l'interprétabilité de leurs explications et leur performance dans des scénarios hors distribution. Pour SysCRED, des modèles dont les raisonnements sont "court-circuités" ne sont pas fiables, car ils peuvent donner l'illusion de la justesse sans réellement comprendre les concepts sous-jacents, rendant leurs décisions difficilement auditables ou dignes de confiance.
Bien que non directement mentionné, le "grounding" des symboles et des concepts est fondamental et peut être lié aux **ontologies**, qui fournissent une structure et une sémantique aux connaissances symboliques. Des RSs impliquent un "grounding" incorrect, ce qui met en péril l'alignement entre les représentations internes du modèle et la réalité conceptuelle modélisée, un défi majeur pour l'ingénierie des connaissances et les ontologies.
Enfin, la difficulté à détecter et prévenir les RSs, surtout sans supervision directe des concepts, renvoie à la problématique de la **bureaucratie algorithmique** et des "boîtes noires". Des systèmes qui fonctionnent sur des "raccourcis" cachés peuvent conduire à des décisions arbitraires ou incompréhensibles, défiant la transparence et la responsabilité algorithmique, des piliers fondamentaux pour les travaux de SysCRED sur la confiance et l'éthique dans l'IA.

*(Généré par Gemini 2.5)*

