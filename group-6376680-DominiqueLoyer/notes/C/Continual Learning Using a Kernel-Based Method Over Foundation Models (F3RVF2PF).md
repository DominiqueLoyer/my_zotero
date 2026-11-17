---
title: "Continual Learning Using a Kernel-Based Method Over Foundation Models"
item-type: "preprint"
authors:
  - "Momeni, Saleh"
  - "Mazumder, Sahisnu"
  - "Liu, Bing"
date: "2024-12-20"
year: "2024"
doi: "10.48550/arXiv.2412.15571"
url: "http://arxiv.org/abs/2412.15571"
language: "en"
tags:
  - "Computer Science - Artificial Intelligence"
  - "Computer Science - Computation and Language"
  - "Computer Science - Computer Vision and Pattern Recognition"
  - "Computer Science - Machine Learning"
  - "notion"
collections:
  - "_ALL_CIT_140326/2eTP_dic9335_040326/AVEC SOURCES CUSTOM/PDFs"
zotero-key: "F3RVF2PF"
zotero-library: 2
zotero-uri: "zotero://select/groups/6376680/items/F3RVF2PF"
date-added: "2026-04-17 21:22:52"
date-modified: "2026-04-17 21:22:52"
---

# Continual Learning Using a Kernel-Based Method Over Foundation Models

**Momeni, Saleh; Mazumder, Sahisnu; Liu, Bing**

## Abstract

Continual learning (CL) learns a sequence of tasks incrementally. This paper studies the challenging CL setting of class-incremental learning (CIL). CIL has two key challenges: catastrophic forgetting (CF) and inter-task class separation (ICS). Despite numerous proposed methods, these issues remain persistent obstacles. This paper proposes a novel CIL method, called Kernel Linear Discriminant Analysis (KLDA), that can effectively avoid CF and ICS problems. It leverages only the powerful features learned in a foundation model (FM). However, directly using these features proves suboptimal. To address this, KLDA incorporates the Radial Basis Function (RBF) kernel and its Random Fourier Features (RFF) to enhance the feature representations from the FM, leading to improved performance. When a new task arrives, KLDA computes only the mean for each class in the task and updates a shared covariance matrix for all learned classes based on the kernelized features. Classification is performed using Linear Discriminant Analysis. Our empirical evaluation using text and image classification datasets demonstrates that KLDA significantly outperforms baselines. Remarkably, without relying on replay data, KLDA achieves accuracy comparable to joint training of all classes, which is considered the upper bound for CIL performance. The KLDA code is available at https://github.com/salehmomeni/klda.

## Extra

arXiv:2412.15571 [cs]

## Attachments

- [Notion](notion://www.notion.so/momeniContinualLearningUsing2024a-3239fa248c5781cf8ef4c4993eaed98e)

---

[Open in Zotero](zotero://select/groups/6376680/items/F3RVF2PF)
