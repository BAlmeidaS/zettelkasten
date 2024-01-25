---
tags:
  - Linear-algebra
---
*eigenvector* are [[vector|vectors]] that *after a [[linear transformation]] don't change their direction*, the lingo is "the span is the same". Thus, they can be used as the *characteristic* property of the *transformation*.

Each *eigenvector* has associated an [[eigenvalue]].

So, an *eigenvector* $\displaystyle \large \vec{v}$ is the one that points to the same direction after the transformation $\displaystyle \large A$, only scaling it by its [[eigenvalue]] $\displaystyle \large \lambda$:
$$\displaystyle \Huge \begin{eqnarray} 
A\vec{v} &=& \lambda\vec{v}\\
\end{eqnarray}$$

A transformation can have from 0 to infinite eigenvectors.

>[!note] Math to solve the equation
>$\displaystyle \large I$ stands for [[identity matrix]]
>$$\displaystyle \Huge \begin{eqnarray} 
>A\vec{v} = \lambda\vec{v} \\
>A\vec{v} = (\lambda I)\vec{v} \\
>(A-\lambda I)\vec{v} = \vec{0}
>\end{eqnarray}$$
>Either $\displaystyle \large \vec{v} = \vec{0}$  or $\displaystyle \large (A-\lambda I) = \vec{0}$, being the later the one that we are interested in
>$$\displaystyle \Huge \begin{eqnarray} 
>A-\lambda I = \vec{0}
>\end{eqnarray}$$
>This will be zero, if its [[Determinant]] is zero - *which means that might exist a vector $\displaystyle \large \vec{v}$ that when multiplied by $\displaystyle \large I$ and removed from A, the space will be squished*, the only way is having determinant zero. 
>$$\displaystyle \Huge \begin{eqnarray} 
>det(A-\lambda I) = 0
>\end{eqnarray}$$
>Evaluating this [[Determinant]] we have the **characteristic polynomial**. The solution of this polynomial are the [[eigenvalue|eigenvalues]].
>
>By plugging the [[eigenvalue|eigenvalues]] in the original expression $\displaystyle \large (A-\lambda I)\vec{v} = 0$ *we can find the eigenvectors*

>[!example] example with a 2x2 easy matrix
> Considering $\displaystyle \large A = \begin{bmatrix} 1 & 0 \\ 0 & 2 \end{bmatrix}$:
>$$\displaystyle \Huge \begin{eqnarray} 
>det\left(
>\begin{bmatrix} 1&0 \\ 0&2 \end{bmatrix} - 
>\begin{bmatrix} \lambda&0 \\ 0&\lambda \end{bmatrix}
>\right) &=& 0
>\\
>det\left(
>\begin{bmatrix} 1-\lambda&0 \\ 0&2-\lambda \end{bmatrix}
>\right) &=& 0
>\\
>(1-\lambda)(2-\lambda) &=& 0 \\\\
>
>\text{solutions:}\\
>\lambda_1 &=& 1\\
>\lambda_2 &=& 2
>\end{eqnarray}$$ 
>now applying back in the original expression:
>$$\displaystyle \Huge \begin{eqnarray} 
>\lambda=1 &:& 
>\begin{bmatrix} 1-1 & 0 \\ 0 & 2-1 \end{bmatrix}
>\begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = \vec{0}
>\\ & & 
>\begin{bmatrix} 0 & 0 \\ 0 & 1 \end{bmatrix}
>\begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = \vec{0}
>\\ & &
>\begin{bmatrix} 0 \\ x_2 \end{bmatrix} = \vec{0}
>\\\\
>\lambda=2 &:& 
>\begin{bmatrix} 1-2 & 0 \\ 0 & 2-2 \end{bmatrix}
>\begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = \vec{0}
>\\ & & 
>\begin{bmatrix} -1 & 0 \\ 0 & 0 \end{bmatrix}
>\begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = \vec{0}
>\\ & &
>\begin{bmatrix} -x_1 \\ 0 \end{bmatrix} = \vec{0}
>\\
>\end{eqnarray}$$
>
>For $\displaystyle \large \lambda = 1$, any vector that $\displaystyle \large x_2 = 0$ is an eigenvector. Thus, the vector $\displaystyle \large \begin{bmatrix} t \\ 0 \end{bmatrix}$ is an *eigenvector*, and its *eigenvalue* is $\displaystyle \large 1$.
>
>For $\displaystyle \large \lambda = 2$, any vector that $\displaystyle \large x_1 = 0$ is an eigenvector. Thus, the vector $\displaystyle \large \begin{bmatrix} 0 \\ t \end{bmatrix}$ is an *eigenvector*, and its *eigenvalue* is $\displaystyle \large 2$.

Bare in mind that the **characteristic polynomial** has the *degree equivalent to the number of dimensions*, which vary fast has a problem to be solved manually!