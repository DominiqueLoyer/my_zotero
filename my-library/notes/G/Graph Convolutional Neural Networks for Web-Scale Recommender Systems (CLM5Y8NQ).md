---
title: "Graph Convolutional Neural Networks for Web-Scale Recommender Systems"
item-type: "conferencePaper"
authors:
  - "Ying, Rex"
  - "He, Ruining"
  - "Chen, Kaifeng"
  - "Eksombatchai, Pong"
  - "Hamilton, William L."
  - "Leskovec, Jure"
date: "2018-07-19"
year: "2018"
publication: "Proceedings of the 24th ACM SIGKDD International Conference on Knowledge Discovery & Data Mining"
pages: "974-983"
doi: "10.1145/3219819.3219890"
url: "http://arxiv.org/abs/1806.01973"
tags:
  - "Computer Science - Information Retrieval"
  - "Computer Science - Machine Learning"
  - "Statistics - Machine Learning"
  - "notion"
collections:
  - "_ALL_CIT_140326/9401_ic_/PDFs"
zotero-key: "CLM5Y8NQ"
zotero-library: 1
zotero-uri: "zotero://select/library/items/CLM5Y8NQ"
date-added: "2026-03-14 17:40:10"
date-modified: "2026-03-25 21:28:24"
---

# Graph Convolutional Neural Networks for Web-Scale Recommender Systems

**Ying, Rex; He, Ruining; Chen, Kaifeng; Eksombatchai, Pong; Hamilton, William L.; Leskovec, Jure**

## Abstract

Recent advancements in deep neural networks for graph-structured data have led to state-of-the-art performance on recommender system benchmarks. However, making these methods practical and scalable to web-scale recommendation tasks with billions of items and hundreds of millions of users remains a challenge. Here we describe a large-scale deep recommendation engine that we developed and deployed at Pinterest. We develop a data-efficient Graph Convolutional Network (GCN) algorithm PinSage, which combines efficient random walks and graph convolutions to generate embeddings of nodes (i.e., items) that incorporate both graph structure as well as node feature information. Compared to prior GCN approaches, we develop a novel method based on highly efficient random walks to structure the convolutions and design a novel training strategy that relies on harder-and-harder training examples to improve robustness and convergence of the model. We also develop an efficient MapReduce model inference algorithm to generate embeddings using a trained model. We deploy PinSage at Pinterest and train it on 7.5 billion examples on a graph with 3 billion nodes representing pins and boards, and 18 billion edges. According to offline metrics, user studies and A/B tests, PinSage generates higher-quality recommendations than comparable deep learning and graph-based alternatives. To our knowledge, this is the largest application of deep graph embeddings to date and paves the way for a new generation of web-scale recommender systems based on graph convolutional architectures.

## Extra

arXiv:1806.01973 [cs]

## Notes

### Comment: KDD 2018

Comment: KDD 2018

## Attachments

- [Notion](https://app.notion.com/p/Ying-et-al-2018-4129fa248c5781f28ca5c5f79d3300b9)
- [Ying et al. - 2018 - Graph Convolutional Neural Networks for Web-Scale Recommender Systems.pdf](../../attachments/W4/W4ZV6US4/Ying%20et%20al.%20-%202018%20-%20Graph%20Convolutional%20Neural%20Networks%20for%20Web-Scale%20Recommender%20Systems.pdf)

---

[Open in Zotero](zotero://select/library/items/CLM5Y8NQ)
