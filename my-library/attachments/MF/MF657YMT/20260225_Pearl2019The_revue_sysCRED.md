---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Pearl2019The'
---
# Pearl2019The
- **Titre:** The seven tools of causal inference, with reflections on machine learning
- **Auteurs:** Pearl, Judea
- **Année:** 2019
- **DOI:** 10.1145/3241036
- **PDF:** ![[MANQUANT]]

---
## Abstract
Cet article de Judea Pearl (2019) propose une synthèse des principes fondamentaux de l'inférence causale et de ses applications potentielles pour surmonter les limitations actuelles de l'apprentissage automatique (ML). L'auteur y expose la "Ladder of Causation" (échelle de la causalité) en trois niveaux – association, intervention et contrefactuel – et démontre que la majorité des systèmes de ML opèrent uniquement au niveau de l'association. Pearl identifie sept outils pratiques, issus de son cadre formel de la causalité, pour permettre aux systèmes d'IA de raisonner au-delà de la corrélation, vers la compréhension des causes et des effets, l'explication et la capacité à répondre à des questions contrefactuelles. L'objectif est de guider le développement de systèmes d'IA plus robustes, explicables, éthiques et dotés d'une intelligence de niveau humain.

## Contribution principale
La contribution principale de Pearl est de fournir un cadre conceptuel et opérationnel pour intégrer le raisonnement causal dans les systèmes d'IA, arguant que c'est la voie indispensable pour passer d'une IA basée sur les données à une IA basée sur la connaissance et la compréhension. Il établit clairement la distinction entre les tâches d'apprentissage automatique purement statistiques (niveau 1 de l'échelle de la causalité) et les questions causales nécessitant des interventions (niveau 2) ou des raisonnements contrefactuels (niveau 3), soulignant les lacunes intrinsèques des approches ML actuelles pour ces derniers. En présentant les "sept outils de l'inférence causale", Pearl offre une feuille de route concrète pour doter les machines de la capacité à modéliser, identifier et prédire les relations de cause à effet, une étape cruciale pour l'explicabilité, la transférabilité et la robustesse des modèles d'IA.

## Méthodologie
L'article est une œuvre conceptuelle et théorique, s'appuyant sur des fondements logiques et mathématiques rigoureux développés par Pearl au fil de décennies de recherche. La "méthodologie" employée est celle de la formalisation et de la systématisation des principes de l'inférence causale.
1.  **Modélisation Graphique:** Utilisation des graphes acycliques dirigés (DAGs) pour représenter visuellement les relations causales entre les variables, permettant une formalisation claire des hypothèses causales.
2.  **La "Ladder of Causation":** Proposition d'une hiérarchie structurée des capacités cognitives, de l'observation à l'imagination contrefactuelle.
3.  **Le do-calculus:** Présentation d'un langage formel et d'un ensemble de règles algébriques pour dériver les effets des interventions à partir de données observationnelles et de modèles graphiques.
4.  **Identification des Sept Outils:** Synthèse et application de ces principes sous forme d'outils pratiques pour des problèmes spécifiques d'inférence causale.

## Résultats clés
Les résultats clés du papier sont l'identification et la description des sept outils fondamentaux de l'inférence causale, chacun répondant à un type spécifique de question causale ou de problème de modélisation :
1.  **Causal Diagrams (DAGs) :** Représentation graphique des hypothèses causales.
2.  **The Ladder of Causation :** Un cadre pour classer les tâches cognitives (association, intervention, contrefactuel).
3.  **Causal Effect Identification :** Utilisation du do-calculus et des critères de backdoor/frontdoor pour identifier les effets causaux.
4.  **Mediation Analysis :** Comprendre les mécanismes par lesquels une cause produit son effet.
5.  **Counterfactual Analysis :** Répondre à des questions "que se serait-il passé si...".
6.  **External Validity/Transportability :** Adapter les conclusions causales d'un contexte à un autre.
7.  **Missing Data :** Gérer les données manquantes en utilisant des modèles causaux pour éviter les biais.
Ensemble, ces outils constituent une base pour construire des systèmes d'IA capables de raisonner sur les causes et les effets, offrant ainsi une voie vers une intelligence artificielle plus avancée, robuste et interprétable, capable de gérer des tâches comme l'explication, la détection des biais, la planification d'interventions et la généralisation à de nouveaux environnements.

## Pertinence SysCRED
Pour un centre comme SysCRED (Systèmes, Cyber, Recherche, Éthique, Droit), la lecture de cet article est d'une pertinence capitale, car il aborde directement les limitations des systèmes d'IA actuels en matière de transparence, de robustesse, d'équité et de responsabilité :
1.  **Explicabilité (XAI) :** Les modèles causaux de Pearl fournissent un cadre pour l'IA explicable en permettant de comprendre *pourquoi* une décision est prise (en identifiant les causes) plutôt que simplement *comment* elle est prise (par des corrélations). Cela est crucial pour la confiance, l'auditabilité et la conformité juridique et éthique des systèmes.
2.  **Équité et Bias :** L'inférence causale est essentielle pour identifier et mitiger les biais algorithmiques. Elle permet de distinguer les corrélations fortuites des véritables liens causaux qui contribuent à l'inéquité, et de concevoir des interventions ciblées pour promouvoir l'équité, plutôt que de simplement masquer les symptômes.
3.  **Robustesse et Sécurité Cyber :** La compréhension des relations causales est fondamentale pour construire des systèmes d'IA plus robustes face aux changements de distribution (dérive des données) ou aux attaques adverses. Un système qui comprend les causes sous-jacentes d'un comportement est mieux à même de s'adapter et de résister aux perturbations imprévues, ce qui est vital pour la cybersécurité et la résilience des systèmes.
4.  **Réglementation et Droit :** La capacité à répondre à des questions contrefactuelles ("qu'aurait-il fallu faire pour obtenir un autre résultat ?") est au cœur de la responsabilité juridique et éthique. Les cadres causaux de Pearl offrent des outils pour évaluer les conséquences d'actions alternatives, ce qui est indispensable pour l'élaboration de politiques et la régulation de l'IA.
5.  **Prise de Décision Éthique :** En permettant aux systèmes de raisonner sur les conséquences d'interventions et de considérer des scénarios contrefactuels, les outils de Pearl facilitent la conception d'IA capable de prendre des décisions plus éthiques et alignées sur les valeurs humaines, en anticipant les impacts potentiels de leurs actions.

*(Généré par Gemini)*


### 🔴 Accès Manuel Requis
- [Sofia UQAM](https://uqam.on.worldcat.org/search?queryString=ti:The%20seven%20tools%20of%20causal%20inference%2C%20with%20reflections%20on%20machine%20learning)
- [Google Scholar (Proxy UQAM)](https://proxy.bibliotheques.uqam.ca/login?url=https://scholar.google.com/scholar?q=The%20seven%20tools%20of%20causal%20inference%2C%20with%20reflections%20on%20machine%20learning)

