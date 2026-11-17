---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Zhang2024A'
---
# Zhang2024A
- **Titre:** A Survey on Large Language Models for Recommendation
- **Auteurs:** Zhang, Zhaocheng and Liu, Jiongnan and Wu, Likang and Wang, Zhaopeng and Geng, Xingcan and Yuan, Fajie and Ren, Zhaochun
- **Année:** 2024
- **DOI:** 10.1007/s11280-024-01291-2
- **PDF:** ![[Zhang_2024_A_Survey_on.pdf]]

---
En tant qu'assistant de recherche doctoral (UQAM, SysCRED), voici mon analyse de l'extrait de l'article "A Survey on Large Language Models for Recommendation" :

## Abstract
Cette enquête examine l'intégration des grands modèles linguistiques (LLM) dans les systèmes de recommandation (RS), soulignant leur potentiel à améliorer la qualité des recommandations grâce à leurs représentations de haute qualité des caractéristiques textuelles et leur vaste couverture des connaissances externes. Les LLM, formés sur d'énormes quantités de données via l'apprentissage auto-supervisé, permettent des transferts efficaces (comme le fine-tuning ou le prompt tuning). Le survey propose une taxonomie inédite des systèmes de recommandation basés sur les LLM, les catégorisant en deux paradigmes principaux : les LLM discriminatifs pour la recommandation (DLLM4Rec) et les LLM génératifs pour la recommandation (GLLM4Rec), ce dernier étant systématiquement organisé pour la première fois. L'étude analyse les méthodologies, techniques et performances de ces systèmes, identifie les défis clés et fournit des pistes pour la recherche et la pratique, avec un dépôt GitHub associé.

## Contribution principale
La contribution principale de cette étude est de fournir une compréhension exhaustive et structurée des systèmes de recommandation basés sur les LLM. Plus spécifiquement, elle propose une taxonomie originale qui divise ces modèles en deux paradigmes distincts (DLLM4Rec et GLLM4Rec), organisant pour la première fois de manière systématique les approches génératives (GLLM4Rec). De plus, l'enquête passe en revue et analyse les systèmes existants au sein de chaque paradigme, offrant des aperçus sur leurs techniques et performances, et identifiant les défis ainsi que des découvertes précieuses pour la communauté de recherche et les praticiens.

## Méthodologie
L'étude adopte une approche de revue systématique de la littérature. La méthodologie consiste à :
1.  Définir les LLM comme des modèles basés sur l'architecture Transformer avec un grand nombre de paramètres, entraînés sur des ensembles de données massifs à l'aide de techniques d'apprentissage auto/semi-supervisé (ex: BERT, séries GPT, séries PaLM).
2.  Développer une taxonomie pour catégoriser les systèmes de recommandation basés sur les LLM en deux paradigmes majeurs : DLLM4Rec et GLLM4Rec.
3.  Procéder à un examen et une analyse systématiques des systèmes de recommandation basés sur les LLM existants dans chaque paradigme.
4.  Fournir des éclaircissements sur leurs méthodologies, techniques et performances.
5.  Identifier les défis clés et les résultats notables découlant de cette analyse.

## Résultats clés
Bien que l'extrait ne détaille pas tous les résultats spécifiques, il met en évidence que les LLM :
*   Permettent d'extraire des représentations de haute qualité des caractéristiques textuelles et de tirer parti de vastes connaissances externes pour établir des corrélations entre les items et les utilisateurs.
*   Améliorent la compréhension du contexte, des requêtes utilisateur et des descriptions d'articles, menant à une meilleure précision et pertinence des recommandations.
*   Offrent des capacités de recommandation "zero/few-shot", permettant de s'attaquer au problème de la rareté des données et de généraliser à des candidats non vus grâce à leur pré-entraînement étendu.
*   La taxonomie distingue clairement les approches discriminatives et génératives, clarifiant ainsi le paysage des LLM pour la recommandation.

## Pertinence SysCRED
Pour le laboratoire SysCRED (Systèmes CRitiques, Éthique, Données), cette enquête est très pertinente à plusieurs égards :
1.  **Fiabilité et Robustesse des Systèmes** : L'intégration des LLM dans les systèmes de recommandation, qui peuvent influencer des décisions importantes (information, achats, santé), soulève des questions critiques sur leur fiabilité, leur robustesse face aux données bruitées ou adversariales, et leur capacité à fournir des recommandations cohérentes et stables.
2.  **Explicabilité et Transparence** : Les LLM sont souvent des "boîtes noires". Pour SysCRED, la compréhension des méthodologies et des techniques (comme décrit dans l'enquête) est essentielle pour développer des mécanismes d'explicabilité et de transparence, permettant aux utilisateurs et aux développeurs de comprendre pourquoi une recommandation a été faite. Ceci est crucial pour la confiance dans les systèmes critiques.
3.  **Éthique et Biais** : L'enquête mentionne la capacité des LLM à capturer le contexte et à utiliser des connaissances externes. Cela implique également le risque de perpétuer ou d'amplifier des biais existants dans les données d'entraînement, ce qui peut conduire à des recommandations discriminatoires ou injustes. SysCRED s'intéresse à l'identification et l'atténuation de ces biais pour garantir des systèmes équitables et responsables.
4.  **Sécurité et Confidentialité** : L'utilisation de "massives amounts of data" et la "couverture extensive de connaissances externes" posent des défis en matière de confidentialité des données utilisateur et de sécurité des modèles contre les attaques d'inférence ou de manipulation.
5.  **Ingénierie des Systèmes Basés sur l'IA** : L'analyse des "méthodologies, techniques et performances" des DLLM4Rec et GLLM4Rec fournit des bases pour la conception et l'ingénierie de systèmes de recommandation complexes et critiques, intégrant l'IA de manière sûre et efficace.

*(Généré par Gemini)*

