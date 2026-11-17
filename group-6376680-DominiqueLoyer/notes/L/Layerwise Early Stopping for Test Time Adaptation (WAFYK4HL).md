---
title: "Layerwise Early Stopping for Test Time Adaptation"
item-type: "preprint"
authors:
  - "Sahoo, Sabyasachi"
  - "ElAraby, Mostafa"
  - "Ngnawe, Jonas"
  - "Pequignot, Yann"
  - "Precioso, Frederic"
  - "Gagne, Christian"
date: "2024-04-04"
year: "2024"
url: "http://arxiv.org/abs/2404.03784"
language: "en"
tags:
  - "Computer Science - Artificial Intelligence"
  - "Computer Science - Computer Vision and Pattern Recognition"
  - "Computer Science - Machine Learning"
  - "notion"
collections:
  - "Ma thèse"
  - "Ma thèse/Systematic review"
zotero-key: "WAFYK4HL"
zotero-library: 2
zotero-uri: "zotero://select/groups/6376680/items/WAFYK4HL"
date-added: "2026-04-17 21:21:41"
date-modified: "2026-04-17 21:21:41"
---

# Layerwise Early Stopping for Test Time Adaptation

**Sahoo, Sabyasachi; ElAraby, Mostafa; Ngnawe, Jonas; Pequignot, Yann; Precioso, Frederic; Gagne, Christian**

## Abstract

Test Time Adaptation (TTA) addresses the problem of distribution shift by enabling pretrained models to learn new features on an unseen domain at test time. However, it poses a significant challenge to maintain a balance between learning new features and retaining useful pretrained features. In this paper, we propose Layerwise EArly STopping (LEAST) for TTA to address this problem. The key idea is to stop adapting individual layers during TTA if the features being learned do not appear beneficial for the new domain. For that purpose, we propose using a novel gradient-based metric to measure the relevance of the current learnt features to the new domain without the need for supervised labels. More specifically, we propose to use this metric to determine dynamically when to stop updating each layer during TTA. This enables a more balanced adaptation, restricted to layers benefiting from it, and only for a certain number of steps. Such an approach also has the added effect of limiting the forgetting of pretrained features useful for dealing with new domains. Through extensive experiments, we demonstrate that Layerwise Early Stopping improves the performance of existing TTA approaches across multiple datasets, domain shifts, model architectures, and TTA losses.

## Extra

arXiv:2404.03784 [cs]

## Notes

### Comment: 14 pages, 5 figures

Comment: 14 pages, 5 figures

## Attachments

- [Notion](notion://www.notion.so/sahooLayerwiseEarlyStopping2024-2c09fa248c57812c853ffa2035de2cd9)

---

[Open in Zotero](zotero://select/groups/6376680/items/WAFYK4HL)
