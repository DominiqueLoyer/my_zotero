---
title: "On Fake News Detection with LLM Enhanced Semantics Mining"
item-type: "conferencePaper"
authors:
  - "Ma, Xiaoxiao"
  - "Zhang, Yuchen"
  - "Ding, Kaize"
  - "Yang, Jian"
  - "Wu, Jia"
  - "Fan, Hao"
  - "Al-Onaizan, Yaser"
  - "Bansal, Mohit"
  - "Chen, Yun-Nung"
date: "2024-11"
year: "2024"
publication: "Proceedings of the 2024 Conference on Empirical Methods in Natural Language Processing"
publisher: "Association for Computational Linguistics"
pages: "508–521"
doi: "10.18653/v1/2024.emnlp-main.31"
url: "https://aclanthology.org/2024.emnlp-main.31/"
tags:
  - "notion"
collections:
  - "Cours H25/Traitement naturel des langues"
  - "Ma thèse/Systematic review/fake-news"
zotero-key: "ZFK9K9E5"
zotero-library: 1
zotero-uri: "zotero://select/library/items/ZFK9K9E5"
date-added: "2025-03-05 19:28:48"
date-modified: "2025-12-05 22:29:21"
---

# On Fake News Detection with LLM Enhanced Semantics Mining

**Ma, Xiaoxiao; Zhang, Yuchen; Ding, Kaize; Yang, Jian; Wu, Jia; Fan, Hao; Al-Onaizan, Yaser; Bansal, Mohit; Chen, Yun-Nung**

## Abstract

Large language models (LLMs) have emerged as valuable tools for enhancing textual features in various text-related tasks. Despite their superiority in capturing the lexical semantics between tokens for text analysis, our preliminary study on two popular LLMs, i.e., ChatGPT and Llama2, showcases that simply applying the news embeddings from LLMs is ineffective for fake news detection. Such embeddings only encapsulate the language styles between tokens. Meanwhile, the high-level semantics among named entities and topics, which reveal the deviating patterns of fake news, have been ignored. Therefore, we propose a topic model together with a set of specially designed prompts to extract topics and real entities from LLMs and model the relations among news, entities, and topics as a heterogeneous graph to facilitate investigating news semantics. We then propose a Generalized Page-Rank model and a consistent learning criteria for mining the local and global semantics centered on each news piece through the adaptive propagation of features across the graph. Our model shows superior performance on five benchmark datasets over seven baseline methods and the efficacy of the key ingredients has been thoroughly validated.

## Attachments

- [Ma et al. - 2024 - On Fake News Detection with LLM Enhanced Semantics Mining.pdf](../../attachments/J9/J9WA64XS/Ma%20et%20al.%20-%202024%20-%20On%20Fake%20News%20Detection%20with%20LLM%20Enhanced%20Semantics%20Mining.pdf)
- [Notion](notion://www.notion.so/maFakeNewsDetection2024-2c09fa248c5781809656fb2e8d3ad09f)

---

[Open in Zotero](zotero://select/library/items/ZFK9K9E5)
