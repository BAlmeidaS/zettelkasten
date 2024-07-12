---
aliases:
  - GloVe
---
GloVe is a method to produce *word embeddings*.

Glove starts defining $\displaystyle \large X_{ij}$ which is *the number of times that $\displaystyle \large i$ appears in the context of $\displaystyle \large j$*. Thus, there is an $\displaystyle \large X_{ij}$ associated to every pair of words.

>[!note]
>if by "context" we define a word that is before another, so $\displaystyle \large X_{ij} \ne X_{ji}$.
>If by "context" we define as words around another, so the definition is symmetric and  $\displaystyle \large X_{ij} = X_{ji}$.

*GloVe is a count-based approach! not a deep learning as [[Word2Vec]]*.

The Idea is building this matrix $\displaystyle \large X$ in a way that this relation is minimised:
$$\displaystyle \Huge \begin{eqnarray} 
\min 
\sum^{vocab}_{i=1}
\sum^{vocab}_{j=1}
weight(X_{ij})(\theta^T_i e_j + b_i + b_j- log X_{ij})^2
\end{eqnarray}$$
- $\displaystyle \large weight$ is a function that gives more or less weight to some words
- $\displaystyle \large b$ are the bias terms
