---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, dic9411, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Baly2020'
---

# Baly2020
- **Titre:** We Can Detect Your Bias: Predicting the Political Ideology of News Articles
- **Auteurs:** Baly, Ramy and Da San Martino, Giovanni and Glass, James and Nakov, Preslav
- **Année:** 2020
- **PDF:** ![[Baly_2020_We_Can_Detect.pdf]]
- **DOI:** 10.18653/v1/2020.emnlp-main.552

---
## Abstract
Cet article explore la tâche de prédire l'idéologie politique (gauche, centre, droite) d'articles de presse individuels. Pour ce faire, les auteurs ont créé et publié un grand ensemble de données de 34 737 articles annotés manuellement, et ont mis en place un cadre expérimental exigeant où les médias de test n'étaient pas vus pendant l'entraînement. Ils proposent des méthodes de modélisation innovantes, notamment une adaptation média adversarielle et une "triplet loss" adaptée, démontrant des améliorations significatives par rapport aux Transformers de l'état de l'art.

## Contribution principale
-   Création et publication d'un grand dataset (34 737 articles) annoté manuellement pour l'idéologie politique (gauche, centre, droite), équilibré en sujets et médias.
-   Mise en place d'un protocole expérimental unique où les médias de test sont exclus de l'entraînement, garantissant que le modèle apprend le biais et non la source.
-   Proposition de nouvelles approches de modélisation, incluant une adaptation média adversarielle et une "triplet loss" spécialement adaptée.
-   Démonstration de l'efficacité de l'intégration d'informations de fond sur la source pour améliorer la prédiction au niveau de l'article.
-   Concentration sur la détection du biais au niveau de l'article, un axe de recherche peu exploré par rapport aux travaux sur le biais des médias globaux.

## Méthodologie
Les auteurs ont compilé un ensemble de données de 34 737 articles de presse, chacun étiqueté manuellement selon son idéologie politique dominante (gauche, centre, ou droite). Pour s'assurer que le modèle généralise au-delà des sources connues, l'évaluation a été réalisée en utilisant des articles provenant de médias non inclus dans l'ensemble d'entraînement. Du point de vue de la modélisation, ils ont développé une méthode d'adaptation adversarielle des médias et une "triplet loss" personnalisée, tout en intégrant des informations contextuelles sur la source de l'article pour enrichir le processus de prédiction.

## Résultats clés
-   Des améliorations "très significatives" (sizable improvements) ont été obtenues par rapport aux modèles Transformers pré-entraînés de l'état de l'art dans le cadre expérimental difficile.
-   L'ajout d'informations de fond sur la source de l'article s'est avéré très utile pour améliorer la précision de la prédiction du biais au niveau de l'article.

## Pertinence SysCRED
Cet article s'aligne directement avec la mission de SysCRED en abordant la détection du biais politique dans les articles de presse, un aspect fondamental de la **crédibilité** de l'information. En rendant le public conscient des biais médiatiques, il contribue à un débat public plus sain et à une meilleure prise de décision. Pour une approche **IA neuro-symbolique**, la tâche de reconnaître différentes formes de biais (omission, sur-rapport, sélection des faits, techniques de propagande) est un excellent candidat. Des modèles neuronaux (comme les Transformers utilisés ici) peuvent identifier des patrons linguistiques, tandis que des règles symboliques et des **ontologies** pourraient formaliser les connaissances sur les types de biais, les sujets sensibles, les affiliations des médias et les implications politiques des termes et concepts. Ces ontologies permettraient de structurer le "background information about the source" que les auteurs ont trouvé utile, en lui donnant un sens sémantique et en permettant une inférence plus robuste et explicable sur *pourquoi* un article est biaisé, plutôt que simplement *qu'il l'est*. Cela pourrait enrichir la compréhension des mécanismes de biais et la génération d'explications pour la détection.

*(Généré par Gemini)*

