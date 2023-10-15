---
tags:
  - Russel-n-Norvig-chap-12
---
$$\Huge P(b \mid a) = \dfrac{P(a \mid b)*P(b)}{P(a)}$$

To remember this formula easier:
$\large P(b \mid a)$ is the [[Posterior]] and It is equal the [[Prior]] $\large P(b)$ times a *factor* of how much the evidence changes the prior.

$$\Huge \begin{eqnarray} 
posterior &=& factor \times prior \\
P(b \mid a) &=& factor \times P(b) \\
&=& \dfrac{P(a \mid b)}{P(a)} * P(b) \\
\end{eqnarray}$$

To be complete, the definition is that $\large P(a\mid b)$ is the **likelihood** and $\large P(B)$ is the **marginal**
$$\Huge \begin{eqnarray} 
posterior &=& \dfrac{likelehood}{marginal} \times prior \\
P(b \mid a) &=& \dfrac{P(a \mid b)}{P(a)} * P(b) \\
\end{eqnarray}$$

Bayes rules is derived from [[Conditional probability]]

---

The correct way to write in English is *Bayes' rule*