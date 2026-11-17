---
Date: '20260304'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-03-04 - Momeni2025Continual'
---
# Momeni2025Continual
- **Titre:** Continual {{Learning Using}} a {{Kernel-Based Method Over Foundation Models
- **Auteurs:** Momeni, Saleh and Mazumder, Sahisnu and Liu, Bing
- **Année:** 2025
- **DOI:** 10.1609/aaai.v39i18.34150
- **PDF:** ![[Momeni_2025_Continual_Learning_Using.pdf]]

---
## Abstract
L'article présente une nouvelle méthode appelée Kernel Linear Discriminant Analysis (KLDA) pour résoudre le problème de l'apprentissage continu (CL) dans le cadre de la reconnaissance de classes incrémentales (CIL). La CIL est un défi important dans le domaine de l'apprentissage automatique, car elle nécessite que le modèle apprenne de nouvelles classes sans oublier les connaissances acquises précédemment.

## Contribution principale
La contribution principale de cet article est l'introduction de la méthode KLDA, qui utilise les représentations de caractéristiques riches d'un modèle de base (FM) pour améliorer la séparabilité des classes dans l'espace de caractéristiques. La méthode KLDA utilise des fonctions noyau pour mapper les données dans un espace de dimension supérieure, où les caractéristiques deviennent plus linéairement séparables.

## Méthodologie
La méthodologie utilisée dans cet article consiste à utiliser un modèle de base (FM) pour extraire les caractéristiques des échantillons d'entrée, puis à appliquer des fonctions noyau pour améliorer la représentation des caractéristiques. Les caractéristiques noyau sont ensuite utilisées pour calculer la moyenne de classe de chaque classe et pour mettre à jour une matrice de covariance partagée pour toutes les classes apprises jusqu'à présent. La moyenne de classe et la matrice de covariance partagée définissent une distribution gaussienne pour chaque classe, qui est ensuite utilisée pour optimiser la séparabilité des classes à l'aide de l'analyse discriminante linéaire (LDA).

## Résultats clés
Les résultats clés de cet article sont que la méthode KLDA peut atteindre un niveau de précision comparable à la limite supérieure de la CIL, sans utiliser de données de répétition. La méthode KLDA est également capable de résoudre les deux défis majeurs de la CIL, à savoir l'oubli catastrophique (CF) et la séparation des classes entre les tâches (ICS).

## Pertinence SysCRED
La pertinence de cet article pour le projet SysCRED est qu'il propose une nouvelle méthode pour résoudre le problème de l'apprentissage continu dans le contexte de la reconnaissance de classes incrémentales. Cette méthode peut être utilisée pour améliorer la capacité d'apprentissage des systèmes de reconnaissance de classes dans des environnements dynamiques, où les données sont incrémentales et où les classes sont ajoutées de manière incrémentale. Cela peut être particulièrement utile dans des applications telles que la reconnaissance d'images, la reconnaissance de parole et la détection d'anomalies.

*(Généré par Groq)*

