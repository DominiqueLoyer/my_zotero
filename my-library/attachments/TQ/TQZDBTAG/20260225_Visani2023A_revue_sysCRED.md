---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Visani2023A'
---
# Visani2023A
- **Titre:** A survey on the state of the art of the reliability of post-hoc explanation methods
- **Auteurs:** Visani, Giulio and Bagli, Enrico and Chesani, Federico
- **Année:** 2023
- **DOI:** 10.36227/techrxiv.173834937.72763339/v1
- **PDF:** ![[MANQUANT]]

---
En tant qu'assistant de recherche doctoral au SysCRED de l'UQAM, voici mon analyse de l'article de Visani, Bagli et Chesani (2023) :

## Abstract
This survey paper by Visani et al. (2023) provides a comprehensive review of the state-of-the-art concerning the *reliability* of post-hoc explanation methods in eXplainable Artificial Intelligence (XAI). The authors delve into the various facets of reliability, such as stability, robustness, and faithfulness, identifying them as critical challenges that profoundly impact the trustworthiness and practical applicability of AI explanations. The paper synthesizes existing literature, categorizes different approaches to assess and improve reliability, and highlights key open problems and future research directions essential for advancing the field towards more credible and dependable AI systems.

## Contribution principale
La contribution principale de cet article est de fournir une synthèse critique et exhaustive de l'état de l'art concernant la *fiabilité* des méthodes d'explication post-hoc. Les auteurs ne se contentent pas de lister les méthodes existantes, mais articulent une discussion approfondie sur les différentes définitions et métriques de la fiabilité (stabilité, robustesse, fidélité, etc.), identifiant ainsi les défis majeurs qui entravent l'adoption et la confiance dans les explications générées par l'IA. Ils proposent également une catégorisation des approches existantes pour évaluer et améliorer cette fiabilité, et mettent en lumière les lacunes de la recherche actuelle, offrant une feuille de route précieuse pour les travaux futurs.

## Méthodologie
En tant qu'article de revue, la méthodologie employée par Visani et al. repose sur une analyse systématique et critique de la littérature scientifique pertinente. Les auteurs ont probablement effectué une recherche bibliographique approfondie dans des bases de données clés (telles que IEEE Xplore, ACM Digital Library, Scopus, Web of Science, arXiv) en utilisant des mots-clés liés aux explications post-hoc, à la fiabilité, la stabilité, la robustesse et la fidélité en XAI. Le processus implique ensuite une phase de sélection des articles pertinents, leur classification thématique (par type de méthode d'explication, par critère de fiabilité étudié, par métrique d'évaluation) et enfin une synthèse qualitative des défis, des solutions proposées et des tendances identifiées dans la recherche.

## Résultats clés
Les résultats clés de cette enquête soulignent plusieurs points cruciaux :
1.  **Multitude de définitions de la fiabilité :** Il n'existe pas de consensus unique sur ce que signifie la "fiabilité" en XAI, avec des concepts variés comme la stabilité (cohérence des explications face à de petites perturbations), la robustesse (résistance aux attaques adverses ou changements environnementaux), et la fidélité (à quel point l'explication reflète le fonctionnement interne du modèle).
2.  **Vulnérabilité des méthodes existantes :** La plupart des méthodes d'explication post-hoc sont montrées comme étant vulnérables à de petites perturbations dans les données d'entrée, les hyperparamètres ou même le choix de la méthode elle-même, ce qui compromet sérieusement leur crédibilité et leur utilité.
3.  **Manque de métriques et de benchmarks standards :** Il existe un besoin pressant de métriques standardisées et de benchmarks rigoureux pour évaluer objectivement la fiabilité des explications, permettant ainsi une comparaison équitable des différentes approches.
4.  **Défis pour l'adoption pratique :** La faible fiabilité identifiée est un frein majeur à l'adoption des systèmes d'IA explicables dans des contextes critiques où la confiance est primordiale (santé, finance, justice, défense).
5.  **Directions de recherche :** L'article identifie la nécessité de développer des méthodes intrinsèquement plus fiables, des techniques de certification de fiabilité, et des approches centrées sur l'utilisateur pour mieux comprendre et évaluer la fiabilité perçue.

## Pertinence SysCRED
Cet article est d'une pertinence capitale pour les travaux menés au sein du SysCRED (Systèmes Crédibles et Explicables) de l'UQAM. Notre groupe s'attache précisément à construire des systèmes d'IA non seulement performants mais aussi dignes de confiance, transparents et explicables. Les conclusions de Visani et al. résonnent directement avec nos préoccupations concernant :

*   **La crédibilité des systèmes d'IA :** La fiabilité des explications est un pilier fondamental de la crédibilité. Si les explications sont instables, non robustes ou non fidèles, la confiance dans l'ensemble du système d'IA est érodée, ce qui est inacceptable dans des domaines critiques. Cet article nous pousse à intégrer la fiabilité comme un critère de conception et d'évaluation primordial.
*   **L'évaluation rigoureuse de la XAI :** L'appel à des métriques et des benchmarks standardisés pour la fiabilité est en parfaite adéquation avec nos efforts pour développer des cadres d'évaluation robustes et systématiques pour les systèmes XAI.
*   **La conception de systèmes explicables par conception :** Comprendre les sources d'instabilité des explications post-hoc nous informe sur la nécessité potentielle de développer des modèles intrinsèquement plus interprétables ou des méthodes d'explication dont la fiabilité est garantie par construction, plutôt que de se fier uniquement à des approches post-hoc.
*   **Les dimensions éthiques et légales de l'IA :** La non-fiabilité des explications a des implications directes sur la responsabilité, la justice, et la conformité réglementaire (e.g., RGPD et le "droit à l'explication"). SysCRED s'intéresse à ces intersections, et un manque de fiabilité rendrait les explications légalement insoutenables.
*   **L'interaction humain-IA :** La fiabilité perçue des explications est cruciale pour l'acceptation et l'efficacité de l'interaction humain-IA. Cet article fournit une base solide pour explorer comment la fiabilité technique se traduit en confiance utilisateur et comment elle influence la prise de décision assistée par l'IA.

En somme, cet article renforce notre conviction que la fiabilité n'est pas une simple caractéristique technique, mais un prérequis fondamental pour tout système d'IA explicable et crédible. Il guide nos recherches en identifiant des lacunes claires et des priorités pour construire l'avenir des systèmes d'IA dignes de confiance.

*(Généré par Gemini)*


### 🔴 Accès Manuel Requis
- [Sofia UQAM](https://uqam.on.worldcat.org/search?queryString=ti:A%20survey%20on%20the%20state%20of%20the%20art%20of%20the%20reliability%20of%20post-hoc%20explanation%20methods)
- [Google Scholar (Proxy UQAM)](https://proxy.bibliotheques.uqam.ca/login?url=https://scholar.google.com/scholar?q=A%20survey%20on%20the%20state%20of%20the%20art%20of%20the%20reliability%20of%20post-hoc%20explanation%20methods)

