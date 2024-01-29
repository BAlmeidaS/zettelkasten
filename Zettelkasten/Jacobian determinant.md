---
tags:
  - Calculus
---
Given that the [[Jacobian matrix]] is the linear transformation around each point of the [[domain of a function|domain]]. It is worth to notice that it will be only possible to calculate if the [[Jacobian matrix]] is squared, in other words, if the [[domain of a function|domain]] and [[codomain of a function|codomain]] have the same number of variables:
$$\displaystyle \Huge \begin{eqnarray} 
f: \mathbb{R}^n\rightarrow\mathbb{R}^n
\end{eqnarray}$$

Its [[Determinant]] is basically *how much a transformation stretches or squishes the space*

>[!example]
>$$\displaystyle \Huge \begin{eqnarray} 
>f(x, y) &=&
>\begin{bmatrix}  
>xy \\ x^2-y^2
>\end{bmatrix}
>\\\\
>J(f(x,y)) &=&
>\begin{bmatrix}  
>y & x \\
>2x & -2y
>\end{bmatrix}
>\\\\
>det(J(f(x,y))) &=& -2y^2 - 2x^2
>\end{eqnarray}$$
>
>around point $\displaystyle \large (1,1)$ the function *stretches* the space in $\displaystyle \large 4$ and *invert* its orientation:
>$$\displaystyle \Huge \begin{eqnarray} 
>det(J(f(1,1))) &=& -2*1^2 - 2*1^2 \\
>&=& -4
>\end{eqnarray}$$

