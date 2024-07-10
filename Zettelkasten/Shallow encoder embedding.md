---
tags:
  - computer-science
---
This type of [[Node Embeddings|encoder for node embeddings]] defines a *lookup matrix*, with size $\displaystyle \large (\text{number of nodes} \times dim(embedding))$.

So basically each [[Vertices|Node]] *represented as columns* will have an specific [[embedding]] *represented as rows*.

Being $\displaystyle \large o_u$ the original space representation and $\displaystyle \large e_u$ the embedding space representation:
$$\displaystyle \Huge \begin{eqnarray} 
e_w = E*o_w
\end{eqnarray}$$
Being $\displaystyle \large E$ the lookup matrix (or the function the maps from one space to the other)

what [[Node Embeddings|encode decode approach]] will do is finding these cells parameters.
