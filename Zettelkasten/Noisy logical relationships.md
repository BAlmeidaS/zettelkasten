---
tags:
  - Russel-n-Norvig-chap-13
---

Some relationships on [[Bayesian Network|Bayes Nets]] (especially involving binary random variables) can be modelled as *noisy logical operations*. Basically a node is a consequence of a logical operator of the result of its parents but with a some uncertainty (noisy) attached to the outcome

The most common example is **noisy-OR**, which represents the ability of each parent to cause the child to be true.

$$\displaystyle \Huge P(X_i \mid parents(X_i))=1-\prod_{j: X_k=true}q_j$$