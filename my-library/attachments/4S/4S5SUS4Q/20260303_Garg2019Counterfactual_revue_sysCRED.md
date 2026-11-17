---
Date: '20260303'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-03-03 - Garg2019Counterfactual'
---
# Garg2019Counterfactual
- **Titre:** Counterfactual Fairness in Text Classification through Robustness
- **Auteurs:** Garg, Sahaj and Perot, Vincent and Limtiaco, Nicole and Taly, Ankur and D'Amour, Alexander and Hooker, Steve
- **Année:** 2019
- **DOI:** 10.1145/3306618.3317950
- **PDF:** ![[Garg_2019_Counterfactual_Fairness_in.pdf]]

---
## Abstract
L'article "Counterfactual Fairness in Text Classification through Robustness" étudie la fairness contre-factuelle dans la classification de texte, en se demandant comment la prédiction changerait si l'attribut sensible référencé dans l'exemple était différent. Les auteurs proposent une métrique, la fairness contre-factuelle des tokens (CTF), pour mesurer cette forme de fairness dans les classifieurs de texte.

## Contribution principale
La contribution principale de cet article est l'introduction de la métrique CTF et de trois approches pour optimiser la fairness contre-factuelle des tokens pendant l'entraînement : la cécité, l'augmentation contre-factuelle et l'appariement des logits contre-factuels (CLP). Ces approches visent à réduire les biais dans les classifieurs de texte sans nuire à leur performance.

## Méthodologie
La méthodologie utilisée dans cet article consiste à générer des contre-faits en substituant des tokens associés à des groupes d'identité, tels que "gay" avec "straight" ou "Asiatique" avec "Américain". Les auteurs utilisent ensuite ces contre-faits pour définir la métrique CTF et évaluer les performances des trois approches proposées.

## Résultats clés
Les résultats clés de cet article sont que les approches de cécité et de CLP améliorent la fairness contre-factuelle des tokens sans nuire à la performance des classifieurs. Les auteurs constatent également que ces approches ont des compromis variables avec la fairness de groupe.

## Pertinence SysCRED
La pertinence de cet article pour le SysCRED est qu'il aborde les questions de fairness et de biais dans les systèmes de classification de texte, qui sont des enjeux importants pour la recherche en systèmes de recommandation et en apprentissage automatique. Les résultats de cet article pourraient être appliqués pour améliorer la fairness et la transparence des systèmes de recommandation et de classification de texte utilisés dans divers domaines, tels que la santé, la finance et les médias sociaux.

*(Généré par Groq)*

