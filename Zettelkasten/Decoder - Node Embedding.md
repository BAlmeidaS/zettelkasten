---
tags:
  - machine-learning
aliases:
  - decoder
---
The idea of the *decoder* in [[Node Embeddings]] is to *reconstruct graph characteristics*. The most common way is defining pairwise function:
$$\displaystyle \Huge \begin{eqnarray} 
DEC:
\mathbb{R}^d
\times
\mathbb{R}^d
\rightarrow
\mathbb{R}^+
\end{eqnarray}$$
- two embedding that map to a positive number, and this number might be understood as [[Similarity function|similarity]] of both nodes.

So we must define:
1. what is the function $\displaystyle \large DEC$
2. what will be the [[Similarity function|similarity]] definition used

*Applying the pairwise decoder to a pair of embeddings $\displaystyle \large (z_u, z_v)$ results in the reconstruction of the relationship between nodes $\displaystyle \large u$ and $\displaystyle \large v$. The goal is optimise the encoder and decoder to minimise the reconstruction loss* 
$$\displaystyle \Huge \begin{eqnarray} 
DEC(ENC(u), ENC(v)) = DEC(z_u, z_v) \approx Similarity[u, v]
\end{eqnarray}$$