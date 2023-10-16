---
tags:
  - Russel-n-Norvig-chap-13
aliases:
  - CPT
---
Only used to discrete [[Random Variable]]s. Each row contains the conditional probability of each node value for a *conditional case*. Each row sums 1, which means that when is a boolean variable we omit one of the cases - $\displaystyle \large \{p, 1-p\}$.

A table with boolean parents has $\displaystyle \large 2^k$ independent probabilities.

An example of a [[Bayesian Network]] with each node with its CPT
![[Pasted image 20231016015522.png|500]]
