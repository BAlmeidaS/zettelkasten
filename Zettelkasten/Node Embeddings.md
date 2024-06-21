---
tags:
  - deep-learning
aliases:
  - encode decode approach
---
*Nodes embedding* are a type of [[embedding]] for [[Vertices|Nodes]] in a [[Graphs|Graph]]. The idea is defining a function $\displaystyle \large f$ that maps the node $\displaystyle \large u$ to its embedding representation $\displaystyle \large z_u$:
$$\displaystyle \Huge \begin{eqnarray} 
f: node \rightarrow \mathbb{R}^d
\end{eqnarray}$$

Important to say that they will not use any labels or features from the nodes, thus such models will not be trained for a specific task but can be used to many downstream tasks.

A way to define this function is using the framework *encoding and decoding graphs*. This will be reduce the *Graph [[Representation Learning]]* into two operations:
- [[Encoder - Node Embedding]]
- [[Decoder - Node Embedding]]

![[Pasted image 20240621183208.png|600]]

*Applying the pairwise decoder to a pair of embeddings $\displaystyle \large (z_u, z_v)$ results in the reconstruction of the relationship between nodes $\displaystyle \large u$ and $\displaystyle \large v$. The goal is optimise the encoder and decoder to minimise the reconstruction loss* 
$$\displaystyle \Huge \begin{eqnarray} 
DEC(ENC(u), ENC(v)) = DEC(z_u, z_v) \approx Similarity[u, v]
\end{eqnarray}$$

Thus, we can define a [[loss function]]:
$$\displaystyle \Huge \begin{eqnarray} 
L = \sum_{(u, v) \in V} l(DEC(z_u, z_v), S[u,v])
\end{eqnarray}$$
$\displaystyle \large V$: is the the set of [[Vertices]]
$\displaystyle \large l$: is a function that measures the difference between this two numbers, it might be [[Mean squared Error|MSE]] but it also be [[Cross-entropy]]. It depends on the definition of $\displaystyle \large DEC$ and $\displaystyle \large Similarity$.


