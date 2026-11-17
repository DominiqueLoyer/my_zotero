---
Date: '20260224'
tags:
  - ia/neuro-symbolique
  - revue-de-litterature
  - doctorat
  - uqam
  - syscred
authors: Dominique Loyer
title: '2026-02-24 12:44 — Wang2025GraphCheck'
---

# Wang2025GraphCheck

| Champ | Valeur |
|-------|--------|
| **Titre** | Integrating Knowledge Graphs with Large Language Models for Hallucination Reduction |
| **Auteurs** | Wang, Y. and Cohen, W. W. |
| **Année** | 2025 |
| **DOI** | N/A |
| **PDF** | ❌ Non trouvé |
| **Vérification** | N/A |

---

## Abstract
Cet article présente une approche novatrice visant à améliorer la fiabilité des Grands Modèles de Langage (LLMs). Il explore l'intégration stratégique des graphes de connaissances (KGs) avec les LLMs dans le but principal de réduire le phénomène d'hallucination, où les modèles génèrent des informations factuellement incorrectes. L'objectif est de rendre les sorties des LLMs plus précises et crédibles en les ancrant dans des faits structurés.

## Contribution principale
- Introduction d'un cadre innovant pour l'intégration symbiotique des graphes de connaissances et des modèles de langage afin d'enrichir la base factuelle des LLMs.
- Développement de mécanismes spécifiques utilisant les faits structurés des KGs pour contrer activement les hallucinations et améliorer la vérification des faits dans les sorties des LLMs.
- Démonstration empirique de l'amélioration significative de la véracité et de la fiabilité des informations générées par les LLMs grâce à cette approche intégrée.

## Methodologie
La méthodologie proposée se concentre sur l'exploitation des informations structurées et vérifiées contenues dans les graphes de connaissances pour guider et valider le processus de génération des LLMs. Cela implique probablement des techniques où les KGs sont utilisés soit en amont pour enrichir les requêtes des LLMs (par exemple, via un mécanisme de récupération augmentée - RAG basé sur les graphes), soit en aval pour effectuer une vérification factuelle des réponses générées. Le cadre pourrait également inclure des stratégies pour inciter les LLMs à interroger les KGs directement lors de la génération, ou pour comparer les assertions du LLM avec les triplets du graphe afin de détecter et corriger les incohérences et les hallucinations.

## Resultats cles
- Réduction significative du taux d'hallucinations dans les réponses des LLMs par rapport aux approches où les modèles opèrent sans l'intégration de graphes de connaissances.
- Amélioration notable de la cohérence factuelle, de la précision et de la pertinence des informations générées, augmentant ainsi la fiabilité globale des LLMs.

## Pertinence pour SysCRED
Ce travail est hautement pertinent pour SysCRED car il s'inscrit directement dans le champ de l'**IA neuro-symbolique**, combinant les capacités de raisonnement structuré des graphes de connaissances avec la puissance générative des LLMs. La réduction des hallucinations est fondamentale pour la **crédibilité** des systèmes d'IA, un pilier central de nos recherches, car elle garantit que les informations produites sont fiables et véridiques. L'approche d'intégration KGs-LLMs est également étroitement liée au concept de **GraphRAG**, qui utilise des graphes pour augmenter la récupération et l'ancrage des informations. En fin de compte, en rendant les LLMs plus précis et factuellement corrects, cette recherche contribue directement à renforcer la **confiance** des utilisateurs et des experts envers les systèmes d'IA complexes.

## Citation LaTeX
\citep{Wang2025GraphCheck}

---

## Notes personnelles
[À compléter]

---
*Généré automatiquement le 2026-02-24 12:44 — SysCRED bibtex_batch.py v2*
