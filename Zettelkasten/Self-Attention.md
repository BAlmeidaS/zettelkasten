---
tags:
  - deep-learning
---
*Self-attention* was designed, originally, to deal with [[Natural Language Processing|NLP]]. The idea is to [[Representation Learning|learn a representation]] for each word in the input sentence, this representation will take into account all the other words, for the same step the representations might be computed in parallel (which means that there is no the concept of sequence as in [[Attention method]])

Each word will have calculate an *attention-based representation* described as $\displaystyle \large A(q, K, V)$:
$$\displaystyle \Huge \begin{eqnarray} 
A(q, K, V) = \sum_i\dfrac{e^{q*k_i}}{\sum\limits_je^}
\end{eqnarray}$$
