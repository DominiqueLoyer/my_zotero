---
title: "A few useful things to know about machine learning"
item-type: "journalArticle"
authors:
  - "Domingos, Pedro"
date: "10/2012"
year: "2012"
publication: "Communications of the ACM"
volume: "55"
issue: "10"
pages: "78-87"
doi: "10.1145/2347736.2347755"
issn: "0001-0782, 1557-7317"
url: "https://dl.acm.org/doi/10.1145/2347736.2347755"
language: "en"
tags:
  - "notion"
collections:
  - "Cours H25/Modélisation/2e lecture à résumer"
  - "Examen doctoral 9401(été25)"
  - "Examen doctoral 9401(été25)/littératures"
  - "GS_301225.bibtex"
zotero-key: "57DT53SS"
zotero-library: 1
zotero-uri: "zotero://select/library/items/57DT53SS"
date-added: "2025-04-03 14:41:49"
date-modified: "2026-11-09 15:05:50"
---

# A few useful things to know about machine learning

**Domingos, Pedro**

## Abstract

Machine learning algorithms can ﬁgure out how to perform important tasks by generalizing from examples. This is often feasible and cost-eﬀective where manual programming is not. As more data becomes available, more ambitious problems can be tackled. As a result, machine learning is widely used in computer science and other ﬁelds. However, developing successful machine learning applications requires a substantial amount of “black art” that is hard to ﬁnd in textbooks. This article summarizes twelve key lessons that machine learning researchers and practitioners have learned. These include pitfalls to avoid, important issues to focus on, and answers to common questions.

## Attachments

- [Notion](https://app.notion.com/p/Domingos-2012-4129fa248c57816f86e7e4effa5aab22)
- Domingos - 2012 - A few useful things to know about machine learning.pdf _(file not in repository: missing)_
- Domingos - 2012 - A few useful things to know about machine learning.pdf _(file not in repository: missing)_
- Domingos - 2012 - A few useful things to know about machine learning.pdf _(file not in repository: missing)_
- [Domingos - 2012 - A few useful things to know about machine learning.pdf](../../attachments/I6/I6W6Z8WJ/Domingos%20-%202012%20-%20A%20few%20useful%20things%20to%20know%20about%20machine%20learning.pdf)

## Annotations

- **p. 1, highlight** “generalizing from examples”
- **p. 1, highlight** ““black art”
- **p. 1, highlight** “d placement, credit scoring, fraud detection, stock trading, drug design, and many other applications”
- **p. 1, highlight** “folk knowledge”
- **p. 1, highlight** “A classifier is a system that inputs (typically) a vector of discrete and/or continuous feature values and outputs a single discrete value, the class.”
- **p. 1, highlight** “The first problem facing you is the bewildering variety of learning algorithms available. Which one to use?”
- **p. 1, highlight** “There are literally thousands available, and hundreds more are published each year.”
- **p. 1, highlight** “A classifier must be represented in some formal language that the computer can handl”
- **p. 1, highlight** “An evaluation function (also called objective function or scoring function) is needed to distinguish good classifiers from bad ones.”
- **p. 1, highlight** “Finally, we need a method to search among the classifiers in the language for the highest-scoring one”
- **p. 1, highlight** “The choice of optimization technique is key to the efficiency of the learner, and also helps determine the classifier produced if the evaluation function has more than one optimum.”
- **p. 1, highlight** “k-nearest neighbor classifies”
- **p. 1, highlight** “k most similar training examples and predicting the majority class among them”
- **p. 1, highlight** “Hyperplanebased methods form a linear combination of the features per class and predict the class with the highest-valued combination.”
- **p. 1, highlight** “Decision trees test one feature at each internal node,”
- **p. 2, highlight** “with one branch for each feature value, and have class predictions at the leaves.”
- **p. 2, highlight** “The fundamental goal of machine learning is to generalize beyond the examples in the training set.”
- **p. 2, highlight** “Contamination of your classifier by test data can occur in insidious ways, e.g.,”
- **p. 2, highlight** “Of course, holding out data reduces the amount available for training. This can be mitigated by doing cross-validation”
- **p. 2, highlight** “n the early days of machine learning, the need to keep training and test data separate was not widely appreciated”
- **p. 2, highlight** “Notice that generalization being the goal has an interesting consequence for machine learning. Unlike in most other optimization problems, we don’t have access to the function we want to optimize!”
- **p. 2, highlight** “We have to use training error as a surrogate for test error, and this is fraught with danger.”
- **p. 2, highlight** “since the objective function is only a proxy for the true goal, we may not need to fully optimize it; in fact, a local optimum returned by simple greedy search may be better than the global optimum.”
- **p. 3, highlight** “Ge”
- **p. 3, highlight** “eneralization being the goal has another major consequence: data alone is not enough, no matter how much of it you have.”
- **p. 3, highlight** “Consider learning a Boolean function of (say) 100 variables from a million examples. There are 2100 − 106 examples whose classes you don’t know”
- **p. 3, highlight** “the philosopher David Hume over 200 years ago”
- **p. 3, highlight** “What if the knowledge and data we have are not sufficient to completely determine the correct classifier?”
- **p. 3, highlight** “Th”
- **p. 3, highlight** “hen we run the risk of just hallucinating a classifier (or parts of it) that is not grounded in reality”
- **p. 3, highlight** “This problem is called overfitting, and is the bugbear of machine learning.”
- **p. 3, highlight** “When your learner outputs a classifier that is 100% accurate on the training data but only 50% accurate on test data, when in fact it could have output one that is 75% accurate on both, it has overfit”
- **p. 3, highlight** “One way to understand overfitting is by decomposing generalization error into bias and variance [9]”
- **p. 3, highlight** “Bias is a learner’s tendency to consistently learn the same wrong thing. Variance is the tendency to learn random things irrespective of the real signal”
- **p. 3, highlight** “A linear learner has high bias, because when the frontier between two classes is not a hyperplane the learner is unable to induce it”
- **p. 3, highlight** “Decision trees don’t have this problem because they can represent any Boolean function, but on the other hand they can suffer from high variance:”
- **p. 3, highlight** “decision trees learned on different training sets generated by the same phenomenon are often very different, when in fact they should be the same”
- **p. 3, highlight** “Thus, contrary to intuition, a more powerful learner is not necessarily better than a less powerful one.”
- **p. 4, highlight** “Cross-validation can help to combat overfitting, for example by using it to choose the best size of decision tree to learn.”
- **p. 4, highlight** “Besides cross-validation, there are many methods to combat overfitting.”
- **p. 4, highlight** “The most popular one is adding a regularization term to the evaluation function.”
- **p. 4, highlight** “This can, for example, penalize classifiers with more structure, thereby favoring smaller ones with less room to overfit”
- **p. 4, highlight** “Another option is to perform a statistical significance test like chi-square before adding new structure,”
- **p. 4, highlight** “After overfitting, the biggest problem in machine learning is the curse of dimensionality.”
- **p. 4, highlight** “This expression was coined by Bellman in 1961 to refer to the fact that many algorithms that work fine in low dimensions become intractable when the input is high-dimensional.”

---

[Open in Zotero](zotero://select/library/items/57DT53SS)
