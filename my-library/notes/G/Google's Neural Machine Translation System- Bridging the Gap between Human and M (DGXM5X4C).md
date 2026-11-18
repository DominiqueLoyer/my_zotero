---
title: "Google's Neural Machine Translation System: Bridging the Gap between Human and Machine Translation"
item-type: "preprint"
authors:
  - "Wu, Yonghui"
  - "Schuster, Mike"
  - "Chen, Zhifeng"
  - "Le, Quoc V."
  - "Norouzi, Mohammad"
  - "Macherey, Wolfgang"
  - "Krikun, Maxim"
  - "Cao, Yuan"
  - "Gao, Qin"
  - "Macherey, Klaus"
  - "Klingner, Jeff"
  - "Shah, Apurva"
  - "Johnson, Melvin"
  - "Liu, Xiaobing"
  - "Kaiser, Łukasz"
  - "Gouws, Stephan"
  - "Kato, Yoshikiyo"
  - "Kudo, Taku"
  - "Kazawa, Hideto"
  - "Stevens, Keith"
  - "Kurian, George"
  - "Patil, Nishant"
  - "Wang, Wei"
  - "Young, Cliff"
  - "Smith, Jason"
  - "Riesa, Jason"
  - "Rudnick, Alex"
  - "Vinyals, Oriol"
  - "Corrado, Greg"
  - "Hughes, Macduff"
  - "Dean, Jeffrey"
date: "2016-10-08"
year: "2016"
doi: "10.48550/arXiv.1609.08144"
url: "http://arxiv.org/abs/1609.08144"
tags:
  - "Computer Science - Artificial Intelligence"
  - "Computer Science - Computation and Language"
  - "Computer Science - Machine Learning"
  - "doi-fix:low-confidence"
  - "notion"
collections:
  - "_ALL_CIT_140326/NMT_en-ru_040326/PDFs"
zotero-key: "DGXM5X4C"
zotero-library: 1
zotero-uri: "zotero://select/library/items/DGXM5X4C"
date-added: "2026-03-14 17:36:09"
date-modified: "2026-11-18 01:45:36"
---

# Google's Neural Machine Translation System: Bridging the Gap between Human and Machine Translation

**Wu, Yonghui; Schuster, Mike; Chen, Zhifeng; Le, Quoc V.; Norouzi, Mohammad; Macherey, Wolfgang; Krikun, Maxim; Cao, Yuan; Gao, Qin; Macherey, Klaus; Klingner, Jeff; Shah, Apurva; Johnson, Melvin; Liu, Xiaobing; Kaiser, Łukasz; Gouws, Stephan; Kato, Yoshikiyo; Kudo, Taku; Kazawa, Hideto; Stevens, Keith; Kurian, George; Patil, Nishant; Wang, Wei; Young, Cliff; Smith, Jason; Riesa, Jason; Rudnick, Alex; Vinyals, Oriol; Corrado, Greg; Hughes, Macduff; Dean, Jeffrey**

## Abstract

Neural Machine Translation (NMT) is an end-to-end learning approach for automated translation, with the potential to overcome many of the weaknesses of conventional phrase-based translation systems. Unfortunately, NMT systems are known to be computationally expensive both in training and in translation inference. Also, most NMT systems have difficulty with rare words. These issues have hindered NMT's use in practical deployments and services, where both accuracy and speed are essential. In this work, we present GNMT, Google's Neural Machine Translation system, which attempts to address many of these issues. Our model consists of a deep LSTM network with 8 encoder and 8 decoder layers using attention and residual connections. To improve parallelism and therefore decrease training time, our attention mechanism connects the bottom layer of the decoder to the top layer of the encoder. To accelerate the final translation speed, we employ low-precision arithmetic during inference computations. To improve handling of rare words, we divide words into a limited set of common sub-word units ("wordpieces") for both input and output. This method provides a good balance between the flexibility of "character"-delimited models and the efficiency of "word"-delimited models, naturally handles translation of rare words, and ultimately improves the overall accuracy of the system. Our beam search technique employs a length-normalization procedure and uses a coverage penalty, which encourages generation of an output sentence that is most likely to cover all the words in the source sentence. On the WMT'14 English-to-French and English-to-German benchmarks, GNMT achieves competitive results to state-of-the-art. Using a human side-by-side evaluation on a set of isolated simple sentences, it reduces translation errors by an average of 60% compared to Google's phrase-based production system.

## Extra

arXiv:1609.08144 [cs]

## Attachments

- [Notion](https://app.notion.com/p/Wu-et-al-2016-4129fa248c57814f9014e89b236e034e)
- [Wu et al. - 2016 - Google's Neural Machine Translation System Bridging the Gap between Human and Machine Translation.pdf](../../attachments/VB/VBGII6KM/Wu%20et%20al.%20-%202016%20-%20Google's%20Neural%20Machine%20Translation%20System%20Bridging%20the%20Gap%20between%20Human%20and%20Machine%20Translation.pdf)

---

[Open in Zotero](zotero://select/library/items/DGXM5X4C)
