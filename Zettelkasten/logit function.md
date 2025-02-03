---
tags:
  - Statistics
aliases:
  - logits
---
The logit function is the inverse of the [[logistic regression|logistic function]]. It is useful because *maps probabilities (range $\displaystyle \large [0, 1]$) to real numbers range $\displaystyle \large [- \infty, \infty]$*.

#### Binary classification

Being $\displaystyle \large p$ the probability of success / *binary classification*:
$$\displaystyle \Huge \begin{eqnarray} 
logit(p) &=& log\left(\dfrac{p}{1-p}\right) \\
&=& \beta_0 + \beta_1x_1 + \dots + \beta_kx_k
\end{eqnarray}$$

Thus, in this case,  *logit function* is in the the same of [[Log Odds]].  It is the [[linear combination]] *of the features with the weights*.

A way to understand using [[logistic regression]] is that:
$$\displaystyle \Huge \begin{eqnarray} 
p = \dfrac{1}{1+e^{-logit}}
\end{eqnarray}$$

#### Multi-class classification

In the *multi-class classification*, we have *one logit for each class* $\displaystyle \large k$:
$$\displaystyle \Huge \begin{eqnarray} 
logit_k(x) = z_k = w_k^Tx
\end{eqnarray}$$
So we end-up with a *vector of logits*, one for each class!

These logits are passed through a [[softmax function]] to obtaing the class probabilities.

---

>[!important] What are logits?
>**Logits are numbers that represent raw scores for each class before being converted into probabilities. Higher logits indicate a higher likelihood of a class, but they are not probabilities themselves.**
