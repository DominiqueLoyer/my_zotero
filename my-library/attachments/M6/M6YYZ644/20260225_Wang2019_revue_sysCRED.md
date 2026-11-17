---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Wang2019'
---
# Wang2019
- **Titre:** Neural Graph Collaborative Filtering
- **Auteurs:** Wang, Xiang and He, Xiangnan and Wang, Meng and Feng, Fuli and Chua, Tat-Seng
- **Année:** 2019
- **DOI:** 10.1145/3331184.3331267
- **PDF:** ![[Wang_2019_Neural_Graph_Collaborative.pdf]]

---
## Abstract
L'article aborde un défi fondamental dans les systèmes de recommandation modernes : l'apprentissage de représentations vectorielles (embeddings) pour les utilisateurs et les items. Les méthodes existantes, de la factorisation de matrices au deep learning, obtiennent généralement ces embeddings à partir de caractéristiques préexistantes (ID, attributs), mais ne parviennent pas à intégrer explicitement le "signal collaboratif" latent dans les interactions utilisateur-item. Les auteurs proposent une nouvelle approche, le Neural Graph Collaborative Filtering (NGCF), qui intègre la structure de graphe bipartite utilisateur-item directement dans le processus d'embedding. NGCF propage les embeddings sur ce graphe, modélisant de manière expressive la connectivité d'ordre supérieur et injectant explicitement le signal collaboratif.

## Contribution principale
La contribution principale est la proposition du framework NGCF, qui résout le problème de l'encodage implicite du signal collaboratif dans les méthodes d'embedding existantes pour les systèmes de recommandation. En exploitant la structure de graphe bipartite utilisateur-item et en propageant les embeddings sur celui-ci, NGCF parvient à modéliser explicitement la connectivité d'ordre supérieur et à injecter le signal collaboratif de manière plus efficace, conduisant à des représentations utilisateur et item plus informatives.

## Méthodologie
Les auteurs développent le framework Neural Graph Collaborative Filtering (NGCF). La méthodologie clé repose sur l'intégration directe des interactions utilisateur-item, sous la forme d'un graphe bipartite, dans le processus d'apprentissage des embeddings. Plus précisément, NGCF exploite la structure de ce graphe en propageant les embeddings des utilisateurs et des items à travers leurs connexions. Cette propagation permet de capturer et de modéliser la connectivité d'ordre supérieur au sein du graphe, injectant ainsi explicitement le signal collaboratif dans les représentations apprises.

## Résultats clés
Les expériences menées sur trois benchmarks publics démontrent des améliorations significatives de NGCF par rapport à plusieurs modèles de pointe, incluant HOPRec et Collaborative Memory Network. Une analyse approfondie confirme l'importance de la propagation des embeddings pour apprendre de meilleures représentations utilisateur et item, justifiant la rationalité et l'efficacité de NGCF.

## Pertinence SysCRED
Pour SysCRED, ce travail est hautement pertinent car il aborde l'amélioration fondamentale des systèmes de recommandation, qui sont des composants cruciaux dans de nombreux systèmes intelligents de prise de décision, notamment en commerce électronique, publicité et médias sociaux. La capacité de NGCF à générer des recommandations plus précises via une meilleure modélisation des interactions utilisateur-item, en intégrant explicitement le signal collaboratif et la connectivité d'ordre supérieur à travers les Graphes Neuronaux, a des implications directes pour l'optimisation des décisions basées sur les données. SysCRED s'intéresse aux systèmes complexes et à l'intelligence artificielle pour la prise de décision, et NGCF offre une avancée méthodologique significative dans la modélisation des préférences et comportements des utilisateurs, ce qui est essentiel pour des applications allant de la personnalisation des services à l'évaluation du risque ou à la détection de fraude, des domaines d'intérêt pour le laboratoire.

*(Généré par Gemini)*

