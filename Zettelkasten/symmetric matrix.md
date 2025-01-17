---
tags:
  - Linear-algebra
---
A *symmetric matrix* is a matrix that is *symmetric* concerning its diagonal. In other words, the *superior triangle* is equal to the *inferior triangle*.

$$\displaystyle \Huge \begin{eqnarray} 
\boldsymbol{M}\text{ is quadratic} \iff M_{ij} = M_{ji}\ \forall i,j
\end{eqnarray}$$

or by using [[Matrix transpose]]:
$$\displaystyle \Huge \begin{eqnarray} 
\boldsymbol{M} \text{is symmetric if } \boldsymbol{M} = \boldsymbol{M}^T
\end{eqnarray}$$

For instance:
$$\displaystyle \Huge \begin{eqnarray} 
\begin{bmatrix} 
11 & 1 & 2 & 3 \\
1 & 22 & 4 & 5 \\
2 & 4 & 33 & 6 \\
3 & 5 & 6 & 44 \\
\end{bmatrix}
\end{eqnarray}$$

![[Pasted image 20240131221416.png]]

>[!tip]
> *Symmetric matrix* have [[eigenvector]] that are *guaranteed* to be [[Orthogonal]] to each other
