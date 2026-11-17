---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Sarwar2001'
---
# Sarwar2001
- **Titre:** Item-Based Collaborative Filtering Recommendation Algorithms
- **Auteurs:** Sarwar, Badrul and Karypis, George and Konstan, Joseph A. and Riedl, John
- **Année:** 2001
- **DOI:** 10.1145/371920.372071
- **PDF:** ![[Sarwar_2001_Item_Based_Collaborative.pdf]]

---
## Abstract
Cet article aborde les défis des systèmes de recommandation, notamment la production de recommandations de haute qualité à grande échelle pour des millions d'utilisateurs et d'éléments, et la couverture malgré la rareté des données. Les systèmes traditionnels de filtrage collaboratif (basés sur les utilisateurs) voient leur travail augmenter avec le nombre de participants. Pour y remédier, les auteurs explorent les techniques de filtrage collaboratif basé sur les éléments. Ces techniques analysent la matrice utilisateur-élément pour identifier les relations entre les éléments, puis utilisent ces relations pour calculer indirectement des recommandations. L'article analyse différentes techniques de calcul de similarité entre éléments (corrélation, similarité cosinus) et de génération de recommandations (somme pondérée, modèle de régression). Les résultats expérimentaux suggèrent que les algorithmes basés sur les éléments offrent des performances et une qualité nettement supérieures à celles des algorithmes basés sur les utilisateurs.

## Contribution principale
La contribution principale est l'introduction et l'évaluation approfondie des techniques de filtrage collaboratif basé sur les éléments (item-based collaborative filtering) comme solution aux problèmes de scalabilité et de performance des algorithmes traditionnels basés sur les utilisateurs (k-plus proches voisins), tout en offrant une meilleure qualité de recommandation. L'article détaille et compare diverses approches pour calculer la similarité entre éléments et générer des recommandations.

## Méthodologie
Les auteurs ont exploré et analysé différentes techniques de filtrage collaboratif basé sur les éléments. Leur méthodologie comprend :
1.  **Analyse de la matrice utilisateur-élément** pour identifier les relations entre les éléments.
2.  **Comparaison de techniques de calcul de similarité inter-éléments** : notamment la corrélation item-item et la similarité cosinus entre les vecteurs d'éléments.
3.  **Comparaison de techniques de génération de recommandations** : incluant la somme pondérée et le modèle de régression.
4.  **Évaluation expérimentale** des algorithmes basés sur les éléments.
5.  **Comparaison** des résultats avec l'approche de base du k-plus proches voisins (user-based).

## Résultats clés
Les expérimentations ont montré que :
*   Les algorithmes basés sur les éléments offrent des **performances considérablement meilleures** que les algorithmes basés sur les utilisateurs.
*   Les algorithmes basés sur les éléments fournissent une **meilleure qualité de recommandation** que les meilleurs algorithmes basés sur les utilisateurs disponibles.

## Pertinence SysCRED
Ce travail est hautement pertinent pour SysCRED car il aborde des défis fondamentaux et critiques des systèmes de recommandation.
1.  **Scalabilité et Performance** : Le papier propose une solution majeure aux problèmes de scalabilité des systèmes de recommandation traditionnels, un aspect crucial pour le déploiement de systèmes "critiques" dans des environnements réels avec des millions d'utilisateurs et d'éléments.
2.  **Qualité des Recommandations** : L'amélioration de la qualité des recommandations est un objectif central pour tout système critique, et cet article démontre comment l'approche basée sur les éléments y parvient.
3.  **Fondation Théorique et Pratique** : Cet article est une œuvre fondatrice pour les approches basées sur les éléments, qui sont devenues un pilier de nombreux systèmes de recommandation modernes. Comprendre cette base est essentiel pour toute recherche avancée ou critique dans le domaine.
4.  **Dépassement des Limites Existantestes** : Le papier identifie et propose des solutions aux limitations inhérentes aux systèmes de filtrage collaboratif basés sur les utilisateurs, ce qui est pertinent pour l'analyse des faiblesses et l'amélioration des systèmes de recommandation.

*(Généré par Gemini)*

