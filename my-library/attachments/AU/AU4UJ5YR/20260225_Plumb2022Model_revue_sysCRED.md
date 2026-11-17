---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Plumb2022Model'
---
# Plumb2022Model
- **Titre:** Model Agnostic Supervised Local Explanations
- **Auteurs:** Plumb, Gregory and Molitor, David and Talwalkar, Ameet S.
- **Année:** 2022
- **DOI:** 10.14428/esann/2022.es2022-34
- **PDF:** ![[MANQUANT]]

---
## Abstract
L'article "Model Agnostic Supervised Local Explanations" introduit une nouvelle approche pour l'explicabilité locale des modèles d'apprentissage automatique complexes. Contrairement aux méthodes existantes qui construisent des explications pour chaque instance individuellement et de manière non supervisée (comme LIME ou SHAP), cette recherche propose une méthode pour *apprendre* à générer des explications locales. Le but est d'améliorer la stabilité, la cohérence et la fidélité des explications en tirant parti d'une supervision globale sur l'ensemble des données. La méthode vise à produire des modèles explicatifs locaux plus robustes et plus faciles à interpréter pour des prédictions spécifiques de modèles "boîtes noires".

## Contribution principale
La contribution principale est l'introduction du concept d'explications locales *supervisées* et agnostiques au modèle, concrétisée par la méthode SLISEMAP (Supervised LInear SimplE Model Agnostic Explanations). Au lieu d'ajuster un modèle interprétable localement à chaque point de données de manière indépendante, SLISEMAP apprend un ensemble de modèles explicatifs linéaires simples qui approximent localement le modèle complexe sur l'ensemble du jeu de données. Cet apprentissage global permet d'obtenir des explications plus cohérentes et stables pour des instances similaires, et d'optimiser simultanément la fidélité de l'explication et sa simplicité.

## Méthodologie
La méthodologie de SLISEMAP repose sur une formulation d'optimisation. Elle cherche à apprendre, pour chaque instance dans un voisinage, un modèle linéaire simple qui reproduit le comportement du modèle boîte noire. Plutôt que de faire cela instance par instance, l'approche *supervise* cet apprentissage en optimisant une fonction de coût sur l'ensemble du dataset. Cette fonction de coût équilibre plusieurs objectifs :
1.  **Fidélité locale :** La capacité du modèle explicatif simple à se conformer aux prédictions du modèle boîte noire dans le voisinage d'une instance.
2.  **Simplicité/Interprétabilité :** Maintenir la complexité des modèles locaux à un niveau faible (e.g., modèles linéaires avec peu de caractéristiques).
3.  **Cohérence :** Encourager des explications similaires pour des instances similaires dans l'espace des caractéristiques.
Le processus implique l'apprentissage des pondérations pour les caractéristiques de chaque explication locale, en minimisant une erreur combinée sur l'ensemble du dataset.

## Résultats clés
Les auteurs démontrent que SLISEMAP génère des explications locales qui sont significativement plus stables et cohérentes pour des instances similaires par rapport aux méthodes agnostiques non supervisées comme LIME et SHAP. Les évaluations montrent également une fidélité compétitive, voire supérieure, au modèle boîte noire. Les résultats soulignent que l'approche supervisée peut produire des explications plus fiables et moins bruitées, ce qui facilite leur interprétation par les experts humains et permet une meilleure compréhension globale du comportement du modèle complexe.

## Pertinence SysCRED
Cette recherche est d'une grande pertinence pour SysCRED, étant donné l'engagement du laboratoire dans l'étude des systèmes cyber-physiques critiques et de la cybersécurité. L'utilisation croissante de modèles d'apprentissage automatique complexes (souvent opaques) dans la détection d'anomalies, la prédiction de menaces ou l'évaluation de la fiabilité soulève des défis majeurs en termes de confiance, de transparence et d'auditabilité.

1.  **Confiance et Transparence des Systèmes Critiques :** La capacité à expliquer localement les décisions d'un modèle est fondamentale pour les opérateurs humains. Comprendre *pourquoi* un système d'IA a classé une activité réseau comme malveillante ou a prédit une défaillance critique permet une prise de décision éclairée et renforce la confiance dans l'automatisation.
2.  **Auditabilité et Conformité :** Dans les environnements réglementés (énergie, transport, santé), la conformité exige souvent une traçabilité et une justifiabilité des décisions automatisées. Les explications stables et cohérentes de SLISEMAP faciliteraient les audits et la démonstration de la conformité.
3.  **Débogage et Robustesse :** Des explications fiables peuvent aider à identifier les biais ou les faiblesses d'un modèle ML dans un contexte de cybersécurité (par exemple, des vulnérabilités aux attaques adverses) ou de fiabilité. Elles permettent aux ingénieurs de déboguer les modèles et d'améliorer leur robustesse dans des scénarios critiques.
4.  **Optimisation des Interventions Humaines :** En fournissant des raisons claires et stables pour les alertes ou les prédictions, les systèmes basés sur SLISEMAP peuvent aider les analystes de sécurité ou les ingénieurs en fiabilité à prioriser leurs interventions et à agir plus efficacement.

En somme, l'approche de "supervision" des explications proposée par Plumb et al. promet des outils plus robustes pour rendre les systèmes d'IA critiques plus intelligibles, un objectif central pour SysCRED.

*(Généré par Gemini)*


### 🔴 Accès Manuel Requis
- [Sofia UQAM](https://uqam.on.worldcat.org/search?queryString=ti:Model%20Agnostic%20Supervised%20Local%20Explanations)
- [Google Scholar (Proxy UQAM)](https://proxy.bibliotheques.uqam.ca/login?url=https://scholar.google.com/scholar?q=Model%20Agnostic%20Supervised%20Local%20Explanations)

