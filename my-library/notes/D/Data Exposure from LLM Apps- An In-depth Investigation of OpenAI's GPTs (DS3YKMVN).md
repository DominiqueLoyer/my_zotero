---
title: "Data Exposure from LLM Apps: An In-depth Investigation of OpenAI's GPTs"
item-type: "preprint"
authors:
  - "Jaff, Evin"
  - "Wu, Yuhao"
  - "Zhang, Ning"
  - "Iqbal, Umar"
date: "2024-08-23"
year: "2024"
url: "http://arxiv.org/abs/2408.13247"
language: "en"
tags:
  - "Computer Science - Artificial Intelligence"
  - "Computer Science - Computation and Language"
  - "Computer Science - Computers and Society"
  - "Computer Science - Cryptography and Security"
  - "Computer Science - Machine Learning"
  - "doi-fix:low-confidence"
  - "notion"
collections:
  - "Ma thèse"
  - "Ma thèse/Littérature donnée par Daniel"
  - "Ma thèse/Systematic review"
  - "Ma thèse/Systematic review/LLMs"
zotero-key: "DS3YKMVN"
zotero-library: 1
zotero-uri: "zotero://select/library/items/DS3YKMVN"
date-added: "2024-11-02 18:24:35"
date-modified: "2026-11-13 19:35:30"
---

# Data Exposure from LLM Apps: An In-depth Investigation of OpenAI's GPTs

**Jaff, Evin; Wu, Yuhao; Zhang, Ning; Iqbal, Umar**

## Abstract

LLM app ecosystems are quickly maturing and supporting a wide range of use cases, which requires them to collect excessive user data. Given that the LLM apps are developed by third-parties and that anecdotal evidence suggests LLM platforms currently do not strictly enforce their policies, user data shared with arbitrary third-parties poses a significant privacy risk. In this paper we aim to bring transparency in data practices of LLM apps. As a case study, we study OpenAI’s GPT app ecosystem. We develop an LLM-based framework to conduct the static analysis of natural language-based source code of GPTs and their Actions (external services) to characterize their data collection practices. Our findings indicate that Actions collect expansive data about users, including sensitive information prohibited by OpenAI, such as passwords. We find that some Actions, including related to advertising and analytics, are embedded in multiple GPTs, which allow them to track user activities across GPTs. Additionally, co-occurrence of Actions exposes as much as 9.5× more data to them, than it is exposed to individual Actions. Lastly, we develop an LLM-based privacy policy analysis framework to automatically check the consistency of data collection by Actions with disclosures in their privacy policies. Our measurements indicate that the disclosures for most of the collected data types are omitted in privacy policies, with only 5.8% of Actions clearly disclosing their data collection practices.

## Extra

arXiv:2408.13247 [cs]

## Attachments

- [Notion](https://app.notion.com/p/Jaff-et-al-2024-4129fa248c5781ee8869c944731aef62)
- [Jaff et al. - 2024 - Data Exposure from LLM Apps An In-depth Investigation of OpenAI's GPTs.pdf](../../attachments/UA/UAPWRX4K/Jaff%20et%20al.%20-%202024%20-%20Data%20Exposure%20from%20LLM%20Apps%20An%20In-depth%20Investigation%20of%20OpenAI's%20GPTs.pdf)
- [2408.html](../../attachments/XB/XBTAESLG/2408.html)

---

[Open in Zotero](zotero://select/library/items/DS3YKMVN)
