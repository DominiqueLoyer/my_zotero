---
Date: '20260304'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-03-04 - Liu2020Multilingual'
---
# Liu2020Multilingual
- **Titre:** Multilingual Denoising Pre-training for Neural Machine Translation
- **Auteurs:** Liu, Yinhan and Gu, Jiatao and Goyal, Naman and Li, Xuan and Smith,грайворонский, Сергей and Zettlemoyer, Luke and Stoyanov, Veselin
- **Année:** 2020
- **DOI:** 10.1162/tacl_a_00343
- **PDF:** ![[Liu_2020_Multilingual_Denoising_Pre.pdf]]

---
## Abstract
Cet article présente une approche de pré-entraînement multilingue pour la traduction automatique neuronale, appelée mBART. Cette méthode utilise un modèle de type sequence-to-sequence pour reconstruire des textes entiers à partir de versions bruyantes, en appliquant l'objectif BART à des corpus monolingues à grande échelle dans de nombreuses langues.

## Contribution principale
La contribution principale de cet article est de proposer une méthode de pré-entraînement qui permet d'améliorer les performances de la traduction automatique neuronale, en particulier pour les paires de langues à faibles ressources. La méthode mBART pré-entraîne un modèle complet de type sequence-to-sequence, qui peut être affiné pour différentes tâches de traduction sans modification spécifique.

## Méthodologie
La méthodologie utilisée dans cet article consiste à pré-entraîner un modèle mBART sur des corpus monolingues à grande échelle dans de nombreuses langues, en appliquant l'objectif BART. Les textes d'entrée sont bruyés en masquant des phrases et en permutant des phrases, et un modèle Transformer est appris pour reconstruire les textes. Le modèle mBART est ensuite affiné pour différentes tâches de traduction, notamment la traduction supervisée et non supervisée.

## Résultats clés
Les résultats clés de cet article montrent que la méthode mBART améliore les performances de la traduction automatique neuronale, en particulier pour les paires de langues à faibles ressources. Les gains de performance sont de l'ordre de 12 points BLEU pour les paires de langues à faibles ressources et de 5 points BLEU pour les paires de langues à ressources moyennes.

## Pertinence SysCRED
La pertinence de cet article pour le SysCRED est élevée, car il propose une méthode de pré-entraînement qui peut être utilisée pour améliorer les performances de la traduction automatique neuronale, notamment pour les paires de langues à faibles ressources. Cela est particulièrement pertinent pour les applications de traduction automatique dans les contextes de développement, où les ressources de traduction sont souvent limitées. De plus, la méthode mBART peut être utilisée pour améliorer les performances de la traduction automatique dans d'autres domaines, tels que la traduction de documents et la traduction non supervisée.

*(Généré par Groq)*

