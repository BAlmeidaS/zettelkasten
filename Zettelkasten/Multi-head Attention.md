---
tags:
  - deep-learning
---
The main concept here is, each running of a [[Self-Attention]] is considered *one head*, so, if we run multiple times we have a *multi-head*.

Instead of having only one set of $\displaystyle \large W^Q, W^K, \text{and } W^V$, there will be $\displaystyle \large h$ sets (for $\displaystyle \large h$ heads):
$$\displaystyle \Huge \begin{eqnarray} 
W^Q_i, W^K_i, W^V_i, i \in [1, h]
\end{eqnarray}$$

So we will compute n times the [[Self-Attention]], and for each word we will end-up with *n different self-attention mechanism*.

However, a new matrix $\displaystyle \large W^O$ is added, this is the weights to be learned about how to put all together this representations.
$$\displaystyle \Huge \begin{eqnarray} 
MultiHead(Q,K,V) &=& concat(head_1, head_2, \dots, head_h) \cdot W^O
\\[5pt]
head_i &=& Attention(W_i^Q Q, W_i^K K, W_i^V V)
\end{eqnarray}$$

![[Pasted image 20240716173750.png]]
