---
tags:
  - machine-learning
aliases:
  - cross-entropy loss
---
*Cross-entropy* quantify **the difference between two probabilities distributions**, $\displaystyle \large p(x)$ and $\displaystyle \large q(x)$. 

The cross-entropy of a distribution $\displaystyle \large q$ relative to a distribution $\displaystyle \large p$ is:
$$\displaystyle \Huge \begin{eqnarray} 
H(p, q) &=& -\sum_{x \in Data}p(x)\log q(x)\\
\end{eqnarray}$$


The definition might be formulated using [[Kullback–Leibler divergence|kl divergence]]:
$$\displaystyle \Huge \begin{eqnarray} 
D_{KL}(P\parallel Q) &=& \sum_{x}P(x)\log\dfrac{P(x)}{Q(x)} \\
&=& \sum_{x}P(x)\log P(x) - \sum_{x}P(x)\log Q(x) \\
\end{eqnarray}$$
Here you must remember of [[Entropy]] to reduce the first term to $\displaystyle \large -H(p)$
$$\displaystyle \Huge \begin{eqnarray} 
&D_{KL}(P\parallel Q) = -H(P) - \sum_{x}P(x)\log Q(x) \\
&\text{(rearranging the terms...)} \\\\
&-\sum_{x}P(x)\log Q(x) = H(P) + D_{KL}(P\parallel Q) \\
&H(P,Q) = H(P) + D_{KL}(P\parallel Q) \\
\end{eqnarray}$$

