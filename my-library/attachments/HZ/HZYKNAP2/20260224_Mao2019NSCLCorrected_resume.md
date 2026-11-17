---
Date: '20260224'
tags:
  - ia/neuro-symbolique
  - revue-de-litterature
  - doctorat
  - uqam
  - syscred
authors: Dominique Loyer
title: '2026-02-24 12:45 — Mao2019NSCLCorrected'
---

# Mao2019NSCLCorrected

| Champ | Valeur |
|-------|--------|
| **Titre** | The Neuro-Symbolic Concept Learner: Interpreting Scenes Words and Sentences From Natural Supervision |
| **Auteurs** | Mao, Jiayuan and Gan, Chuang and Kohli, Pushmeet and Tenenbaum, Joshua B and Wu, Jiajun |
| **Année** | 2019 |
| **DOI** | N/A |
| **PDF** | ✅ Mao_2019_The_Neuro_Symbolic.pdf |
| **Vérification** | ✅ Vérifié |

---

## Abstract
Le Neuro-Symbolic Concept Learner (NS-CL) est un modèle qui apprend les concepts visuels, les mots et l'analyse sémantique de phrases sans supervision explicite, en se basant uniquement sur l'observation d'images et la lecture de paires questions-réponses. Ce modèle construit une représentation de scène basée sur des objets et traduit les phrases en programmes symboliques exécutables. Un module de raisonnement neuro-symbolique exécute ces programmes sur la représentation latente de la scène, permettant ainsi de relier la perception et le langage.

## Contribution principale
- Apprentissage de concepts visuels, de représentations de mots et d'analyse sémantique de phrases sans supervision explicite, uniquement à partir de supervision naturelle (images et paires questions-réponses).
- Proposition d'une architecture qui combine une représentation de scène basée sur des objets avec la traduction de phrases en programmes symboliques exécutables, liés par un module de raisonnement neuro-symbolique.
- Démontre une capacité de généralisation aisée à de nouveaux attributs d'objets, compositions, concepts linguistiques, scènes, questions et même à de nouveaux domaines de programmes.

## Methodologie
Le NS-CL est structuré autour de modules de perception et de langage interdépendants. Le module de perception apprend les concepts visuels en se basant sur la description linguistique des objets, à la manière de l'apprentissage humain. Simultanément, les concepts visuels acquis facilitent l'apprentissage de nouveaux mots et l'analyse de nouvelles phrases par le module de langage. Ce dernier traduit les phrases en programmes symboliques. Un module de raisonnement neuro-symbolique joue un rôle clé en exécutant ces programmes sur la représentation latente de la scène, servant de pont entre les modules visuel et linguistique. L'apprentissage est guidé par une approche de curriculum learning pour naviguer efficacement dans le vaste espace compositionnel des images et du langage.

## Resultats cles
- Le modèle démontre une exactitude et une efficacité élevées pour l'apprentissage des concepts visuels, des représentations de mots et de l'analyse sémantique des phrases.
- Il permet une généralisation facile à de nouveaux attributs d'objets, compositions, concepts linguistiques, scènes et questions, et même à de nouveaux domaines de programmes.

## Pertinence pour SysCRED
Ce travail est hautement pertinent pour SysCRED, car il s'inscrit directement dans le domaine de l'IA neuro-symbolique, une approche prometteuse pour construire des systèmes plus interprétables et fiables. La capacité du NS-CL à apprendre des concepts complexes à partir de supervision naturelle, tout en assurant une généralisation robuste, est fondamentale pour développer des agents crédibles. L'intégration du raisonnement symbolique avec des représentations neuronales latentes pourrait inspirer la conception de systèmes de GraphRAG plus performants, où la structure symbolique pourrait enrichir la contextualisation et la génération d'informations vérifiables. En améliorant l'interprétabilité et la capacité de généralisation, le NS-CL contribue directement à renforcer la confiance envers les systèmes d'IA.

## Citation LaTeX
\citep{Mao2019NSCLCorrected}

---

## Notes personnelles
[À compléter]

---
*Généré automatiquement le 2026-02-24 12:45 — SysCRED bibtex_batch.py v2*
