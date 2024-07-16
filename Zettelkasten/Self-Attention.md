---
tags:
  - deep-learning
---
*Self-attention* was designed, originally, to deal with [[Natural Language Processing|NLP]]. The idea is to [[Representation Learning|learn a representation]] for each word in the input sentence, this representation will take into account all the other words, for the same step the representations might be computed in parallel (which means that there is no the concept of sequence as in [[Attention method]])

Each word will have calculate an *attention-based representation* described as $\displaystyle \large A(Q, K, V)$ using [[softmax function|softmax]] and [[dot product]]:
$$\displaystyle \Huge \begin{eqnarray} 
A(Q, K, V) = \sum_i\dfrac{e^{q\cdot k_i}}{\sum\limits_j e^{q\cdot k_j}}*v_i
\end{eqnarray}$$
- $\displaystyle \large Q$: Query - *asks a question about the word that you are learning the representation*
- $\displaystyle \large K$: Key - *shows among the **other words** the ones that have good fit to the query*
- $\displaystyle \large V$: Value - *brings the value from the other words to that word that your are learning the presentation*

Each one of these letters, have a *matrix associated that will be learned*, $\displaystyle \large W^Q, W^K, W^V$,
$$\displaystyle \Huge \begin{eqnarray} 
head &=& Attention(
QW^Q, KW^K, VW^V)
\\[5pt]
W^Q &\in& \mathbb{R}^{\displaystyle d_{model} \times d_k}
\\[5pt]
W^K &\in& \mathbb{R}^{\displaystyle d_{model} \times d_k}
\\[5pt]
W^V &\in& \mathbb{R}^{\displaystyle d_{model} \times d_v}
\end{eqnarray}$$

*Usually $\displaystyle \large d_k = d_v$ but they might be different!*

![[Pasted image 20240716170515.png]]


The [[Attention is all you need|paper]] defines $\displaystyle \large A$ with another term, a normalisation term, to avoid the dot product to explode, $\displaystyle \large d_k$, and so they called *Scaled dot-product attention*
- $\displaystyle \large d_k$: the dimension of the key (which is the same of the queries)
$$\displaystyle \Huge \begin{eqnarray} 
A(Q, K, V) = softmax\left(\dfrac{Q\cdot K^T}{\sqrt{d_k}}\right)*V
\end{eqnarray}$$

![[Pasted image 20240716154601.png|300]]