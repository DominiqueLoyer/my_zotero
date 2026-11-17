---
Date: '20260225'
tags: [ia/neuro-symbolique, uqam, doctorat, revue-de-littérature, syscred]
author: Dominique Loyer
title: '2026-02-25 - Tjeng2025Evaluating'
---
# Tjeng2025Evaluating
- **Titre:** Evaluating robustness of neural networks with mixed integer programming
- **Auteurs:** Tjeng, Vincent and Xiao, Kai Y. and Tedrake, Russ
- **Année:** 2025
- **DOI:** 10.1016/j.neucom.2025.130214
- **PDF:** ![[MANQUANT]]

---
## Abstract
Cet article aborde le problème crucial de l'évaluation formelle de la robustesse des réseaux de neurones (NNs). Il propose une approche novatrice utilisant la programmation en nombres entiers mixtes (MIP) pour fournir des garanties vérifiables sur le comportement des NNs, notamment face à des perturbations adverses des entrées. Les auteurs développent vraisemblablement un cadre permettant de transformer les problèmes de vérification de robustesse des NNs en formulations MIP, permettant ainsi une analyse rigoureuse de leur résilience.

## Contribution principale
La contribution principale réside dans l'établissement d'un cadre rigoureux et formellement vérifiable pour évaluer la robustesse des réseaux de neurones, en exploitant la puissance de la Programmation en Nombres Entiers Mixtes. Contrairement aux méthodes d'attaques adverses empiriques, ce travail vise à fournir des bornes *prouvables* sur la sortie d'un NN pour une plage donnée de perturbations d'entrée. Cela permet des déclarations définitives sur la sécurité et la fiabilité d'un NN, ce qui est essentiel pour les applications critiques. L'article propose probablement de nouvelles formulations MIP adaptées à diverses architectures de NNs et à des propriétés de robustesse spécifiques.

## Méthodologie
La méthodologie repose sur l'encodage de l'architecture du réseau de neurones, des contraintes de son espace d'entrée et de la propriété de robustesse à vérifier, dans un problème de Programmation en Nombres Entiers Mixtes. Les fonctions d'activation ReLU, courantes dans les NNs modernes, sont généralement modélisées à l'aide de variables binaires auxiliaires et de contraintes linéaires. L'idée fondamentale est de déterminer s'il existe une perturbation d'entrée, dans une borne spécifiée, qui conduit à une sortie indésirable (par exemple, une mauvaise classification ou une déviation d'une plage de sécurité). Cette "requête de vérification" est ensuite résolue par un solveur MIP standard. Le résultat du solveur (solution réalisable ou infaisable) indique directement la présence ou l'absence d'une violation de robustesse.

## Résultats clés
Les résultats clés démontreraient la capacité de *prouver* formellement des propriétés de robustesse pour diverses architectures de réseaux de neurones, en particulier celles utilisant des activations ReLU. L'article présenterait des bornes quantifiables sur les perturbations d'entrée qu'un NN peut tolérer sans violer une propriété spécifiée. Il mettrait probablement en évidence l'identification de vulnérabilités jusqu'alors inconnues ou confirmerait la robustesse de certains réseaux dans des paramètres définis. Une comparaison avec les méthodes d'attaques adverses empiriques de pointe montrerait la supériorité de la vérification basée sur MIP pour fournir des garanties, même si potentiellement plus coûteuse en calcul pour les très grands réseaux. L'article aborderait également l'évolutivité de l'approche et les compromis potentiels.

## Pertinence SysCRED
Cette recherche est d'une pertinence capitale pour SysCRED, étant donné notre axe sur la conception, l'analyse et l'assurance des systèmes critiques, résilients et durables. L'intégration croissante des réseaux de neurones dans des domaines de sécurité critique (par exemple, la conduite autonome, les dispositifs médicaux, le contrôle industriel) exige des méthodes rigoureuses pour garantir leur fiabilité et leur crédibilité. L'approche de cet article, utilisant la MIP pour une évaluation *prouvable* de la robustesse, répond directement au besoin de vérification formelle dans de tels systèmes. Elle fournit une méthodologie fondamentale pour :

*   **Assurer la sûreté de l'IA :** Offrir des garanties contre les attaques adverses ou les comportements imprévus, cruciaux pour les systèmes où une défaillance peut avoir des conséquences graves.
*   **Certification et réglementation :** Contribuer à des méthodes pouvant étayer les processus de certification des systèmes critiques alimentés par l'IA en fournissant des preuves objectives de robustesse.
*   **Ingénierie de la résilience :** Comprendre les limites exactes de l'opération fiable d'un NN éclaire les stratégies pour construire des systèmes plus résilients capables de faire face aux incertitudes ou aux attaques ciblées.

La capacité de passer des tests empiriques aux preuves formelles s'aligne parfaitement avec l'engagement de SysCRED envers la recherche fondamentale pour des systèmes ultra-fiables.

*(Généré par Gemini)*


### 🔴 Accès Manuel Requis
- [Sofia UQAM](https://uqam.on.worldcat.org/search?queryString=ti:Evaluating%20robustness%20of%20neural%20networks%20with%20mixed%20integer%20programming)
- [Google Scholar (Proxy UQAM)](https://proxy.bibliotheques.uqam.ca/login?url=https://scholar.google.com/scholar?q=Evaluating%20robustness%20of%20neural%20networks%20with%20mixed%20integer%20programming)

