---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, dic9411, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Garg2019'
---

# Garg2019
- **Titre:** Counterfactual Fairness in Text Classification through Robustness
- **Auteurs:** Garg, Sahaj and Perot, Vincent and Limtiaco, Nicole and Taly, Ankur and D'Amour, Alexander and Hooker, Steve
- **Année:** 2019
- **PDF:** ![[Garg_2019_Counterfactual_Fairness_in.pdf]]
- **DOI:** 10.1145/3306618.3314246

---
## Abstract
Cet article aborde la question de la fairness contrefactuelle en classification de texte, qui examine comment une prédiction changerait si un attribut sensible référencé dans un exemple était différent. Les auteurs proposent une métrique, la fairness contrefactuelle de token (CTF), pour mesurer cette forme spécifique de fairness et introduisent trois approches (blindness, augmentation contrefactuelle et appariement logit contrefactuel - CLP) pour l'optimiser. Ils visent à garantir que les modèles ne traitent pas des phrases presque identiques différemment en fonction d'attributs sensibles.

## Contribution principale
- Étude de la fairness contrefactuelle en classification de texte, définie comme l'analyse du changement de prédiction en cas de modification d'un attribut sensible.
- Introduction de la métrique `Counterfactual Token Fairness (CTF)` pour mesurer cette forme de fairness.
- Proposition de trois méthodes d'optimisation de la CTF durant l'entraînement : `blindness`, `counterfactual augmentation` et `counterfactual logit pairing (CLP)`.
- Établissement d'un pont entre la littérature sur la robustesse et celle sur la fairness.

## Méthodologie
La méthodologie repose sur la génération de paires contrefactuelles par substitution de tokens associés à des groupes d'identité sensibles (ex: "gay" par "straight"). Ces paires sont utilisées pour définir la métrique de fairness contrefactuelle de token (CTF). Pour optimiser cette métrique, trois approches sont explorées : la "blindness" (rendre le modèle aveugle aux attributs sensibles), l'augmentation de données par des exemples contrefactuels, et l'appariement logit contrefactuel (CLP) qui ajuste les logits des paires contrefactuelles durant l'entraînement.

## Résultats clés
- Les méthodes "blindness" et "counterfactual logit pairing (CLP)" sont efficaces pour améliorer la fairness contrefactuelle de token.
- Les approches proposées ne dégradent pas les performances du classifieur.
- Il existe des compromis variables entre les méthodes et la fairness de groupe.

## Pertinence SysCRED
- **Crédibilité:** La recherche renforce la crédibilité des systèmes d'IA en garantissant que les prédictions ne sont pas biaisées par des attributs sensibles. Un modèle juste et stable face aux variations contrefactuelles est intrinsèquement plus digne de confiance, car il évite les décisions arbitraires qui mineraient la crédibilité des systèmes d'IA dans des applications critiques.
- **Ontologies:** Bien que non explicitement employées, l'identification et la catégorisation des "tokens d'identité" et des "attributs sensibles" pour générer des contrefactuels pourraient être formalisées par des ontologies. Ces structures sémantiques pourraient définir les relations entre les identités et les stéréotypes, permettant une génération plus systématique et éthiquement fondée des paires contrefactuelles.
- **IA neuro-symbolique:** L'intégration de contraintes de fairness symboliques (comme l'exigence d'une prédiction similaire pour des paires contrefactuelles) dans l'entraînement de modèles neuronaux (par exemple, via CLP) représente une forme d'IA neuro-symbolique. Elle cherche à infuser un raisonnement de haut niveau (règles de fairness) dans des systèmes d'apprentissage sub-symboliques, guidant leur comportement vers des objectifs éthiques prédéfinis.

*(Généré par Gemini)*

