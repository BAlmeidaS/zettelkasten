---
tags:
  - Calculus
---
*Jacobian* can be understood as a generalisation of the [[gradient]] - Gradient is like the "Jacobian row".

Jacobians are applied on [[vector-valued function]] rather than multivariable functions.

So, given a function $\displaystyle \large  f: \mathbb{R}^n \rightarrow \mathbb{R}^m$, the *jacobian* $\displaystyle \large J(f)$ is a matrix of $\displaystyle \large m \times n$, with all the [[partial derivatives]] possible:
$$\displaystyle \Huge \begin{eqnarray} 
J(f) = 
\begin{bmatrix} 
\dfrac{\partial f_1}{\partial x_1} & \cdots & \dfrac{\partial f_1}{\partial x_n}
\\
\vdots & \ddots & \vdots
\\
\dfrac{\partial f_m}{\partial x_1} & \cdots & \dfrac{\partial f_m}{\partial x_n}
\end{bmatrix}
\end{eqnarray}$$

The *jacobian matrix* is the best *linear approximation of a vector-valued function near a given point* - it illustrates how the [[linear transformation|function transform]], stretches and rotates its [[domain of a function|domain]]. 

*It more than recording what are the partial derivatives, **the Jacobian matrix represents the [[linear transformation]] when you zoom in near to a specific point**.

>[!hint] Explanation
> given the function $\displaystyle \large f$:
>$$\displaystyle \Huge \begin{eqnarray} 
>f(
>\begin{bmatrix}  x \\ y \end{bmatrix}
>) &=& 
>\begin{bmatrix}  
>x+sin(y) \\ y+sin(x)
>\end{bmatrix}
>\end{eqnarray}$$
>Note how it changes the [[domain]], in a non-linear way:
>![[Peek 2022-07-18 17-13.gif|300]]
>
How ever, *it does transform the domain* **linearly** on a very very small area:
![[Peek 2022-07-18 17-17.gif]]
>
The *Jacobian matrix represents the [[linear transformation]] around each point*!

>[!example]
>$$\displaystyle \Huge \begin{eqnarray} 
>f(x, y) &=&
>\begin{bmatrix}  
>xy \\ sin(x+y) \\ x^2-y^2
>\end{bmatrix}
>\\\\
>J(f(x,y)) &=&
>\begin{bmatrix}  
>y & x \\
>cos(x+y) & cos (x+y) \\
>2x & -2y
>\end{bmatrix} \\
>\end{eqnarray}$$

If we want to apply the *Jacobian*/transformation in a point of the domain, we have to calculate the *matrix multiplication*:
$$\displaystyle \Huge \begin{eqnarray} 
J(f(x_0, x_1, \cdots)) * \begin{bmatrix} x_0 \\ x_1 \\ \vdots \end{bmatrix} =\text{the transformation around the input point}
\end{eqnarray}$$
