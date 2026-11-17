---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Ying2018'
---
# Ying2018
- **Titre:** Graph Convolutional Neural Networks for Web-Scale Recommender Systems
- **Auteurs:** Ying, Rex and He, Ruining and Chen, Kaifeng and Eksombatchai, Pong and Hamilton, William L. and Leskovec, Jure
- **Année:** 2018
- **DOI:** 10.1145/3219819.3219890
- **PDF:** ![[Ying_2018_Graph_Convolutional_Neural.pdf]]

---
## Abstract
Recent advancements in deep neural networks for graph-structured data have shown state-of-the-art performance on recommender system benchmarks. However, scaling these methods to web-scale recommendation tasks with billions of items and hundreds of millions of users remains a challenge. This paper describes PinSage, a large-scale deep recommendation engine developed and deployed at Pinterest. PinSage is a data-efficient Graph Convolutional Network (GCN) algorithm that combines efficient random walks and graph convolutions to generate node embeddings (items) incorporating both graph structure and node feature information. Compared to prior GCN approaches, PinSage introduces a novel method based on highly efficient random walks to structure convolutions and a novel training strategy using progressively harder examples to improve robustness and convergence. Deployed at Pinterest, PinSage was trained on 7.5 billion examples on a graph with 3 billion nodes (pins and boards) and 18 billion edges. Offline metrics, user studies, and A/B tests show that PinSage generates higher-quality recommendations than comparable deep learning and graph-based alternatives. This work represents the largest application of deep graph embeddings to date, paving the way for a new generation of web-scale recommender systems based on graph convolutional architectures.

## Contribution principale
La contribution principale est le développement et le déploiement à grande échelle de PinSage, un algorithme de réseau de neurones convolutif sur graphe (GCN) spécifiquement conçu pour les systèmes de recommandation web-scale. PinSage introduit une approche innovante combinant des marches aléatoires efficaces et des convolutions sur graphe pour générer des plongements de nœuds (items) qui intègrent la structure du graphe et les caractéristiques des nœuds. L'article propose également une nouvelle méthode pour structurer les convolutions basée sur des marches aléatoires très efficaces, ainsi qu'une stratégie d'entraînement inédite utilisant des exemples de plus en plus difficiles pour améliorer la robustesse et la convergence du modèle. Il s'agit de la plus grande application de plongements de graphes profonds à ce jour, démontrant la faisabilité et la supériorité des architectures GCN pour des systèmes de recommandation massifs comme celui de Pinterest.

## Méthodologie
La méthodologie repose sur le développement de PinSage, un algorithme GCN qui résout les défis de scalabilité des méthodes GCN précédentes.
1.  **Architecture GCN sur mesure :** PinSage combine des marches aléatoires efficaces et des opérations de convolution sur graphe pour générer des plongements (embeddings) de nœuds. Ces plongements intègrent à la fois la structure du graphe et les informations de caractéristiques des nœuds (items).
2.  **Nouvelle structuration des convolutions :** Une méthode innovante est introduite, s'appuyant sur des marches aléatoires très efficaces pour échantillonner et structurer les voisins des nœuds lors des opérations de convolution, rendant le processus plus efficient pour les graphes à grande échelle.
3.  **Stratégie d'entraînement adaptative :** Une stratégie d'entraînement progressive est conçue, utilisant des exemples d'entraînement de difficulté croissante ("harder-and-harder training examples"). Cette approche vise à améliorer la robustesse du modèle et à accélérer sa convergence.
4.  **Déploiement et échelle :** Le modèle a été déployé chez Pinterest et entraîné sur des données massives : 7,5 milliards d'exemples sur un graphe composé de 3 milliards de nœuds (représentant des "pins" et des "boards") et 18 milliards d'arêtes.

## Résultats clés
*   **Qualité des recommandations supérieure :** PinSage génère des recommandations de meilleure qualité que les alternatives comparables basées sur l'apprentissage profond et les graphes, comme l'attestent les métriques hors ligne, les études utilisateurs et les tests A/B.
*   **Scalabilité et déploiement réel :** Le modèle a été déployé avec succès chez Pinterest, démontrant sa capacité à opérer à l'échelle du web sur des graphes massifs (3 milliards de nœuds, 18 milliards d'arêtes).
*   **Plus grande application de plongements de graphes profonds :** Au moment de la publication, cette étude représente la plus grande application de plongements de graphes profonds jamais réalisée, ouvrant la voie à une nouvelle génération de systèmes de recommandation web-scale.

## Pertinence SysCRED
Pour SysCRED, ce papier est d'une grande pertinence pour plusieurs raisons :
1.  **Systèmes de recommandation à grande échelle :** L'article aborde directement la conception et l'implémentation de systèmes de recommandation pour des environnements web-scale, un domaine clé pour la recherche appliquée en IA.
2.  **Apprentissage profond sur graphes (GNNs) :** La recherche explore l'utilisation des GCNs, une famille de modèles d'apprentissage profond de plus en plus influente pour les données structurées en graphes, qui sont omniprésentes dans les interactions utilisateur-item.
3.  **Scalabilité et efficience :** Les innovations de PinSage en matière de marches aléatoires efficaces et de stratégies d'entraînement pour la robustesse sont cruciales pour adresser les défis de scalabilité et d'efficience des modèles d'IA en production, un aspect souvent négligé dans la recherche théorique.
4.  **Applications réelles et validation :** Le déploiement réussi chez Pinterest et la validation par des tests A/B en conditions réelles fournissent une preuve concrète de l'impact des GNNs dans des systèmes critiques, offrant des cas d'études précieux.
5.  **Nouvelles directions de recherche :** Le papier "ouvre la voie à une nouvelle génération de systèmes de recommandation" basés sur des architectures GCN, suggérant de nombreuses avenues de recherche pour SysCRED, notamment sur l'amélioration des GNNs pour l'échelle, la robustesse, et l'intégration de divers types de données.

*(Généré par Gemini)*

