---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Rudin2019'
---
# Rudin2019
- **Titre:** Stop explaining black box machine learning models for high stakes decisions and use interpretable models instead
- **Auteurs:** Rudin, Cynthia
- **Année:** 2019
- **DOI:** 10.1038/s42256-019-0048-x
- **PDF:** ![[MANQUANT]]

---
## Abstract
Cet article de Cynthia Rudin (2019) critique fermement l'approche consistant à utiliser des modèles d'apprentissage automatique "boîte noire" pour des décisions à fort enjeu, puis à tenter d'expliquer leurs résultats a posteriori. Elle soutient que ces explications sont souvent trompeuses, incomplètes et peuvent créer une fausse impression de compréhension et de confiance. Rudin plaide plutôt pour l'utilisation de modèles intrinsèquement interprétables dès le départ, affirmant qu'ils offrent une transparence, une fiabilité et une responsabilité supérieures, tout en pouvant atteindre une précision comparable dans de nombreux domaines critiques.

## Contribution principale
La contribution principale de Rudin est de remettre en question le paradigme dominant de l'IA explicable (XAI) qui se concentre sur les explications post-hoc des modèles complexes. Elle propose un changement de paradigme, suggérant que pour les applications à enjeux élevés, il est essentiel de construire des modèles qui sont interprétables "par conception" (interpretable-by-design) plutôt que d'essayer d'expliquer l'opacité. Elle démontre que les modèles interprétables peuvent rivaliser avec les performances des boîtes noires tout en offrant une transparence et une fiabilité bien supérieures, remettant en question la nécessité même des modèles boîte noire dans ces contextes critiques.

## Méthodologie
L'article de Rudin n'est pas une étude empirique mais plutôt un essai théorique et une prise de position. Sa méthodologie repose sur :
1.  **Une critique conceptuelle et argumentative** des limites inhérentes et des dangers des explications post-hoc pour les modèles boîte noire, en soulignant leur manque de fidélité, de stabilité et leur potentiel de tromperie.
2.  **Une analyse comparative** entre les propriétés des modèles boîte noire expliqués et les modèles intrinsèquement interprétables.
3.  **La présentation d'exemples** concrets de modèles interprétables (comme les modèles additifs généralisés parcimonieux ou les arbres de décision optimaux) qui ont démontré des performances de pointe dans des domaines à fort enjeu, tels que la médecine ou la justice pénale.
4.  **L'articulation d'un cadre éthique et pratique** pour la construction de systèmes d'IA responsables dans des contextes critiques.

## Résultats clés
1.  **Les explications des boîtes noires sont souvent imparfaites et dangereuses :** Elles peuvent être inexactes, instables face à de petites perturbations d'entrée, ou incomplètes, conduisant à une compréhension erronée du comportement réel du modèle et masquant potentiellement des biais ou des erreurs.
2.  **Les modèles interprétables peuvent égaler la précision des boîtes noires :** Rudin démontre, avec des exemples concrets, qu'il est souvent possible de concevoir des modèles simples et transparents qui atteignent une précision comparable, voire supérieure, aux modèles boîte noire les plus complexes dans des tâches à haute criticité.
3.  **L'interprétabilité intrinsèque favorise la confiance et la responsabilité :** En connaissant précisément le fonctionnement d'un modèle, les experts humains peuvent le vérifier, le corriger et en assumer la responsabilité, ce qui est crucial pour les décisions à fort enjeu.
4.  **Un changement de mentalité est nécessaire :** Il est impératif de cesser de considérer l'interprétabilité comme une fonctionnalité ajoutée à un modèle opaque, mais plutôt comme une exigence fondamentale dès la phase de conception pour les systèmes critiques.

## Pertinence SysCRED
Pour SysCRED (Systèmes CRitiques et ExigenceS Déterminantes), l'article de Rudin est d'une pertinence capitale pour plusieurs raisons :

*   **Décisions à fort enjeu :** Le cœur de SysCRED réside dans l'étude et la conception de systèmes où les erreurs ont des conséquences graves. La thèse de Rudin s'aligne parfaitement avec cette préoccupation en insistant sur la nécessité d'une transparence maximale pour les modèles décisionnels dans de tels systèmes (santé, justice, transport, etc.).
*   **Fiabilité et Confiance :** La capacité à comprendre et à vérifier le comportement d'un système est fondamentale pour sa fiabilité et pour instaurer la confiance des utilisateurs et des régulateurs. Les modèles interprétables par conception, tels que proposés par Rudin, sont intrinsèquement plus fiables et dignes de confiance que les boîtes noires dont les "explications" peuvent induire en erreur.
*   **Vérification et Validation :** Dans les systèmes critiques, la vérification et la validation sont des processus rigoureux. Il est beaucoup plus aisé de valider un modèle dont la logique est explicite et compréhensible qu'un modèle opaque. Ceci aide à identifier et à corriger les biais ou les vulnérabilités.
*   **Responsabilité et Éthique :** L'article aborde directement la question de la responsabilité des systèmes d'IA. Pour les systèmes critiques, savoir "qui est responsable de quoi" est essentiel. Les modèles interprétables permettent d'attribuer une responsabilité claire, car la logique de décision est transparente, ce qui est crucial pour l'IA éthique et responsable.
*   **Exigences réglementaires :** De nombreuses réglementations (comme le Règlement Général sur la Protection des Données ou le futur AI Act européen) exigent une certaine forme d'explicabilité pour les décisions automatisées. L'approche de Rudin offre une voie robuste et plus authentique pour répondre à ces exigences, en allant au-delà de simples "explications" superficielles.
*   **Ingénierie des exigences :** L'article suggère d'intégrer l'interprétabilité comme une exigence non fonctionnelle essentielle dès le début du cycle de vie du développement des systèmes critiques basés sur l'IA, influençant ainsi la sélection et la conception des modèles.

*(Généré par Gemini)*


### 🔴 Accès Manuel Requis
- [Sofia UQAM](https://uqam.on.worldcat.org/search?queryString=ti:Stop%20explaining%20black%20box%20machine%20learning%20models%20for%20high%20stakes%20decisions%20and%20use%20interpretable%20models%20instead)
- [Google Scholar (Proxy UQAM)](https://proxy.bibliotheques.uqam.ca/login?url=https://scholar.google.com/scholar?q=Stop%20explaining%20black%20box%20machine%20learning%20models%20for%20high%20stakes%20decisions%20and%20use%20interpretable%20models%20instead)

