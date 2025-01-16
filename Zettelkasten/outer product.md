---
tags:
  - Linear-algebra
---
In linear algebra, the **outer product** is a mathematical operation that takes two [[vector]] and produces a [[matrix]].

If $\displaystyle \large u$ is a column vector ($\displaystyle \large n \times 1$) and $\displaystyle \large v$ is a row vector ($\displaystyle \large 1 \times m$), the outer product is a matrix $\displaystyle \large A$ $\displaystyle \large (n\times m)$
$$\displaystyle \Huge \begin{eqnarray} 
A &=& u \otimes v
\\\text{where, }&&
\\
A_{ij} &=& u_iv_j
\end{eqnarray}$$

*The outer product computes the **pairwise multiplication** of **each element of one vector with every element of the other vector***.

>[!example]
> $$\displaystyle \Huge \begin{eqnarray} 
> && u = \begin{bmatrix}  1 \\ 2 \end{bmatrix},
> v = \begin{bmatrix} 3 & 4 \\ \end{bmatrix}
> \\
> A &=& \begin{bmatrix} 1*3 & 1*4 \\ 2*3 & 2*4 \end{bmatrix}
> = \begin{bmatrix} 3 & 4 \\ 6 & 8 \end{bmatrix}
> \end{eqnarray}$$

>[!note]
> *outer product* is not [[matrix multiplication]]. *outer product* involves two [[vector|vectors]] rather than two [[matrix|matrices]].
>
> *Matrix multiplication*, on each cell calculation have *sums*. Nonetheless, *outer product* has only multiplications!



