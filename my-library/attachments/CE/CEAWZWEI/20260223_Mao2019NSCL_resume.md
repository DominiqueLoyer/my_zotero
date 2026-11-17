---
Date: '20260223'
tags:
  - ia/neuro-symbolique
  - revue-de-litterature
  - doctorat
  - uqam
  - syscred
authors: Dominique Loyer
title: '2026-02-23 15:52 — Mao2019NSCL'
---

# Mao2019NSCL

| Champ | Valeur |
|-------|--------|
| **Titre** | The Neuro-Symbolic Concept Learner: Interpreting Scenes, Words, and Sentences |
| **Auteurs** | Mao, Jiayuan and others |
| **Année** | 2019 |
| **DOI** | N/A |
| **PDF** | ✅ Mao_2019_The_Neuro_Symbolic.pdf |

---

## Abstract
Le Neuro-Symbolic Concept Learner (NS-CL) est un modèle qui apprend des concepts visuels, des mots et le parsing sémantique de phrases sans supervision explicite. Il y parvient en observant des images et en lisant des paires de questions/réponses, en construisant une représentation de scène basée sur les objets et en traduisant les phrases en programmes symboliques exécutables. Un module de raisonnement neuro-symbolique exécute ces programmes sur la représentation latente de la scène pour faciliter un apprentissage mutuel entre la perception et le langage.

## Contribution principale
- Apprentissage de concepts visuels, de mots et du parsing sémantique *sans supervision explicite*, uniquement à partir de paires images/questions/réponses.
- Introduction d'une architecture *neuro-symbolique* intégrant un module de raisonnement pour exécuter des programmes symboliques sur une représentation de scène latente.
- Démontre une *généralisation facile* à de nouveaux attributs d'objets, compositions, concepts linguistiques, scènes et questions, ainsi qu'à de nouveaux domaines de programmes.

## Methodologie
Le modèle NS-CL apprend en observant des images et en traitant des questions et réponses appariées. Il construit une représentation de scène basée sur des objets et traduit les phrases en programmes symboliques exécutables. Pour lier ces deux modules, il utilise un module de raisonnement neuro-symbolique qui exécute les programmes sur la représentation latente de la scène. Similaire à l'apprentissage humain, le module de perception apprend les concepts visuels à partir de descriptions linguistiques, et réciproquement, les concepts visuels facilitent l'apprentissage de nouveaux mots et le parsing de phrases. L'apprentissage par curriculum est employé pour guider la recherche dans le vaste espace compositionnel des images et du langage.

## Resultats cles
- Démontre une grande précision et efficacité dans l'apprentissage des concepts visuels, des représentations de mots et du parsing sémantique des phrases.
- Permet une généralisation aisée à de nouveaux attributs d'objets, compositions, concepts linguistiques, scènes, questions et même de nouveaux domaines de programmes.
- Habilite des applications pratiques telles que le *Visual Question Answering* et la recherche bidirectionnelle image-texte.

## Pertinence pour SysCRED
Le NS-CL est hautement pertinent pour SysCRED car il représente une avancée majeure dans l'**IA neuro-symbolique**, un domaine clé pour la robustesse et l'explicabilité des systèmes intelligents. Sa capacité à apprendre des concepts interprétables à partir de supervision naturelle, et à traduire des requêtes linguistiques en programmes symboliques exécutables, améliore la **crédibilité** en offrant des chemins de raisonnement potentiellement plus clairs. Ce type d'architecture, en construisant des représentations de scènes basées sur des objets et en les liant à des logiques symboliques, pourrait faciliter l'intégration avec des systèmes de **GraphRAG** en permettant l'extraction et la structuration de connaissances visuelles et textuelles en graphes sémantiques. Enfin, l'analogie avec l'apprentissage humain pour la co-construction de la perception et du langage ouvre des voies vers une **confiance** accrue dans les modèles d'IA, car ils s'alignent davantage sur nos propres modes de compréhension.

## Citation LaTeX
\citep{Mao2019NSCL}

---

## Notes personnelles
[À compléter]

---
*Généré automatiquement le 2026-02-23 15:52 — SysCRED bibtex_batch.py*
