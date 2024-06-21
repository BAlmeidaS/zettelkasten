---
tags:
  - math
aliases:
  - number of paths between two nodes in a graph
---
Powers of [[Adjacency Matrix]] are useful to calculate *the number of paths between a pair of nodes*. 

More precisely:
- The matrix $\displaystyle \large P^{(k)}$ has the *number of paths of length $\displaystyle \large k$ between all nodes*
$$\displaystyle \Huge \begin{eqnarray} 

P^{(k)}&:& \text{is a matrix where } dim(P^{(k)}) = V \times V \\
P^{(k)}_{uv}&:& \#\text{number of paths of length k between u and v}
\end{eqnarray}$$

The claim is, the matrix $\displaystyle \large P^{(k)}$ is defined as the powers of the adjacency matrix
$$\displaystyle \Huge \begin{eqnarray} 
P^{(k)} = A^k
\end{eqnarray}$$
