---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Wiz2018Data'
---
# Wiz2018Data
- **Titre:** Data poisoning attacks explained
- **Auteurs:** Wiz
- **Année:** 2018
- **DOI:** 10.1007/978-3-031-01580-9_6
- **PDF:** ![[MANQUANT]]

---
## Abstract
Cet article, "Data poisoning attacks explained", fournit une introduction et une vue d'ensemble complètes des attaques par empoisonnement des données ciblant les systèmes d'apprentissage automatique. Il clarifie les mécanismes, les objectifs et les impacts de ces attaques, où des acteurs malveillants injectent des données corrompues dans l'ensemble d'entraînement d'un modèle ML pour compromettre son intégrité, sa performance ou son comportement futur. L'auteur explique comment ces attaques peuvent mener à une dégradation de la précision du modèle, à des biais indésirables ou à l'introduction de vulnérabilités "backdoor".

## Contribution principale
La contribution principale de cet article est de démystifier et de vulgariser le concept des attaques par empoisonnement des données pour un public potentiellement non expert en sécurité ML. Il offre une explication claire des différentes typologies d'attaques (e.g., empoisonnement de la disponibilité pour dégrader la performance générale, empoisonnement de l'intégrité pour introduire des comportements spécifiques), de leurs motivations sous-jacentes et des vecteurs possibles. L'article sert de ressource fondamentale pour comprendre les menaces pesant sur la phase d'entraînement des modèles d'apprentissage.

## Méthodologie
La méthodologie de "Data poisoning attacks explained" repose sur une approche descriptive et explicative. L'auteur synthétise les connaissances existantes et les concepts théoriques relatifs aux attaques par empoisonnement. Il s'agit d'une analyse conceptuelle et d'une revue structurée des différentes facettes de ces attaques, en s'appuyant potentiellement sur des exemples ou des scénarios hypothétiques pour illustrer les mécanismes. Aucune expérimentation originale ou développement algorithmique n'est présenté; l'article se concentre sur la clarification et la systématisation des connaissances établies sur le sujet.

## Résultats clés
Les résultats clés de cet article mettent en lumière plusieurs aspects critiques des attaques par empoisonnement des données :
1.  **Nature et Impact:** Ces attaques manipulent les données d'entraînement pour soit dégrader la performance globale du modèle (attaques de disponibilité), soit lui faire adopter des comportements spécifiques ou introduire des erreurs ciblées pour certaines entrées (attaques d'intégrité ou de backdoor).
2.  **Subtilité et Détection:** Les attaques peuvent être très subtiles, rendant difficile la détection des données empoisonnées parmi l'ensemble d'entraînement légitime, surtout dans les systèmes où les données sont collectées de sources ouvertes ou dynamiques.
3.  **Vulnérabilité des Systèmes ML:** L'article souligne la vulnérabilité intrinsèque des modèles ML au processus d'entraînement, faisant de l'empoisonnement une menace sérieuse pour la confiance et la fiabilité des systèmes basés sur l'IA.
4.  **Prérequis de l'Attaquant:** L'efficacité de l'attaque dépend souvent de la connaissance qu'a l'attaquant de l'algorithme d'apprentissage, de l'ensemble de données, ou des caractéristiques de l'espace des fonctionnalités.

## Pertinence SysCRED
Pour SysCRED (UQAM), cet article est d'une pertinence capitale, s'inscrivant directement dans plusieurs de nos axes de recherche :
*   **Sécurité des Systèmes d'Apprentissage Automatique :** Les attaques par empoisonnement des données représentent une menace fondamentale pour la sécurité et l'intégrité des systèmes d'IA/ML, un domaine d'intérêt majeur pour SysCRED. Comprendre ces attaques est la première étape vers le développement de défenses robustes.
*   **Fiabilité et Dépendabilité :** Un modèle empoisonné est par définition non fiable et non dépendable. L'article met en évidence comment ces attaques peuvent compromettre la capacité d'un système à fonctionner comme prévu, ce qui est au cœur de nos préoccupations en matière de fiabilité et de dépendabilité des systèmes.
*   **Robustesse des Systèmes :** La recherche SysCRED vise à concevoir des systèmes robustes. Cet article identifie une faiblesse majeure dans la chaîne de valeur de l'IA, stimulant la recherche sur des mécanismes d'entraînement plus résilients, des techniques de détection d'anomalies dans les données d'entraînement et des stratégies de désintoxication des données.
*   **Évaluation des Risques Cybersécurité :** Il fournit une base conceptuelle pour l'évaluation des risques liés au déploiement de modèles ML en production, en particulier dans des environnements où les données d'entraînement peuvent être soumises à des manipulations adverses.
*   **Pistes de Recherche :** Il ouvre des pistes de recherche pour développer des méthodes d'apprentissage fédéré sécurisées, des techniques d'apprentissage adversaires pour la détection et la mitigation de l'empoisonnement, et des architectures de pipelines ML résilientes aux attaques de la chaîne d'approvisionnement de données.

*(Généré par Gemini)*


### 🔴 Accès Manuel Requis
- [Sofia UQAM](https://uqam.on.worldcat.org/search?queryString=ti:Data%20poisoning%20attacks%20explained)
- [Google Scholar (Proxy UQAM)](https://proxy.bibliotheques.uqam.ca/login?url=https://scholar.google.com/scholar?q=Data%20poisoning%20attacks%20explained)

