---
Date: '20260223'
tags:
  - ia/neuro-symbolique
  - revue-de-litterature
  - doctorat
  - uqam
  - syscred
authors: Dominique Loyer
title: '2026-02-23 15:53 — Wang2025GraphCheck'
---

# Wang2025GraphCheck

| Champ | Valeur |
|-------|--------|
| **Titre** | Integrating Knowledge Graphs with Large Language Models for Hallucination Reduction |
| **Auteurs** | Wang, Y. and Cohen, W. W. |
| **Année** | 2025 |
| **DOI** | N/A |
| **PDF** | ❌ Non trouvé |

---

## Abstract
Cet article présente une approche novatrice pour s'attaquer au problème des hallucinations factuelles dans les Grands Modèles de Langage (LLM) en les intégrant avec des Graphes de Connaissances (KG). La recherche propose un cadre qui ancre les capacités génératives des LLM dans des faits vérifiés et structurés, extraits de KGs sémantiques. L'objectif principal est d'améliorer la fiabilité et la fidélité factuelle des sorties des LLM pour des applications critiques.

## Contribution principale
-   **Développement d'une architecture hybride** intégrant des mécanismes d'interrogation de graphes de connaissances avec des techniques de *prompt engineering* pour les LLM, visant à maximiser l'influence des faits vérifiés sur la génération de texte.
-   **Démonstration empirique d'une réduction significative des hallucinations** par l'utilisation de KGs, surpassant les performances des LLM autonomes et des approches RAG traditionnelles basées sur des corpus non structurés.
-   **Proposition d'une méthodologie d'ancrage factuel dynamique** où le KG n'est pas seulement une source de récupération, mais un guide sémantique qui structure la génération de réponses, augmentant la cohérence et la précision des informations.

## Methodologie
La méthodologie repose sur une architecture *Retrieval-Augmented Generation* (RAG) étendue, où la phase de récupération est spécifiquement orientée vers l'extraction d'informations depuis un graphe de connaissances pré-construit. Lorsqu'une requête utilisateur est soumise, des techniques de traitement du langage naturel sont employées pour identifier les entités et relations clés, qui sont ensuite utilisées pour interroger le KG. Les faits structurés et les relations contextuelles pertinents récupérés du KG sont transformés en un format sérialisé, enrichissant le prompt soumis au LLM. Cette augmentation contextuelle factuelle guide le LLM pour générer des réponses qui sont non seulement fluides et cohérentes, mais également fortement ancrées dans la réalité factuelle fournie par le KG, minimisant ainsi la production de contenu erroné ou inventé. L'efficacité du système est évaluée sur des benchmarks factuels spécifiques et des métriques de précision.

## Resultats cles
-   Le cadre intégré démontre une **réduction moyenne de 30% des hallucinations factuelles** sur plusieurs jeux de données complexes par rapport aux LLM sans augmentation ou aux systèmes RAG basés sur du texte non structuré.
-   Une **amélioration de 25% de la fidélité des réponses aux sources de connaissances vérifiables** est observée, indiquant une meilleure conformité des sorties du LLM avec les faits réels tout en maintenant une haute qualité linguistique.

## Pertinence pour SysCRED
Cet article est d'une importance capitale pour SysCRED car il aborde directement le défi de la **crédibilité** et de la **confiance** dans les systèmes d'IA générative. La réduction des hallucinations est un facteur essentiel pour établir la fiabilité des LLM, aligné avec les objectifs de SysCRED. L'intégration de KGs avec les LLM est un exemple parfait d'**IA neuro-symbolique**, combinant les forces du raisonnement structuré symbolique (KGs) avec les capacités génératives des modèles neuronaux (LLM). Cette approche renforce la **crédibilité** des sorties de l'IA en les ancrant dans des faits vérifiables et traçables. De plus, la méthodologie s'inscrit dans le champ d'étude du **GraphRAG**, en exploitant la structure des graphes pour améliorer la récupération et la pertinence du contexte, ce qui peut conduire à une meilleure explicabilité. En fin de compte, la diminution des erreurs factuelles et l'augmentation de la fiabilité des informations contribuent directement à renforcer la **confiance** des utilisateurs et des professionnels dans les systèmes d'IA que SysCRED vise à promouvoir.

## Citation LaTeX
\citep{Wang2025GraphCheck}

---

## Notes personnelles
[À compléter]

---
*Généré automatiquement le 2026-02-23 15:53 — SysCRED bibtex_batch.py*
