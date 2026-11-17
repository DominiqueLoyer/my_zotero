---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Siganos2019Explaining'
---
# Siganos2019Explaining
- **Titre:** Explaining and Interpreting Black-Box Models: A Survey on the Role of Interaction
- **Auteurs:** Siganos, Georgios and Vlachos, Michalis and Gunopulos, Dimitrios
- **Année:** 2019
- **DOI:** 10.1145/3236009
- **PDF:** ![[MANQUANT]]

---
## Abstract
Cet article de revue aborde la problématique croissante des modèles "boîtes noires" en apprentissage automatique et la nécessité d'en expliquer et d'en interpréter les décisions. Les auteurs passent en revue les méthodes existantes d'explicabilité de l'IA (XAI), en mettant un accent particulier sur le rôle de l'interaction entre l'utilisateur et le système d'explication. Ils soutiennent que les approches statiques d'explication sont souvent insuffisantes et que l'intégration de mécanismes interactifs est essentielle pour une compréhension plus profonde, une confiance accrue et une meilleure utilisation des systèmes d'IA. Le survey classifie les méthodes XAI existantes selon leur degré et leur type d'interaction, identifie les lacunes et propose des pistes pour les recherches futures dans le domaine.

## Contribution principale
La contribution principale de Siganos et al. est la systématisation et la classification des méthodes d'explicabilité des modèles "boîtes noires" en fonction de la nature et de l'étendue de l'interaction utilisateur qu'elles proposent. Le papier ne se contente pas de recenser les techniques XAI, mais argumente de manière convaincante que l'interaction n'est pas un aspect secondaire, mais un élément fondamental pour la construction d'explications *efficaces*, *pertinentes* et *adaptées* aux besoins spécifiques de l'utilisateur. Ils mettent en lumière que l'interaction permet une meilleure compréhension des incertitudes, une investigation plus poussée et une adaptation des explications en temps réel, offrant ainsi une perspective critique sur les limites des approches XAI non-interactives.

## Méthodologie
La méthodologie employée est celle d'une étude de revue systématique de la littérature (survey). Les auteurs ont identifié et analysé un large éventail de publications pertinentes dans le domaine de l'explicabilité de l'IA. Ils ont ensuite catégorisé ces approches en fonction de plusieurs dimensions clés, notamment :
1.  **La nature de l'explication :** Locale (pour une instance spécifique) ou globale (pour le modèle entier).
2.  **Le moment de l'explication :** Post-hoc (après l'entraînement du modèle) ou intrinsèque (modèle explicable par conception).
3.  **Le type d'interaction :** Absence d'interaction, interaction par requête (ex: "pourquoi cette décision ?"), interaction itérative (ex: affiner une explication), interaction par feedback (ex: l'utilisateur évalue la qualité de l'explication).
Cette classification a permis de dégager un cadre conceptuel pour évaluer les différentes techniques et identifier les tendances ainsi que les lacunes en matière d'intégration de l'interaction.

## Résultats clés
1.  **Typologie de l'interaction :** Le survey propose une classification des méthodes XAI en fonction de leur capacité interactive, allant des méthodes purement statiques aux systèmes permettant des requêtes complexes et des boucles de rétroaction utilisateur.
2.  **Bénéfices de l'interaction :** Les auteurs montrent que l'interaction peut considérablement améliorer la compréhension utilisateur, la confiance dans le modèle, la détection des biais et la capacité à déboguer les modèles d'IA. Elle permet également d'adapter les explications aux connaissances et aux objectifs spécifiques de l'utilisateur.
3.  **Lacunes identifiées :** Le survey met en évidence un manque d'outils et de méthodologies robustes pour évaluer l'efficacité des méthodes XAI interactives, notamment en termes de charge cognitive pour l'utilisateur, de temps d'interaction et d'impact réel sur la prise de décision. Il pointe également une insuffisance de l'intégration des principes de l'interaction humain-machine (IHM) dans la conception des systèmes XAI.
4.  **Orientations futures :** Les auteurs appellent à davantage de recherches sur la conception d'interfaces interactives pour l'XAI, l'évaluation centrée sur l'utilisateur, et l'exploration de nouvelles formes d'interaction (e.g., explications personnalisées, multi-modales).

## Pertinence SysCRED
Pour SysCRED (UQAM), cet article est d'une pertinence capitale pour plusieurs raisons :
1.  **Confiance et Crédibilité des Systèmes :** L'un des piliers de SysCRED est la recherche sur la confiance et la crédibilité des systèmes. En démontrant que l'interaction est cruciale pour une compréhension effective et une acceptation des décisions de l'IA, cet article fournit une base théorique solide pour la conception de systèmes plus fiables et dignes de confiance.
2.  **Interaction Humain-Machine (IHM) et IA Responsable :** La mise en avant du rôle de l'interaction place l'utilisateur au centre de la démarche d'explicabilité, ce qui est fondamental pour l'IHM et l'élaboration de principes d'IA responsable. SysCRED peut s'appuyer sur ces travaux pour développer des interfaces XAI qui tiennent compte des facteurs cognitifs et sociaux.
3.  **Conception et Évaluation de Systèmes Explicables :** Le travail de classification et l'identification des lacunes offrent une feuille de route pour les chercheurs de SysCRED souhaitant concevoir et évaluer de nouveaux systèmes XAI. Cela inclut la recherche sur des métriques d'évaluation plus pertinentes pour les explications interactives et l'intégration de boucles de rétroaction utilisateur dans des architectures de systèmes complexes.
4.  **Sécurité et Détection de Biais :** Une meilleure compréhension des modèles grâce à l'interaction peut aider à identifier les vulnérabilités, les biais ou les comportements inattendus, contribuant ainsi à la robustesse et à la sécurité des systèmes d'IA, des domaines d'intérêt majeurs pour SysCRED.
5.  **Gouvernance et Éthique de l'IA :** La capacité à expliquer et à interagir avec les modèles est essentielle pour la mise en œuvre de régulations et de cadres éthiques autour de l'IA. Cet article contribue à la réflexion sur les moyens techniques de répondre aux exigences de transparence et de redevabilité.

*(Généré par Gemini)*


### 🔴 Accès Manuel Requis
- [Sofia UQAM](https://uqam.on.worldcat.org/search?queryString=ti:Explaining%20and%20Interpreting%20Black-Box%20Models%3A%20A%20Survey%20on%20the%20Role%20of%20Interaction)
- [Google Scholar (Proxy UQAM)](https://proxy.bibliotheques.uqam.ca/login?url=https://scholar.google.com/scholar?q=Explaining%20and%20Interpreting%20Black-Box%20Models%3A%20A%20Survey%20on%20the%20Role%20of%20Interaction)

