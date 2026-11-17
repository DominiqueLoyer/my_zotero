---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, dic9411, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Prabhakaran2019'
---

# Prabhakaran2019
- **Titre:** Perturbation Sensitivity Analysis to Detect Unintended Model Biases
- **Auteurs:** Prabhakaran, Vinodkumar and Hutchinson, Ben and Mitchell, Margaret
- **Année:** 2019
- **PDF:** ![[Prabhakaran_2019_Perturbation_Sensitivity_Analysis.pdf]]
- **DOI:** 

---
## Abstract
Les techniques de traitement du langage naturel (TLN) basées sur les données sont susceptibles d'apprendre des associations fortuites liées à des entités nommées et à leurs contextes sociaux, en plus du sens linguistique général. Idéalement, un système TLN évaluant le sentiment ou la toxicité devrait produire des scores indépendants de l'identité de ces entités. Les auteurs proposent l'Analyse de Sensibilité par Perturbation, un cadre d'évaluation générique pour détecter ces biais non intentionnels sans nécessiter de nouvelles annotations ou corpus.

## Contribution principale
- Proposition d'un cadre d'évaluation générique : l'Analyse de Sensibilité par Perturbation.
- Détection des biais de modèle non intentionnels liés aux entités nommées dans les systèmes NLP.
- La méthode ne nécessite pas de nouvelles annotations ou de corpus spécifiques.

## Méthodologie
La méthodologie, nommée Analyse de Sensibilité par Perturbation, évalue les modèles NLP en substituant des entités nommées dans des phrases (par exemple, remplacer "Katy Perry" par "Taylor Swift" dans "I hate X") et en observant la variation des scores de sortie du modèle (comme le sentiment ou la toxicité). Cette approche vise à déterminer si les scores restent indépendants de l'identité de l'entité mentionnée, sans recourir à des annotations manuelles ou à la création de nouveaux corpus.

## Résultats clés
- La méthode a été démontrée sur des modèles de sentiment et de toxicité appliqués à des commentaires en ligne en anglais.
- Les modèles NLP testés ont montré une sensibilité notable aux entités nommées : des phrases structurellement identiques (ex: "I hate Justin Timberlake." vs "I hate Katy Perry.") ont produit des scores de toxicité et de sentiment significativement différents.
- Ces variations confirment la présence de biais non intentionnels dans les modèles, qui associent des significations incidentes aux entités spécifiques.

## Pertinence SysCRED
La détection des biais non intentionnels par l'Analyse de Sensibilité par Perturbation est fondamentale pour la **crédibilité** des systèmes d'IA. Un modèle NLP qui produit des scores fluctuants pour des énoncés sémantiquement équivalents, simplement en fonction de l'entité nommée, manque de fiabilité et d'équité, minant ainsi la confiance des utilisateurs. Pour l'**IA neuro-symbolique**, cette analyse met en lumière la nécessité d'intégrer des connaissances symboliques (comme des ontologies d'entités ou des règles de généralisation) pour tempérer les associations statistiques apprises. Les **ontologies** pourraient structurer les entités nommées et leurs relations, permettant aux modèles de raisonner sur des catégories d'entités plutôt que sur des occurrences spécifiques biaisées, et ainsi garantir que les évaluations de sentiment ou de toxicité sont plus robustes et cohérentes, renforçant la crédibilité globale du système.

*(Généré par Gemini)*

