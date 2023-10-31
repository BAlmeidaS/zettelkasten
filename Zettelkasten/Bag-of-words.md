---
tags:
  - Russel-n-Norvig-chap-23
---
Considering [[Natural Language Processing|NLP]], the application of [[Naive Bayes]] to string of words is called *Bag-of-words* model. A **generative model** that describes a process for generating a sentence.

Given a sentence consisting of the words $\displaystyle \large w_1, w_2, \dots, w_N$ or $\displaystyle \large w_{1:N}$, we have:

$$\displaystyle \Huge P(Class\mid W_{1:N}) = \alpha P(Class)\prod_jP(w_j \mid Class)$$

For each $\displaystyle \large Class$ (business, weather, ...) we have a *bag of full words*.

*To generate a text, first select one of the bags (based on the Class) and discard the others. Take a word randomly, it will be the first word of the sequence. Put it back on the back and repeat the process until you get an **end-of-sentence** indicator*