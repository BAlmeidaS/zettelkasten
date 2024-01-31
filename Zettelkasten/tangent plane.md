---
tags:
  - Calculus
aliases:
  - tangent plane
  - local linearization
---
Given a [[multivariable function]], we can find the plane (or hyperplane) that is tangent to a point in the graph using [[partial derivatives]]. This is called as well *local linearization
*

![[Pasted image 20240131155408.png|400]]
_tangent plane on the red-point_

The way to calculate the formula of this plane $\displaystyle \large L_f(x,y)$, defined on the red-point $\displaystyle \large (x_0, y_0)$, given a function $\displaystyle \large f(x,y): \mathbb{R}^2 \rightarrow \mathbb{R}$:

$$\displaystyle \Huge \begin{eqnarray} 
f(x,y) &=& z
\\\\
L_f(x,y) &=&
\dfrac{\partial f(x_0,y_0)}{\partial x}*(x-x_0) +
\dfrac{\partial f(x_0,y_0)}{\partial y}*(y-y_0) + f(x_0, y_0)
\end{eqnarray}$$

We can calculate the formula in a *vector form* and extend to m
