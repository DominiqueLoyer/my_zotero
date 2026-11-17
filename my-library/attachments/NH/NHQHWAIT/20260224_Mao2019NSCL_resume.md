---
Date: '20260224'
tags:
  - ia/neuro-symbolique
  - revue-de-litterature
  - doctorat
  - uqam
  - syscred
authors: Dominique Loyer
title: '2026-02-24 12:43 — Mao2019NSCL'
---

# Mao2019NSCL

| Champ | Valeur |
|-------|--------|
| **Titre** | The Neuro-Symbolic Concept Learner: Interpreting Scenes, Words, and Sentences |
| **Auteurs** | Mao, Jiayuan and others |
| **Année** | 2019 |
| **DOI** | N/A |
| **PDF** | ✅ Mao_2019_The_Neuro_Symbolic.pdf |
| **Vérification** | ✅ Vérifié |

---

## Abstract
Le Neuro-Symbolic Concept Learner (NS-CL) est un modèle qui apprend simultanément des concepts visuels, des mots et l'analyse sémantique de phrases sans supervision explicite. Il y parvient en observant des images et en lisant des paires questions-réponses. Le modèle utilise un module de raisonnement neuro-symbolique pour exécuter des programmes symboliques sur une représentation de scène latente.

## Contribution principale
- Apprentissage non supervisé de concepts visuels, de représentations de mots et de l'analyse sémantique de phrases, uniquement à partir d'images et de paires questions-réponses.
- Intégration d'un module neuro-symbolique qui construit une représentation de scène basée sur les objets et traduit les phrases en programmes exécutables.
- Démonstration d'une généralisation aisée à de nouveaux attributs d'objets, compositions, concepts linguistiques, scènes et questions, et même à de nouveaux domaines de programmes, ainsi que des applications au *visual question answering* et à la recherche image-texte.

## Methodologie
Le NS-CL fonctionne en construisant une représentation de scène basée sur les objets et en traduisant les phrases en programmes symboliques exécutables. Un module de raisonnement neuro-symbolique exécute ensuite ces programmes sur la représentation latente de la scène. L'apprentissage des concepts visuels par le module de perception est fondé sur la description linguistique des objets, tandis que les concepts visuels appris facilitent en retour l'apprentissage de nouveaux mots et l'analyse de nouvelles phrases. L'apprentissage curriculaire est utilisé pour guider la recherche dans le vaste espace compositionnel des images et du langage.

## Resultats cles
- Le modèle démontre une précision et une efficacité élevées dans l'apprentissage des concepts visuels, des représentations de mots et de l'analyse sémantique des phrases.
- Il permet une généralisation facile à de nouveaux attributs d'objets, compositions, concepts linguistiques, scènes, questions et domaines de programmes.

## Pertinence pour SysCRED
Cet article est hautement pertinent pour SysCRED, en particulier dans le domaine de l'IA neuro-symbolique et de l'informatique cognitive. Le NS-CL combine explicitement les forces de la perception neuronale et du raisonnement symbolique, ce qui est fondamental pour développer des systèmes d'IA plus interprétables et robustes. La traduction de questions linguistiques en programmes symboliques exécutables sur des représentations de scène latentes est prometteuse pour renforcer la crédibilité et la confiance dans les systèmes d'IA, car elle offre une traçabilité potentielle du processus de raisonnement. De plus, la capacité à apprendre des concepts visuels et à les aligner avec le langage pourrait être exploitée pour construire des représentations de connaissances riches et structurées, essentielles pour alimenter des systèmes de type GraphRAG, en permettant une interrogation plus sémantique et un raisonnement basé sur des graphes à partir de données multimodales.

## Citation LaTeX
\citep{Mao2019NSCL}

---

## Notes personnelles
[À compléter]

---
*Généré automatiquement le 2026-02-24 12:43 — SysCRED bibtex_batch.py v2*
