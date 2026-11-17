---
title: "Neural Graph Collaborative Filtering"
item-type: "conferencePaper"
authors:
  - "Wang, Xiang"
  - "He, Xiangnan"
  - "Wang, Meng"
  - "Feng, Fuli"
  - "Chua, Tat-Seng"
date: "2019-07-18"
year: "2019"
publication: "Proceedings of the 42nd International ACM SIGIR Conference on Research and Development in Information Retrieval"
pages: "165-174"
doi: "10.1145/3331184.3331267"
url: "http://arxiv.org/abs/1905.08108"
tags:
  - "Computer Science - Information Retrieval"
  - "Computer Science - Machine Learning"
  - "Computer Science - Social and Information Networks"
  - "notion"
collections:
  - "_ALL_CIT_140326/9401_ic_/PDFs"
zotero-key: "FPAZNNLK"
zotero-library: 1
zotero-uri: "zotero://select/library/items/FPAZNNLK"
date-added: "2026-03-14 17:40:02"
date-modified: "2026-03-25 21:28:25"
---

# Neural Graph Collaborative Filtering

**Wang, Xiang; He, Xiangnan; Wang, Meng; Feng, Fuli; Chua, Tat-Seng**

## Abstract

Learning vector representations (aka. embeddings) of users and items lies at the core of modern recommender systems. Ranging from early matrix factorization to recently emerged deep learning based methods, existing efforts typically obtain a user's (or an item's) embedding by mapping from pre-existing features that describe the user (or the item), such as ID and attributes. We argue that an inherent drawback of such methods is that, the collaborative signal, which is latent in user-item interactions, is not encoded in the embedding process. As such, the resultant embeddings may not be sufficient to capture the collaborative filtering effect. In this work, we propose to integrate the user-item interactions -- more specifically the bipartite graph structure -- into the embedding process. We develop a new recommendation framework Neural Graph Collaborative Filtering (NGCF), which exploits the user-item graph structure by propagating embeddings on it. This leads to the expressive modeling of high-order connectivity in user-item graph, effectively injecting the collaborative signal into the embedding process in an explicit manner. We conduct extensive experiments on three public benchmarks, demonstrating significant improvements over several state-of-the-art models like HOP-Rec and Collaborative Memory Network. Further analysis verifies the importance of embedding propagation for learning better user and item representations, justifying the rationality and effectiveness of NGCF. Codes are available at https://github.com/xiangwang1223/neural_graph_collaborative_filtering.

## Extra

arXiv:1905.08108 [cs]

## Notes

### Comment: SIGIR 2019; the latest version of NGCF paper, which is distinct from the version published in ACM Digital Libra

Comment: SIGIR 2019; the latest version of NGCF paper, which is distinct from the version published in ACM Digital Library

## Attachments

- [Notion](notion://www.notion.so/wangNeuralGraphCollaborative2019a-3239fa248c5781a6bbb0d4e427890f28)
- [Wang et al. - 2019 - Neural Graph Collaborative Filtering.pdf](../../attachments/SR/SRM2QWIP/Wang%20et%20al.%20-%202019%20-%20Neural%20Graph%20Collaborative%20Filtering.pdf)

---

[Open in Zotero](zotero://select/library/items/FPAZNNLK)
