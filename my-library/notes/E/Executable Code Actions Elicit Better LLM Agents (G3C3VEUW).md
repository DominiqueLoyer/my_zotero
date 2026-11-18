---
title: "Executable Code Actions Elicit Better LLM Agents"
item-type: "preprint"
authors:
  - "Wang, Xingyao"
  - "Chen, Yangyi"
  - "Yuan, Lifan"
  - "Zhang, Yizhe"
  - "Li, Yunzhu"
  - "Peng, Hao"
  - "Ji, Heng"
date: "2024-06-07"
year: "2024"
doi: "10.48550/arXiv.2402.01030"
url: "http://arxiv.org/abs/2402.01030"
tags:
  - "Computer Science - Artificial Intelligence"
  - "Computer Science - Computation and Language"
  - "doi-fix:low-confidence"
  - "notion"
collections:
  - "_ALL_CIT_140326/9401_ic_/PDFs"
zotero-key: "G3C3VEUW"
zotero-library: 1
zotero-uri: "zotero://select/library/items/G3C3VEUW"
date-added: "2026-03-14 17:40:05"
date-modified: "2026-11-18 01:44:21"
---

# Executable Code Actions Elicit Better LLM Agents

**Wang, Xingyao; Chen, Yangyi; Yuan, Lifan; Zhang, Yizhe; Li, Yunzhu; Peng, Hao; Ji, Heng**

## Abstract

Large Language Model (LLM) agents, capable of performing a broad range of actions, such as invoking tools and controlling robots, show great potential in tackling real-world challenges. LLM agents are typically prompted to produce actions by generating JSON or text in a pre-defined format, which is usually limited by constrained action space (e.g., the scope of pre-defined tools) and restricted flexibility (e.g., inability to compose multiple tools). This work proposes to use executable Python code to consolidate LLM agents' actions into a unified action space (CodeAct). Integrated with a Python interpreter, CodeAct can execute code actions and dynamically revise prior actions or emit new actions upon new observations through multi-turn interactions. Our extensive analysis of 17 LLMs on API-Bank and a newly curated benchmark shows that CodeAct outperforms widely used alternatives (up to 20% higher success rate). The encouraging performance of CodeAct motivates us to build an open-source LLM agent that interacts with environments by executing interpretable code and collaborates with users using natural language. To this end, we collect an instruction-tuning dataset CodeActInstruct that consists of 7k multi-turn interactions using CodeAct. We show that it can be used with existing data to improve models in agent-oriented tasks without compromising their general capability. CodeActAgent, finetuned from Llama2 and Mistral, is integrated with Python interpreter and uniquely tailored to perform sophisticated tasks (e.g., model training) using existing libraries and autonomously self-debug.

## Extra

arXiv:2402.01030 [cs]

## Notes

### Comment: Accepted by ICML 2024; Code, data, model, and demo are available at https://github.com/xingyaoww/code-act

Comment: Accepted by ICML 2024; Code, data, model, and demo are available at https://github.com/xingyaoww/code-act

## Attachments

- [Notion](https://app.notion.com/p/Wang-et-al-2024-4129fa248c5781a085b5f7d6901c831d)
- [Wang et al. - 2024 - Executable Code Actions Elicit Better LLM Agents.pdf](../../attachments/XR/XRXKJ2YY/Wang%20et%20al.%20-%202024%20-%20Executable%20Code%20Actions%20Elicit%20Better%20LLM%20Agents.pdf)

---

[Open in Zotero](zotero://select/library/items/G3C3VEUW)
