---
tags:
  - Russel-n-Norvig-chap-13
aliases:
  - Bayes Net
---
Shows the dependencies among [[Random Variable]]s. The ideia is to come up with a connection that makes sense for you on the problem - [[Bayes Net preferably with causal models]] - in order to be more compact - [[Bayes Net - Compactness]]

**Must be** a [[DAG - Directed Acyclic Graph]], with such properties:
1. Each node is a [[Random Variable]]
2. A link from X to Y shows that X is *parent* of Y
3. Each node $\displaystyle \large X_i$ has a probability info $\displaystyle \large \theta(X_i\mid Parents(X_i))$ - *Parents have a direct influence on Children*
![[Pasted image 20231016014023.png|600]]
$$\displaystyle \Huge \begin{eqnarray} 
P(x_1, \dots,x_n) 
&=& \prod^n_{i=1}P(x_i\mid parents(X_i)) \\
\end{eqnarray}$$

Each variable is [[Conditional Independence|Conditionally Independent]] of it its non-descendants given its parents


[[Chain Rule for Bayesian Networks]]
[[Calculating probability using bayes net and CPT]]