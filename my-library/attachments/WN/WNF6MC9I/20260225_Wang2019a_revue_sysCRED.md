---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Wang2019a'
---
# Wang2019a
- **Titre:** Knowledge-aware Graph Neural Networks with Label Smoothness Regularization for Recommender Systems
- **Auteurs:** Wang, Hongwei and Zhang, Fuzheng and Wang, Jialin and Zhao, Miao and Li, Wenjie and Wang, Xing and Xie, Xing
- **Année:** 2019
- **DOI:** 10.1145/3292500.3330836
- **PDF:** ![[Wang_2019_Knowledge_aware_Graph.pdf]]

---
## Abstract
Knowledge graphs capture structured information and relations between a set of entities or items. As such knowledge graphs represent an attractive source of information that could help improve recommender systems. However, existing approaches in this domain rely on manual feature engineering and do not allow for an end-to-end training. Here we propose Knowledge-aware Graph Neural Networks with Label Smoothness regularization (KGNN-LS) to provide better recommendations. Conceptually, our approach computes user-specific item embeddings by first applying a trainable function that identifies important knowledge graph relationships for a given user. This way we transform the knowledge graph into a user-specific weighted graph and then apply a graph neural network to compute personalized item embeddings. To provide better inductive bias, we rely on label smoothness assumption, which posits that adjacent items in the knowledge graph are likely to have similar user relevance labels/scores. Label smoothness provides regularization over the edge weights and we prove that it is equivalent to a label propagation scheme on a graph. We also develop an efficient implementation that shows strong scalability with respect to the knowledge graph size. Experiments on four datasets show that our method outperforms state of the art baselines. KGNN-LS also achieves strong performance in cold-start scenarios where user-item interactions are sparse.

## Contribution principale
Les auteurs proposent les **Knowledge-aware Graph Neural Networks with Label Smoothness regularization (KGNN-LS)**, une nouvelle approche pour les systèmes de recommandation. Cette méthode vise à fournir de meilleures recommandations en surmontant les limitations des approches existantes (ingénierie manuelle de caractéristiques et absence d'entraînement de bout en bout). La contribution clé réside dans la capacité à calculer des embeddings d'items spécifiques à l'utilisateur en transformant le graphe de connaissances (KG) en un graphe pondéré spécifique à l'utilisateur, grâce à une fonction entraînable qui identifie les relations importantes du KG. De plus, ils introduisent une régularisation de la "douceur des labels" (label smoothness) qui suppose que les items adjacents dans le KG ont des scores de pertinence utilisateur similaires, et prouvent son équivalence à un schéma de propagation de labels.

## Méthodologie
La méthode KGNN-LS utilise une approche en plusieurs étapes :
1.  **Identification personnalisée des relations :** Une fonction entraînable est appliquée pour identifier les relations les plus importantes au sein du graphe de connaissances pour un utilisateur spécifique.
2.  **Transformation en graphe pondéré utilisateur-spécifique :** Le graphe de connaissances est transformé en un graphe pondéré où les poids des arêtes sont personnalisés pour chaque utilisateur, reflétant la pertinence de ces relations.
3.  **Calcul d'embeddings avec GNN :** Un réseau de neurones sur graphe (GNN) est ensuite appliqué sur ce graphe pondéré spécifique à l'utilisateur pour calculer des embeddings d'items personnalisés.
4.  **Régularisation par douceur des labels :** Une hypothèse de douceur des labels est introduite, postulant que les items adjacents dans le graphe de connaissances sont susceptibles d'avoir des scores de pertinence utilisateur similaires. Cette hypothèse fournit une régularisation sur les poids des arêtes et est prouvée équivalente à un schéma de propagation de labels sur un graphe.
5.  **Optimisation de l'implémentation :** Une implémentation efficace est développée pour garantir une forte scalabilité du modèle, même avec des graphes de connaissances de grande taille.

## Résultats clés
*   La méthode KGNN-LS surpasse les méthodes de référence (state-of-the-art baselines) lors d'expériences menées sur quatre jeux de données distincts.
*   Le modèle KGNN-LS démontre également des performances robustes et solides dans les scénarios de démarrage à froid (cold-start), caractérisés par une faible densité d'interactions utilisateur-item.

## Pertinence SysCRED
Pour SysCRED (Systèmes CrEdibles), cet article est pertinent à plusieurs égards :
*   **Robustesse et gestion du démarrage à froid :** La capacité de KGNN-LS à fonctionner efficacement dans des scénarios de démarrage à froid est fondamentale pour la crédibilité des systèmes de recommandation. Elle garantit que le système peut fournir des recommandations fiables même face à des données limitées, un facteur clé pour la confiance des utilisateurs et la robustesse du système.
*   **Potentiel d'interprétabilité et d'explicabilité :** L'utilisation de graphes de connaissances (KGs) et la personnalisation des relations importantes pour chaque utilisateur ouvrent la voie à une meilleure interprétabilité. Bien que non l'objectif principal du papier, la structure explicite du KG et la pondération utilisateur-spécifique des relations pourraient servir de base pour générer des explications transparentes sur les recommandations, un élément essentiel des systèmes crédibles.
*   **Fondement sémantique pour l'équité :** En s'appuyant sur des relations sémantiques explicites (KGs) plutôt que uniquement sur des corrélations implicites, KGNN-LS pourrait potentiellement offrir un cadre plus riche pour explorer et atténuer certains types de biais inhérents aux données d'interaction, contribuant ainsi à des recommandations plus équitables, même si la question de l'équité n'est pas directement abordée dans cette recherche.

*(Généré par Gemini)*

