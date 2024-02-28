---
tags:
  - machine-learning
---
In *fuzzy clustering* each objects is assigned to *only one cluster*

In math terms, the result of a hard clustering can be represented as a matrix $\displaystyle \large k \times n$:
$$\displaystyle \Huge \begin{eqnarray} 
u =
\begin{bmatrix} 
u_{11} &  u_{12} & \ldots & u_{1n} \\
u_{21} &  u_{22} & \ldots & u_{2n} \\
\vdots &  \vdots &  \ddots &  \vdots \\
u_{k1} &  u_{k2} & \ldots & u_{kn} \\
\end{bmatrix}
\end{eqnarray}$$
$\displaystyle \large n$ denotes for the number of [[instance|records]]
$\displaystyle \large k$ denotes for the number of [[cluster]]

Moreover,
$$\displaystyle \Huge \begin{eqnarray} 
hard\ clustering \iff u_{ij} \in \{0, 1\}
\end{eqnarray}$$

So it can be either 0 or 1!