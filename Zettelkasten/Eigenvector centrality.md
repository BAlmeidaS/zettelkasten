---
tags:
  - computer-science
---
Given a [[Graphs|Graph]] $\displaystyle \large G = (V, E)$, a **[[Vertices|vertice]] is important if surrounded by important neighbouring vertices**.

$$\displaystyle \Huge \begin{eqnarray} 
c_v = \dfrac{1}{\lambda} \sum_{t\in M(v)}c_t
\end{eqnarray}$$
*The importance of a node $\displaystyle \large v$ is the normalised sum of the importance of its neighbours*. $\displaystyle \large M(v)$ are the neighbours of $\displaystyle \large v$

Its called *eigenvector centrality* because it has the [[eigenvector]] property, considering $\displaystyle \large A$ as the [[Adjacency Matrix]]:
$$\displaystyle \Huge \begin{eqnarray} 
\lambda c=Ac
\end{eqnarray}$$

- $\displaystyle \large \lambda$ is the [[eigenvalue]], and it is a *positive constant* for a particular eigenvector.


There might be many eigenvalues associated with non-zero eigenvector solutions. But *we will consider only the [[eigenvector]] associated with the highest [[eigenvalue]]*, because this is guarantee to have all the entries non-negative (*Perron-Frobenius Theorem*).

- The largest [[eigenvalue]], $\displaystyle \large \lambda_\max$, is always positive and unique (*Perron-Frobenius Theorem*)
- The leading [[eigenvector]], $\displaystyle \large c_\max$ associated with $\displaystyle \large \lambda_\max$,  *is used for centrality of the [[Graphs|Graph]]*.

*the $\displaystyle \large v^{th}$ component of the $\displaystyle \large c_\max$ gives the relative centrality score of the vertex $\displaystyle \large v$ in the network

---

An interesting way to find the largest eigenvector is using an [[iteration]] approach:

1. **Initialization**: Start with a vector of ones (or any initial guess) and normalize it.
2. **Iteration**: Use the power iteration method to update the centrality vector iteratively.
3. **Normalization**: Normalize the vector in each iteration to ensure numerical stability.
4. **Convergence**: Continue iterations until the vector converges (i.e., changes between iterations are below a threshold).