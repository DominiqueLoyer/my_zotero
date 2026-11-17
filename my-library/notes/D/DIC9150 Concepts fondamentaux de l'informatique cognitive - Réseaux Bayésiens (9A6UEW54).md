---
title: "DIC9150 Concepts fondamentaux de l'informatique cognitive - Réseaux Bayésiens"
item-type: "journalArticle"
authors:
  - "Villemaire, Roger"
date: "A2024"
year: "0000"
language: "fr"
tags:
  - "Bayes"
  - "Réseaux Bayésiens"
  - "Villemaire Roger"
  - "notion"
  - "⛔ No DOI found"
collections:
  - "Cours A24/Dic9150/Réseaux bayésiens"
zotero-key: "9A6UEW54"
zotero-library: 1
zotero-uri: "zotero://select/library/items/9A6UEW54"
date-added: "2024-12-08 17:46:23"
date-modified: "2025-12-29 23:57:34"
---

# DIC9150 Concepts fondamentaux de l'informatique cognitive - Réseaux Bayésiens

**Villemaire, Roger**

## Attachments

- [Notion](https://app.notion.com/p/Villemaire-4129fa248c5781f192c2decb8b5adaa6)
- [Villemaire - DIC9150 Concepts fondamentaux de l'informatique cognitive - Réseaux Bayésiens.pdf](../../attachments/JV/JVYH9SIA/Villemaire%20-%20DIC9150%20Concepts%20fondamentaux%20de%20l'informatique%20cognitive%20-%20R%C3%A9seaux%20Bay%C3%A9siens.pdf)

## Annotations

- **p. 7, highlight** “Un événement aléatoire est une condition sur des variables aléatoires, comme par exemple : ● V = d, pour un d ∈ domV ,  ● V /= d ∪ V /= d′, pour des d, d′ ∈ domV .”
- **p. 8, highlight** “événements aléatoires”
- **p. 8, highlight** “unions des “zones”
- **p. 8, highlight** “probabilité P(E)”
- **p. 8, highlight** “événement E”
- **p. 8, highlight** “taille”
- **p. 8, highlight** “probabilité totale”
- **p. 8, highlight** “tout l’espace”
- **p. 8, highlight** “P(True) = 1”
- **p. 10, highlight** “Probabilité a priori”
- **p. 10, highlight** “mesures de la “chance””
- **p. 10, highlight** “événements surviennent”
- **p. 10, highlight** “’on ne sait rien sur les événements qui se sont déjà produits”
- **p. 10, highlight** “Si E′ s’est produit”
- **p. 10, highlight** “probabilité a priori n’est pas un bon indicateur”
- **p. 11, highlight** “Probabilité a posteriori”
- **p. 11, highlight** “a posteriori”
- **p. 11, highlight** “E conditionnelle à E′”
- **p. 11, highlight** “P(E ∩ E′)/P(E′)”
- **p. 12, highlight** “P(Pa∣Pl)”
- **p. 12, highlight** “P(Pa ∩ Pl)/P(Pl)”
- **p. 14, highlight** “Indépendance conditionnelle”
- **p. 14, highlight** “la probabilité que A se produise étant donné C n’est pas changée si l’on sait, de plus, que B s’est produit.”
- **p. 14, highlight** “ceci est le cas si le fait d’avoir B n’influence pas le fait d’avoir A, mais pas réciproquemen”
- **p. 15, highlight** “Belief Network)”
- **p. 15, highlight** “graphe orienté acyclique”
- **p. 15, highlight** “noeuds”
- **p. 15, highlight** “variables aléatoires,”
- **p. 15, highlight** “noeud V ,”
- **p. 15, highlight** “noeud W qui n’est pas un descendant de V”
- **p. 15, highlight** “parents(V ) = {V ′; V ′ → V dans le réseau}”
- **p. 15, highlight** “n’est pas modifiée par l’ajout d’un non-descendant W .”
- **p. 17, highlight** “réseau bayésien représente donc les dépendances conditionnelles.”
- **p. 17, highlight** “les parents d’un noeud ne sont pas nécessairement ses causes,”
- **p. 17, highlight** “les causes permettent en général des réseaux bayésiens compact”
- **p. 17, highlight** “P(noeud∣parents et des non-descendants) = P(noeud∣parents)”
- **p. 18, highlight** “Pour V1, . . . , Vn les variables aléatoires du réseau, la distribution de probabilité totale P(V1, . . . , Vn) détermine la probabilité de toutes les combinaisons de valeurs des variables.”
- **p. 18, highlight** “Elle permet donc de déterminer la probabilité de n’importe quel événement aléatoire défini à partir de ces variables. ● C’est donc un description complète du système probabiliste.”
- **p. 19, highlight** “P(X ∣Y ) = P(X ∩Y )  P(Y ) donc  P(X , Y ) = P(X ∩ Y ) = P(X ∣Y ) ⋅ P(Y )  ● P(TS, PS, Pa) = P(TS∣PS, Pa) ⋅ P(PS, Pa) = P(TS∣PS, Pa) ⋅ P(PS∣Pa) ⋅ P(Pa) = P(TS∣Pa) ⋅ P(PS∣Pa) ⋅ P(Pa)”
- **p. 20, highlight** “expert du domaine pourra déterminer correctement les relations causales”
- **p. 20, highlight** “variables et ainsi établir un réseau bayésien correct”
- **p. 20, highlight** “plus difficile”
- **p. 20, highlight** “les probabilités”
- **p. 20, highlight** “possible d’automatiser ce processus en récupérant des données, pour calculer les fréquences et s’en servir comme valeurs des probabilités”
- **p. 21, highlight** “difficiles voire impossibles à mesurer directement”
- **p. 21, highlight** “variables latentes.”
- **p. 21, highlight** “méthodes analogues à celles utilisées avec les réseaux neuronaux de déterminer des probabilités pour les variables qui minimisent les différences entre les valeurs mesurées (les données) et celles prédites par le réseaux.”
- **p. 22, highlight** “réseau est établi, avec ses probabilités, on peut faire générer des données pseudo-aléatoires satisfaisant ces distributions”
- **p. 22, highlight** “calculer les fréquences pour n’importe quelle événement. Il s’agit donc d’une méthode de calcul par simulation”
- **p. 22, highlight** “déterminer ou transformer un réseau bayésien à partir de données”
- **p. 22, highlight** “comparer les réseaux bayésiens et ainsi valider le modèle”
- **p. 23, highlight** “L’incertitude”
- **p. 23, highlight** “les applications”
- **p. 23, highlight** “probabilités sont une méthode de représentation de l’incertitude”
- **p. 23, highlight** “● Les réseaux bayésiens permettent en général une représentation compacte”
- **p. 23, highlight** “probabilité totale”
- **p. 23, highlight** “probabilité totale.”

---

[Open in Zotero](zotero://select/library/items/9A6UEW54)
