---
tags:
  - machine-learning
aliases:
  - soft clustering
---
In *fuzzy [[Clustering]]* objects can belong to more than one cluster.

The result of a fuzzy clustering can be represented as a matrix $\displaystyle \large k \times n$:
$$\displaystyle \Huge \begin{eqnarray} 
U =
\begin{bmatrix} 
u_{11} &  u_{12} & \ldots & u_{1n} \\
u_{21} &  u_{22} & \ldots & u_{2n} \\
\vdots &  \vdots &  \ddots &  \vdots \\
u_{k1} &  u_{k2} & \ldots & u_{kn} \\
\end{bmatrix}
\end{eqnarray}$$
$\displaystyle \large n$ denotes for the number of [[instance|records]]
$\displaystyle \large k$ denotes for the number of [[cluster]]

Moreover, $\displaystyle \large u_{ij}$ can be *any value between 0 and 1*, and this can be understood as the probability of that point to be from that cluster:
$$\displaystyle \Huge \begin{eqnarray} 
fuzzy\ clustering \iff u_{ij} \in [0, 1]
\end{eqnarray}$$

and, the sum of all the probabilities for a given datapoint must be 1:
$$\displaystyle \Huge \begin{eqnarray} 
\sum^k_{i=1} u_{ij} = 1, \forall j \in [1, n]
\end{eqnarray}$$

Also, there is no empty cluster:
$$\displaystyle \Huge \begin{eqnarray} 
\sum^n_{j=1} u_{ij} > 0, \forall i \in [1, k]
\end{eqnarray}$$

Very much connected with [[Fuzzy Logic]]