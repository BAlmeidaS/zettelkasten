---
tags:
  - Linear-algebra
aliases:
  - row rank
  - column rank
  - rank
---
Given a [[matrix]] $\displaystyle \large A$ $\displaystyle \large (m \times n)$,
- the *row rank* of $\displaystyle \large A$ is the dimension of the span of the rows of A. *It is the maximum number of [[linear independence|linearly independent]] rows*.
- the *column rank* of $\displaystyle \large A$ is the dimension of the span of the columns of $\displaystyle \large A$. *it is the maximum number of [[linear independence|linearly independent]] columns*

the *column rank and the row rank are always equal* ([Rank Theorem](https://en.wikipedia.org/wiki/Rank_(linear_algebra)#Proofs_that_column_rank_=_row_rank)), so we use one of them and we call just *the rank of the matrix* (usually the column).

>[!example]
>$$\displaystyle \Huge \begin{eqnarray} 
>A &=&
>\begin{bmatrix} 
>1 & 0 & 1 \\
>0 & 1 & 1 \\
>0 & 1 & 1 \\
>\end{bmatrix}
>\\\\
>rank(A) &=& 2
>\end{eqnarray}$$
>Since only two columns are *linearly independent*.
