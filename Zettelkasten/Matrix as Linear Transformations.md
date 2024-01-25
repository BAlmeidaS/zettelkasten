---
tags:
  - Linear-algebra
---
*[[Matrix]] can be used to represent [[linear transformation]]!*

A matrix that makes a linear transformation in a space of *$\displaystyle \large n$ dimensions* has $\displaystyle \large n\times n$  *shape*.
The first column is to where $\displaystyle \large \hat{i}$ is going (being $\displaystyle \large \hat{i}$ a [[unit vector]] that points towards x-axis)
The second column is to where $\displaystyle \large \hat{j}$ is going (being $\displaystyle \large \hat{j}$ a [[unit vector]] that points towards y-axis)
...

![[Pasted image 20240124174303.png|400]]

And the matrix can be used as a function to transform input vectors
$$\displaystyle \Huge \begin{eqnarray} 
A * \vec{x} &=& \vec{y} \\\\
\text{for instance,} \\
\begin{bmatrix} 3 & 1 \\ 1 & 2\end{bmatrix}
\begin{bmatrix} -1 \\ 2\end{bmatrix}
&=&
\begin{bmatrix} -1 \\ 3\end{bmatrix}

\end{eqnarray}$$
![[Pasted image 20240124174640.png|500]]