---
title: "Detecting Brittle Decisions for Free: Leveraging Margin Consistency in Deep Robust Classifiers"
item-type: "preprint"
authors:
  - "Ngnawé, Jonas"
  - "Sahoo, Sabyasachi"
  - "Pequignot, Yann"
  - "Precioso, Frédéric"
  - "Gagné, Christian"
date: "2024-07-22"
year: "2024"
doi: "10.52202/079017-0733"
url: "http://arxiv.org/abs/2406.18451"
language: "en"
tags:
  - "Computer Science - Artificial Intelligence"
  - "Computer Science - Computer Vision and Pattern Recognition"
  - "Computer Science - Machine Learning"
  - "notion"
collections:
  - "Ma thèse"
  - "Ma thèse/Systematic review"
zotero-key: "92XNBDEJ"
zotero-library: 1
zotero-uri: "zotero://select/library/items/92XNBDEJ"
date-added: "2024-11-02 17:29:33"
date-modified: "2026-11-18 01:39:26"
---

# Detecting Brittle Decisions for Free: Leveraging Margin Consistency in Deep Robust Classifiers

**Ngnawé, Jonas; Sahoo, Sabyasachi; Pequignot, Yann; Precioso, Frédéric; Gagné, Christian**

## Abstract

Despite extensive research on adversarial training strategies to improve robustness, the decisions of even the most robust deep learning models can still be quite sensitive to imperceptible perturbations, creating serious risks when deploying them for high-stakes real-world applications. While detecting such cases may be critical, evaluating a model’s vulnerability at a per-instance level using adversarial attacks is computationally too intensive and unsuitable for real-time deployment scenarios. The input space margin is the exact score to detect non-robust samples and is intractable for deep neural networks. This paper introduces the concept of margin consistency – a property that links the input space margins and the logit margins in robust models – for efficient detection of vulnerable samples. First, we establish that margin consistency is a necessary and sufficient condition to use a model’s logit margin as a score for identifying non-robust samples. Next, through comprehensive empirical analysis of various robustly trained models on CIFAR10 and CIFAR100 datasets, we show that they indicate strong margin consistency with a strong correlation between their input space margins and the logit margins. Then, we show that we can effectively use the logit margin to confidently detect brittle decisions with such models and accurately estimate robust accuracy on an arbitrarily large test set by estimating the input margins only on a small subset. Finally, we address cases where the model is not sufficiently margin-consistent by learning a pseudo-margin from the feature representation. Our findings highlight the potential of leveraging deep representations to efficiently assess adversarial vulnerability in deployment scenarios.

## Extra

arXiv:2406.18451 [cs]

## Notes

### Comment: 11 pages, 7 figures, 2 tables, 1 algorithm. Version Update: Figure 6

Comment: 11 pages, 7 figures, 2 tables, 1 algorithm. Version Update: Figure 6

## Attachments

- [Notion](https://app.notion.com/p/Ngnaw-et-al-2024-4129fa248c5781dfbedbc7fb8edba386)
- [Ngnawé et al. - 2024 - Detecting Brittle Decisions for Free Leveraging Margin Consistency in Deep Robust Classifiers.pdf](../../attachments/WI/WIQ4MQQP/Ngnaw%C3%A9%20et%20al.%20-%202024%20-%20Detecting%20Brittle%20Decisions%20for%20Free%20Leveraging%20Margin%20Consistency%20in%20Deep%20Robust%20Classifiers.pdf)

---

[Open in Zotero](zotero://select/library/items/92XNBDEJ)
