---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, dic9411, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Barzilay2008'
---

# Barzilay2008
- **Titre:** Modeling Local Coherence: An Entity-Based Approach
- **Auteurs:** Barzilay, Regina and Lapata, Mirella
- **Année:** 2008
- **PDF:** ![[Barzilay_2008_Modeling_Local_Coherence.pdf]]
- **DOI:** 10.1162/coli.2008.34.1.1

---
## Abstract
Cet article propose un nouveau cadre pour représenter et mesurer la cohérence locale du discours, introduisant la représentation "entity-grid" qui capture les schémas de distribution des entités. L'approche re-conceptualise l'évaluation de la cohérence comme une tâche d'apprentissage, permettant de déduire les propriétés des textes cohérents à partir d'un corpus sans annotation manuelle. L'algorithme abstrait un texte en séquences de transitions d'entités, enregistrant des informations distributionnelles, syntaxiques et référentielles.

## Contribution principale
- Introduction d'un cadre novateur pour la représentation et la mesure de la cohérence locale via la grille d'entités ("entity-grid").
- Proposition d'un algorithme automatisé pour abstraire un texte en séquences de transitions d'entités, capturant des informations distributionnelles, syntaxiques et référentielles.
- Re-conceptualisation de l'évaluation de la cohérence comme une tâche d'apprentissage, permettant d'apprendre les propriétés des textes cohérents à partir d'un corpus sans annotation manuelle ni base de connaissances prédéfinie.
- Démonstration de l'efficacité de la représentation pour des tâches de génération et de classification de texte basées sur le classement.

## Méthodologie
L'approche est centrée sur la représentation "entity-grid" du discours, qui modélise les schémas de distribution des entités. Un algorithme est introduit pour abstraire automatiquement un texte en un ensemble de séquences de transitions d'entités, enregistrant des informations distributionnelles, syntaxiques et référentielles sur ces entités. L'évaluation de la cohérence est ensuite formulée comme une tâche d'apprentissage, où les propriétés des textes cohérents sont apprises à partir d'un corpus.

## Résultats clés
- Bonne performance obtenue sur les tâches de réordonnancement de texte ("text ordering").
- Évaluation automatique efficace de la cohérence de résumés ("summary coherence evaluation").
- Application réussie à l'évaluation de la lisibilité ("readability assessment").

## Pertinence SysCRED
Ce travail est pertinent pour SysCRED en Informatique cognitive car il propose une méthode robuste pour modéliser la cohérence textuelle, un facteur clé pour la crédibilité de l'information. L'approche "entity-based" et son cadre d'apprentissage relient la représentation symbolique (entités, transitions) à l'apprentissage statistique, ce qui est fondamental pour l'IA neuro-symbolique. La capacité d'apprendre des propriétés de cohérence à partir de corpus, sans annotation manuelle, pourrait être utilisée pour développer des ontologies dynamiques de la structure du discours ou pour évaluer la crédibilité de documents en analysant leur cohérence intrinsèque, signalant les textes potentiellement peu fiables ou générés de manière artificielle par leur manque de fluidité locale.

*(Généré par Gemini)*

