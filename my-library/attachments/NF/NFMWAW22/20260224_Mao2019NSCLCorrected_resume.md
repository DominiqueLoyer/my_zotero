---
Date: '20260224'
tags:
  - ia/neuro-symbolique
  - revue-de-litterature
  - doctorat
  - uqam
  - syscred
authors: Dominique Loyer
title: '2026-02-24 12:09 — Mao2019NSCLCorrected'
---

# Mao2019NSCLCorrected

| Champ | Valeur |
|-------|--------|
| **Titre** | The Neuro-Symbolic Concept Learner: Interpreting Scenes Words and Sentences |
| **Auteurs** | Mao, Jiayuan and Gan, Chuang and Kohli, Pushmeet and Tenenbaum, Joshua B and Wu, Jiajun |
| **Année** | 2019 |
| **DOI** | N/A |
| **PDF** | ✅ Mao_2019_The_Neuro_Symbolic.pdf |

---

## Abstract
Nous proposons le Neuro-Symbolic Concept Learner (NS-CL), un modèle qui apprend les concepts visuels, les mots et l'analyse sémantique de phrases sans supervision explicite, uniquement en observant des images et en lisant des paires de questions-réponses. Le modèle construit une représentation de scène basée sur des objets et traduit les phrases en programmes symboliques exécutables, connectant ces deux modules via un raisonnement neuro-symbolique. Cette approche permet un apprentissage mutuel où la perception affine les concepts visuels via le langage, et les concepts visuels facilitent l'apprentissage de nouveaux mots et l'analyse de phrases.

## Contribution principale
- Introduction du Neuro-Symbolic Concept Learner (NS-CL) qui apprend des concepts visuels, des mots et l'analyse sémantique de phrases à partir d'une supervision naturelle (images, questions, réponses).
- Proposition d'une architecture neuro-symbolique qui construit une représentation de scène basée sur des objets et traduit des phrases en programmes symboliques exécutables, liés par un module de raisonnement neuro-symbolique.
- Démontre une généralisation facile à de nouveaux attributs d'objets, compositions, concepts linguistiques, scènes, questions et même de nouveaux domaines de programmes.

## Methodologie
Le modèle NS-CL apprend en regardant des images et en lisant des questions et réponses associées, sans supervision explicite pour la perception ou le langage. Il construit une représentation de scène basée sur des objets, à partir de laquelle il exécute des programmes symboliques générés par l'analyse sémantique des phrases. Un module de raisonnement neuro-symbolique assure l'interface entre la perception (représentation latente de la scène) et le raisonnement symbolique. L'apprentissage est guidé par une approche curriculaire pour explorer efficacement le vaste espace compositionnel des images et du langage, où l'apprentissage des concepts visuels et celui du langage se renforcent mutuellement.

## Resultats cles
- Démontre une précision et une efficacité élevées dans l'apprentissage des concepts visuels, des représentations de mots et de l'analyse sémantique de phrases.
- Permet une généralisation aisée à de nouveaux attributs d'objets, compositions, concepts linguistiques, scènes et questions, ainsi qu'à de nouveaux domaines de programmes.
- Habilite des applications comme la réponse visuelle aux questions (VQA) et la recherche bidirectionnelle image-texte.

## Pertinence pour SysCRED
Cet article est hautement pertinent pour SysCRED en raison de son approche neuro-symbolique. La capacité du NS-CL à traduire des phrases en programmes symboliques exécutables sur des représentations de scène offre une **traçabilité** et une **interprétabilité** accrues du raisonnement, éléments cruciaux pour la **confiance** et la **crédibilité** des systèmes d'IA. Contrairement aux modèles purement neuronaux, l'architecture symbolique peut potentiellement expliciter les étapes de décision, permettant de comprendre "pourquoi" une réponse est générée. L'apprentissage de concepts visuels et leur alignement avec des descriptions linguistiques crée des connaissances structurées sur les objets et leurs attributs, ce qui pourrait être exploité pour la construction et l'enrichissement de **GraphRAG**. Ces graphes pourraient ensuite servir à ancrer et justifier les réponses du système, renforçant leur crédibilité par des faits et des relations clairement identifiables.

## Citation LaTeX
\citep{Mao2019NSCLCorrected}

---

## Notes personnelles
[À compléter]

---
*Généré automatiquement le 2026-02-24 12:09 — SysCRED bibtex_batch.py*
