---
Date: '20260304'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-03-04 - Sennrich2016Improving'
---
# Sennrich2016Improving
- **Titre:** Improving Neural Machine Translation Models with Monolingual Data
- **Auteurs:** Sennrich, Rico and Haddow, Barry and Birch, Alexandra
- **Année:** 2016
- **DOI:** 10.18653/v1/p16-1009
- **PDF:** ![[Sennrich_2016_Improving_Neural_Machine.pdf]]

---
## Abstract
L'article "Improving Neural Machine Translation Models with Monolingual Data" présente une approche pour améliorer les modèles de traduction automatique neuronale (NMT) en utilisant des données monolingues. Les auteurs explorent les stratégies pour intégrer des données monolingues dans le processus d'apprentissage sans modifier l'architecture du réseau neuronal.

## Contribution principale
La contribution principale de cet article est de montrer que l'on peut améliorer la qualité de la traduction automatique des systèmes NMT en mélangeant des phrases monolingues cibles dans l'ensemble d'apprentissage. Les auteurs proposent deux méthodes pour remplir le côté source des instances d'apprentissage monolingues : utiliser une phrase source factice ou utiliser une phrase source obtenue via une traduction inverse (backtranslation), qu'ils appellent synthétique.

## Méthodologie
La méthodologie utilisée dans cet article consiste à associer des données monolingues d'apprentissage avec une traduction inverse automatique, ce qui permet de les traiter comme des données d'apprentissage parallèles supplémentaires. Les auteurs ont utilisé des architectures encodeur-décodeur pour les modèles NMT et ont évalué leurs approches sur les tâches WMT 15 et IWSLT 14.

## Résultats clés
Les résultats clés de cet article sont les améliorations substantielles obtenues sur les tâches WMT 15 et IWSLT 14, avec des gains de 2,8-3,7 points BLEU pour la tâche anglais-allemand et de 2,1-3,4 points BLEU pour la tâche turc-anglais. Les auteurs ont également montré que la fine-tuning sur des données monolingues et parallèles dans le domaine donne des améliorations substantielles pour la tâche IWSLT 15.

## Pertinence SysCRED
Cette recherche est pertinente pour le projet SysCRED car elle explore les possibilités d'amélioration des modèles de traduction automatique neuronale en utilisant des données monolingues, ce qui est un aspect important pour améliorer la qualité de la traduction automatique dans les contextes où les données parallèles sont limitées. Les résultats de cette étude pourraient être appliqués pour améliorer les systèmes de traduction automatique utilisés dans les projets de recherche et développement du SysCRED.

*(Généré par Groq)*

