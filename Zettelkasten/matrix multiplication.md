---
tags:
  - Linear-algebra
---
*Matrix multiplication* is a series of [[dot product|dot products]].

when doing $\displaystyle \large A * B$, being $\displaystyle \large A$ and $\displaystyle \large B$ [[matrix|matrices]], the resultant [[matrix]] is the *[[dot product]] of each row of $\displaystyle \large A$ with each column of $\displaystyle \large B$:*

$$\displaystyle \Huge \begin{eqnarray} 
C_{n \times m} &=& A_{n \times p}*B_{p \times m} \\

c_{ij}&=&\sum_{k=1}^{p}a_{ik}b_{kj}
\end{eqnarray}$$
![[Pasted image 20240129212410.png|300]]

>[!hint] python
>in python, using *numpy*, the operator *@* does matrix multiplication
