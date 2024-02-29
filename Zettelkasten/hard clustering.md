---
tags:
  - machine-learning
aliases:
  - crisp clustering
---
In *hard clustering* each objects is assigned to *only one cluster*

The result of a hard clustering can be represented as a matrix $\displaystyle \large k \times n$:
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

Moreover, $\displaystyle \large u_{ij}$ can be *either 0 or 1*:
$$\displaystyle \Huge \begin{eqnarray} 
hard\ clustering \iff u_{ij} \in \{0, 1\}
\end{eqnarray}$$

and, only one cluster is assigned to each datapoint:
$$\displaystyle \Huge \begin{eqnarray} 
\sum^k_{i=1} u_{ij} = 1, \forall j \in [1, n]
\end{eqnarray}$$

Also, there is *no empty cluster*:
$$\displaystyle \Huge \begin{eqnarray} 
\sum^n_{j=1} u_{ij} > 0, \forall i \in [1, k]
\end{eqnarray}$$

Hard clusterings are divided into:
- [[Hierarchical clustering]]
- [[Partitional clustering]]