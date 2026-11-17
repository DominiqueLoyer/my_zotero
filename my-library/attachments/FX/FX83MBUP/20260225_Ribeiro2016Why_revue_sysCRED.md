---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Ribeiro2016Why'
---
# Ribeiro2016Why
- **Titre:** Why Should I Trust You?": Explaining the Predictions of Any Classifier
- **Auteurs:** Ribeiro, Marco Tulio and Singh, Sameer and Guestrin, Carlos
- **Année:** 2016
- **DOI:** 10.18653/v1/n16-3020
- **PDF:** ![[Ribeiro_2016_Why_Should_I.pdf]]

---
## Abstract
L'article aborde le problème du manque de confiance des utilisateurs envers les modèles d'apprentissage automatique, en particulier les réseaux neuronaux "boîte noire", qui rend leur adoption difficile. Il distingue deux types de confiance : (1) la confiance en une prédiction individuelle pour agir, et (2) la confiance en un modèle pour un déploiement "sur le terrain". Pour résoudre ce problème, les auteurs décrivent LIME (Local Interpretable Model-agnostic Explanations), une technique d'explication novatrice, interprétable et fidèle, capable d'expliquer les prédictions de *n'importe quel* classifieur. Ils proposent également une méthode pour expliquer les modèles en présentant des prédictions individuelles représentatives et leurs explications de manière non redondante.

## Contribution principale
La contribution principale est le développement de LIME, une technique d'explication "agnostique au modèle" (model-agnostic) capable de fournir des explications locales, interprétables et fidèles pour les prédictions de n'importe quel classifieur. LIME permet aux utilisateurs de comprendre *pourquoi* une prédiction spécifique a été faite en identifiant les portions pertinentes de l'entrée, favorisant ainsi la confiance dans les systèmes d'IA, y compris les modèles complexes comme les réseaux neuronaux. L'article met également en lumière l'importance de différencier les définitions de la confiance (confiance en une prédiction vs. confiance en un modèle entier) et la faiblesse des métriques d'exactitude seules pour évaluer cette confiance.

## Méthodologie
La méthodologie repose sur le développement de LIME, une technique qui génère des explications locales. Bien que l'extrait ne détaille pas l'algorithme interne de LIME, il indique qu'elle explique les prédictions en identifiant des portions utiles de l'entrée. LIME est conçue pour être interprétable et fidèle à la prédiction du modèle sous-jacent. La validité de ces idées est démontrée sur diverses tâches de traitement du langage naturel (NLP) telles que la classification de documents, la détection de politesse et l'analyse de sentiment. Les classifieurs testés incluent des réseaux neuronaux et des machines à vecteurs de support (SVMs). L'interaction utilisateur inclut la fourniture d'explications de texte libre, la comparaison de classifieurs et l'ingénierie de fonctionnalités.

## Résultats clés
Les résultats clés démontrés par l'article sont :
1.  **Exploration universelle** : LIME peut expliquer les prédictions de *tout* classifieur, quelle que soit sa complexité ou son architecture (ex: réseaux neuronaux, SVMs).
2.  **Explications interprétables et fidèles** : La technique génère des explications qui sont à la fois compréhensibles par les humains et représentatives du comportement du modèle sous-jacent.
3.  **Applicabilité étendue** : LIME est efficace dans diverses tâches NLP (classification de documents, détection de politesse, analyse de sentiment).
4.  **Amélioration de la confiance et de l'acceptation** : Les explications sont essentielles pour évaluer la confiance, prendre des décisions basées sur les prédictions et choisir de déployer ou non un nouveau modèle, et il a été observé qu'elles augmentent l'acceptation des systèmes automatisés.
5.  **Dépassement des limites de l'exactitude** : Le papier souligne que l'exactitude sur des données de validation ne suffit pas et peut être trompeuse, et que les explications aident à combler l'écart avec les métriques d'intérêt réelles (ex: engagement utilisateur).

## Pertinence SysCRED
Pour SysCRED (System Security and Credibility Research Group), cet article est d'une grande pertinence pour plusieurs raisons :
1.  **Confiance et crédibilité des systèmes d'IA** : Le thème central de l'article — l'établissement de la confiance dans les prédictions et les modèles d'IA — est directement lié aux missions de SysCRED concernant la crédibilité des systèmes. Comprendre et justifier les décisions de l'IA est fondamental pour qu'un système soit jugé crédible.
2.  **Explicabilité de l'IA (XAI)** : LIME est une technique fondatrice et largement adoptée dans le domaine de l'IA explicable. La capacité à "ouvrir" les "boîtes noires" est cruciale pour la sécurité, l'auditabilité et la conformité des systèmes d'IA dans des contextes critiques (par exemple, financier, médical, militaire).
3.  **Identification des vulnérabilités et biais** : En expliquant *pourquoi* un modèle fait une prédiction, LIME peut potentiellement aider à identifier des dépendances à des caractéristiques non pertinentes ou biaisées, des "fuites de données" (data leakage) ou d'autres vulnérabilités qui pourraient être exploitées ou miner la crédibilité du système.
4.  **Adoption et déploiement sécurisé** : La différenciation entre la confiance en une prédiction et la confiance en un modèle "in the wild" résonne avec les défis de déploiement de systèmes sécurisés et fiables dans des environnements réels. Les explications peuvent faciliter l'adoption de l'IA en renforçant la confiance des utilisateurs et des régulateurs.
5.  **Ingénierie de la sécurité et robustesse** : La capacité des utilisateurs à effectuer de l'ingénierie de fonctionnalités basée sur des explications suggère un potentiel pour améliorer la robustesse et l'équité des modèles, des aspects essentiels pour la sécurité et la crédibilité des systèmes.

*(Généré par Gemini)*

