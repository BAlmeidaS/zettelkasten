---
tags:
  - Linear-algebra
---
[[how matrices transform space|Some types of transformation that matrix]] can do:

- Only by *scaling the space*, like in $\displaystyle \large \begin{bmatrix} 3 & 0 \\ 0 & 2\end{bmatrix}$, scaling horizontally by 3 and vertically by 2
- flipping the space, like in $\displaystyle \large \begin{bmatrix} -1 & 0 \\ 0 & 1 \end{bmatrix}$
- mirroring in 45 degrees, $\displaystyle \large \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}$
- shearing the space, $\displaystyle \large \begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix}$
- rotating in 45 degrees, $\displaystyle \large \begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}$
- rotating in $\displaystyle \large \theta$, $\displaystyle \large \begin{bmatrix} cos(\theta) & sin(\theta) \\ -sin(\theta) & cos(\theta) \end{bmatrix}$

*the first column of the transformation is the new position of $\displaystyle \large e_1$, the second column is the new position of $\displaystyle \large e_2$, and so on.*

Being, $\displaystyle \large e_1 = \begin{bmatrix} 1 \\ 0 \\ 0 \\ \vdots \end{bmatrix}$, and so on. 

**transformations can be created by a composition of the above transformations**, because [[combine linear transformations]]