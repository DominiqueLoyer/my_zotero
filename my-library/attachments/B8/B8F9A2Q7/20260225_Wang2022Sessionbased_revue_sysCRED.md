---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Wang2022Sessionbased'
---
# Wang2022Sessionbased
- **Titre:** Session-based recommendation with recurrent neural networks
- **Auteurs:** Wang, Xiang and He, Xia and Cao, Tao and Liu, Meng and Chua, Tat-Seng
- **Année:** 2022
- **DOI:** 10.1016/j.compeleceng.2022.107916
- **PDF:** ![[MANQUANT]]

---
## Abstract
Cet article aborde le problème de la recommandation basée sur les sessions (SBR), où l'objectif est de prédire le prochain élément avec lequel un utilisateur interagira, en se basant uniquement sur la séquence d'interactions récentes au sein d'une session anonyme. Les auteurs proposent un modèle de réseau de neurones récurrents (RNN) spécifiquement conçu pour capturer les dépendances séquentielles complexes et les préférences dynamiques des utilisateurs manifestées au cours d'une session. Le modèle vise à surmonter les limitations des approches traditionnelles en modélisant efficacement l'évolution de l'intention de l'utilisateur à court terme.

## Contribution principale
La contribution principale de cet article est la proposition d'une architecture de réseau de neurones récurrents (RNN) optimisée pour la tâche de recommandation basée sur les sessions. Cette architecture est conçue pour modéliser de manière robuste les dépendances séquentielles fines entre les éléments d'une session, permettant ainsi de mieux comprendre l'évolution de l'intérêt de l'utilisateur. Contrairement aux modèles traditionnels, qui peuvent avoir du mal à saisir les dynamiques de session à court terme, ce modèle RNN est capable de générer des représentations contextuelles riches pour chaque étape de la session, menant à des prédictions plus précises du prochain élément.

## Méthodologie
La méthodologie repose sur l'utilisation d'un réseau de neurones récurrents.
1.  **Représentation des éléments:** Chaque élément est d'abord représenté par un *embedding* dense, appris conjointement avec le modèle RNN.
2.  **Traitement séquentiel:** La séquence d'éléments au sein d'une session est traitée séquentiellement par le RNN. À chaque étape, le RNN prend en entrée l'embedding de l'élément actuel et l'état caché précédent pour mettre à jour son état interne.
3.  **Modélisation de l'état de session:** L'état caché du RNN à un instant *t* encapsule l'historique de la session jusqu'à cet instant, servant de représentation vectorielle des préférences de l'utilisateur à ce moment précis.
4.  **Prédiction du prochain élément:** L'état caché final (ou une combinaison d'états) est ensuite projeté vers l'espace des embeddings d'éléments via une couche de sortie (généralement une couche softmax) pour générer une distribution de probabilité sur tous les éléments possibles, indiquant la probabilité que chaque élément soit le prochain dans la session.
5.  **Entraînement:** Le modèle est entraîné de bout en bout en utilisant la descente de gradient stochastique, avec une fonction de perte basée sur l'entropie croisée, pour minimiser l'erreur de prédiction du prochain élément. Les ensembles de données typiques utilisés sont des logs de sessions réelles (ex: Yoochoose, Diginetica).

## Résultats clés
Les résultats clés de l'étude démontrent que le modèle RNN proposé surpasse significativement les méthodes de recommandation basées sur les sessions existantes, y compris les approches basées sur des modèles de Markov et d'autres techniques de filtrage collaboratif. Les métriques d'évaluation telles que la Précision@k (P@k) et le Mean Reciprocal Rank@k (MRR@k) sont généralement plus élevées pour le modèle RNN sur plusieurs ensembles de données réels. Ces résultats mettent en évidence la capacité des RNN à capturer efficacement les dépendances séquentielles complexes et les dynamiques à court terme des préférences des utilisateurs, conduisant à des recommandations plus pertinentes et opportunes au sein d'une session.

## Pertinence SysCRED
Cet article est hautement pertinent pour SysCRED (Systèmes complexes, Réseaux, Éthique, Données) à l'UQAM pour plusieurs raisons :
1.  **Modélisation de systèmes complexes :** Les sessions utilisateur et les systèmes de recommandation sont des exemples classiques de systèmes complexes. L'approche RNN pour SBR s'inscrit directement dans l'intérêt de SysCRED pour la modélisation et l'analyse de ces systèmes, notamment la manière dont les interactions individuelles (clics, vues) se combinent pour former des dynamiques de comportement agrégées.
2.  **Analyse de données et Apprentissage profond :** L'utilisation de réseaux de neurones récurrents, une technique d'apprentissage profond de pointe, est au cœur des compétences et des intérêts de recherche de SysCRED en matière d'analyse avancée de données et de développement de modèles d'IA robustes.
3.  **Fondation pour la recherche éthique et explicable :** Comprendre le fonctionnement interne de modèles de recommandation performants comme celui-ci est une étape fondamentale pour aborder des questions cruciales de SysCRED telles que l'explicabilité (XAI), la partialité et l'équité des recommandations. Un modèle performant sert de base pour explorer comment ces aspects peuvent être améliorés ou analysés.
4.  **Applications pratiques :** Les systèmes de recommandation sont omniprésents dans les plateformes numériques (e-commerce, médias sociaux, etc.). Les avancées dans ce domaine ont des implications directes sur l'expérience utilisateur, l'économie numérique et, par extension, sur des questions sociétales que SysCRED explore.
5.  **Robustesse et sécurité des modèles :** Bien que non directement abordé dans cet article, un modèle SBR basé sur RNN fournit une base pour la recherche future sur la robustesse de ces systèmes face à des données bruitées ou des attaques adverses, un domaine d'intérêt pour SysCRED concernant la fiabilité des systèmes d'IA.

*(Généré par Gemini)*


### 🔴 Accès Manuel Requis
- [Sofia UQAM](https://uqam.on.worldcat.org/search?queryString=ti:Session-based%20recommendation%20with%20recurrent%20neural%20networks)
- [Google Scholar (Proxy UQAM)](https://proxy.bibliotheques.uqam.ca/login?url=https://scholar.google.com/scholar?q=Session-based%20recommendation%20with%20recurrent%20neural%20networks)

