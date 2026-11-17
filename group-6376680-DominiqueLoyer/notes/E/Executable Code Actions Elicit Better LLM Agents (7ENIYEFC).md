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
  - "notion"
collections:
  - "_ALL_CIT_140326/9401_ic_/PDFs"
zotero-key: "7ENIYEFC"
zotero-library: 2
zotero-uri: "zotero://select/groups/6376680/items/7ENIYEFC"
date-added: "2026-04-17 21:22:52"
date-modified: "2026-04-17 21:22:52"
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

- [Notion](notion://www.notion.so/wangExecutableCodeActions2024-3239fa248c57819e984ae57f58f5e33b)

---

[Open in Zotero](zotero://select/groups/6376680/items/7ENIYEFC)
