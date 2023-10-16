---
tags:
  - Russel-n-Norvig-chap-13
---
Important property from [[Bayesian Network|Bayes Net]]. It aims to compact the probability calculation of each random variable reducing the chain of condition probabilities that each one has.

Markov blanket states that everything besides the area (blanket) of the children's node, the parent's node and the other parents from the children's node are [[Conditional Independence|conditional independent]]

In other words, in order to calculate the probability of a random variable in a bayes net (node from the network) we need only the markov blanket of that node as condition:
$$\displaystyle \Huge \begin{eqnarray} 
P(X_k \mid Parents(X_k)) &=& P(X_k\mid MarkovBlanket(X_k)) \\
\\
\end{eqnarray}$$
$$\displaystyle \Huge \begin{eqnarray} 
MB(X_k) &=& MarkovBlanket(X_k) \\
MB(X_k) &=& DirectParents(X_k) \\
& & \land Children(X_k) \\
& & \land OtherParents(Children(X_k)
\end{eqnarray}$$

![[Pasted image 20231016165221.png|400]]
*markov blanket in gray*