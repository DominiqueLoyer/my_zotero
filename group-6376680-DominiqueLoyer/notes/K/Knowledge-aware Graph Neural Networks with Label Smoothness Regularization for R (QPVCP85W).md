---
title: "Knowledge-aware Graph Neural Networks with Label Smoothness Regularization for Recommender Systems"
item-type: "preprint"
authors:
  - "Wang, Hongwei"
  - "Zhang, Fuzheng"
  - "Zhang, Mengdi"
  - "Leskovec, Jure"
  - "Zhao, Miao"
  - "Li, Wenjie"
  - "Wang, Zhongyuan"
date: "2019-06-14"
year: "2019"
doi: "10.48550/arXiv.1905.04413"
url: "http://arxiv.org/abs/1905.04413"
language: "en"
tags:
  - "Computer Science - Information Retrieval"
  - "Computer Science - Machine Learning"
  - "Statistics - Machine Learning"
  - "notion"
collections:
  - "_ALL_CIT_140326/9401_ic_/PDFs"
zotero-key: "QPVCP85W"
zotero-library: 2
zotero-uri: "zotero://select/groups/6376680/items/QPVCP85W"
date-added: "2026-04-17 21:22:52"
date-modified: "2026-04-17 21:22:52"
---

# Knowledge-aware Graph Neural Networks with Label Smoothness Regularization for Recommender Systems

**Wang, Hongwei; Zhang, Fuzheng; Zhang, Mengdi; Leskovec, Jure; Zhao, Miao; Li, Wenjie; Wang, Zhongyuan**

## Abstract

Knowledge graphs capture structured information and relations between a set of entities or items. As such knowledge graphs represent an attractive source of information that could help improve recommender systems. However, existing approaches in this domain rely on manual feature engineering and do not allow for an end-to-end training. Here we propose Knowledge-aware Graph Neural Networks with Label Smoothness regularization (KGNN-LS) to provide better recommendations. Conceptually, our approach computes user-specific item embeddings by first applying a trainable function that identifies important knowledge graph relationships for a given user. This way we transform the knowledge graph into a user-specific weighted graph and then apply a graph neural network to compute personalized item embeddings. To provide better inductive bias, we rely on label smoothness assumption, which posits that adjacent items in the knowledge graph are likely to have similar user relevance labels/scores. Label smoothness provides regularization over the edge weights and we prove that it is equivalent to a label propagation scheme on a graph. We also develop an efficient implementation that shows strong scalability with respect to the knowledge graph size. Experiments on four datasets show that our method outperforms state of the art baselines. KGNN-LS also achieves strong performance in cold-start scenarios where user-item interactions are sparse.

## Extra

arXiv:1905.04413 [cs]

## Attachments

- [Notion](notion://www.notion.so/wangKnowledgeawareGraphNeural2019a-3239fa248c57817a83e4dd9e689a44d6)

---

[Open in Zotero](zotero://select/groups/6376680/items/QPVCP85W)
