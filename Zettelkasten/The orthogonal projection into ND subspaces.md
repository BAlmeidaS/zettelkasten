---
tags:
  - Linear-algebra
aliases:
  - projection matrix
  - orthogonal projection
---
This is the generalisation of [[The orthogonal projection into 1D subspaces]].

Here, the subspace $\displaystyle \large U$ is defined for a set of vector (rather then only one), which is its [[basis]].

So $\displaystyle \large U$ is defined by
$$\displaystyle \Huge \begin{eqnarray} 
[b_1, b_2, \dots, b_n]
\end{eqnarray}$$

Both $\displaystyle \large U$ and the vector $\displaystyle \large x$ live in a [[vector space]] that has $\displaystyle \large n+1$ dimensions. We want to project $\displaystyle \large x$ onto $\displaystyle \large U$, so there will be $\displaystyle \large n$ $\displaystyle \large \lambda$s:

>[!example] example using 3-dimensions
>![[Pasted image 20250115202941.png|600]]

$$\displaystyle \Huge \begin{eqnarray} 
\text{projection} = \pi_U(x) = \sum^n \lambda_ib_i
\end{eqnarray}$$
and *difference vector* between $\displaystyle \large x$ and $\displaystyle \large \pi_U(x)$ is **orthogonal to $\displaystyle \large U$**:
$$\displaystyle \Huge \begin{eqnarray} 
\langle x -\pi_u(x), b_i\rangle = 0, i=1,\dots,n
\end{eqnarray}$$

Thus, we can defined $\displaystyle \large \lambda$ and the [[basis]] $\displaystyle \large B$,
$$\displaystyle \Huge \begin{eqnarray} 
given,\ && \lambda=
\begin{bmatrix}  \lambda_1 \\ \vdots \\ \lambda_n \end{bmatrix}
\text{ and }
B = \begin{bmatrix}  b_1, \dots, b_n \end{bmatrix}

\\\\
\pi_U(x) &=& B\lambda
\end{eqnarray}$$

>[!tip] B will be a matrix composed with the vectors of its basis
The matrix will be the concatenation of the vectors that form the basis
>$$\displaystyle \Huge \begin{eqnarray} 
>B &=& [b_1 | b_2 | \dots]
>\\\\
>B &=& 
>\begin{bmatrix}  
>b_{1_x} & b_{2_x} & \dots \\ 
>b_{1_y} & b_{2_y} & \dots \\ 
>\vdots & \vdots & \ddots
>\end{bmatrix}
>\end{eqnarray}$$

so, we can expand the orthogonal definition:
$$\displaystyle \Huge \begin{eqnarray} 
&& \langle x -\pi_u(x), b_i\rangle = \langle B\lambda - x, b_i \rangle = 0
\\ &\iff& 
\langle B\lambda, b_i \rangle  - \langle x, b_i \rangle = 0
\\ &\iff& 
\lambda^TB^Tb_i - x^Tb_i = 0, i=1, ..., M
\\ &\iff& 
\lambda^TB^TB - x^TB = 0
\\ &\iff& 
\lambda^T = x^TB(B^TB)^{-1}
\\ &\iff& 
\lambda = (x^TB(B^TB)^{-1})^T
\\ &\iff& 
\lambda = (B^TB)^{-1}B^Tx
\end{eqnarray}$$

with the definition of $\displaystyle \large \lambda$, we can find the *projection matrix for n dimensions*:
$$\displaystyle \Huge \begin{eqnarray} 
\pi_U(x) = B\lambda = 
\overbrace{B(B^TB)^{-1}B^T}^{\text{projection matrix}} x
\end{eqnarray}$$

**if the [[basis]] B is [[orthonormal basis]]**:

$$\displaystyle \Huge \begin{eqnarray} 
B^TB = I, \text{ so in this case,}
\\
\pi_U(x) = BB^Tx
\end{eqnarray}$$

Both, the basis $\displaystyle \large B$ (by extension, the subspace $\displaystyle \large U$) and the vector $\displaystyle \large x$, are elements of the [[vector space]] $\displaystyle \large \mathbb{R}^{n+1}$, but the projection, needs only $\displaystyle \large n$ elements to be described, since *its the [[linear combination]] of the vectors that define $\displaystyle \large U$*.
