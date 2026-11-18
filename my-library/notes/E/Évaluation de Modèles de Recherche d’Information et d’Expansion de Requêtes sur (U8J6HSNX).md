---
title: "Évaluation de Modèles de Recherche d’Information et d’Expansion de Requêtes sur la Collection TREC AP 88-90"
item-type: "journalArticle"
authors:
  - "Loyer, Dominique S"
date: "28 avril 2025"
year: "2025"
pages: "7"
language: "fr"
tags:
  - "RI"
  - "RechercheInformation"
  - "TREC, Pyserini, BM25, QLD, Stemming, Expansion de Requêtes, RM3"
  - "doi-fix:low-confidence"
  - "notion"
collections:
  - "mes papiers et beamers"
zotero-key: "U8J6HSNX"
zotero-library: 1
zotero-uri: "zotero://select/library/items/U8J6HSNX"
date-added: "2025-05-30 18:45:25"
date-modified: "2026-11-18 01:43:44"
---

# Évaluation de Modèles de Recherche d’Information et d’Expansion de Requêtes sur la Collection TREC AP 88-90

**Loyer, Dominique S**

## Abstract

Ce rapport détaille l’implémentation et l’évaluation comparative d’un système de recherche d’information (RI) monolingue sur la collection standard TREC Associated Press (AP) 8890. Nous avons étudié l’influence du prétraitement du texte (stemming Porter vs baseline), de la longueur des requêtes (courtes vs longues) et du modèle de pondération (QLD vs BM25). Le système a été développé en Python avec Pyserini sous Java 21. La meilleure configuration de base identifiée (Baseline, Requêtes Longues, BM25) a atteint un MAP de 0.2205. Le stemming s’est avéré moins performant que la baseline (MAP max de 0.1778). Une technique d’amélioration par pseudo-retour de pertinence, RM3, appliquée sur la meilleure configuration baseline, a permis d’atteindre un MAP final de 0.2948, démontrant une amélioration significative (+34

## Attachments

- [Notion](https://app.notion.com/p/Loyer-2025-4129fa248c578196ba5df5ecae29ab47)

---

[Open in Zotero](zotero://select/library/items/U8J6HSNX)
