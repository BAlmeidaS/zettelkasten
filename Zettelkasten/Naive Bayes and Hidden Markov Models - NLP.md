---
tags:
  - Russel-n-Norvig-chap-23
---
[[Naive Bayes]] and [[Hidden Markov Model]] can be used on [[Natural Language Processing|NLP]] field as [[Generative Models]].

They lean a [[Joint Probability Distribution]], $\displaystyle \large \boldsymbol{P}(W,C)$, and we can generate a random sentence *by sampling from that probability distribution* to get a first word of the sentence, and then adding words one at a time.  