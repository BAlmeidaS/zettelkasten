---
tags:
  - Calculus
aliases:
  - tangent plane
---
Given a [[multivariable function]], we can find the plane (or hyperplane) that is tangent to a point in the graph using [[partial derivatives]]. 

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
>[!hint]
>at the red-point, the function and the plane have the same value $\displaystyle \large L_f(x_0, y_0) = f(x_0, y_0)$

Or in general terms, the *tangent plane can be defined as*:
$$\displaystyle \Huge \begin{eqnarray} 
L_f(x, y, z, \dots) &=& F_x(x_0, y_0, z_0, \cdots) \\
&& + F_y(x_0, y_0, z_0, \cdots) \\
&& + F_z(x_0, y_0, z_0, \cdots) \\
&& + \cdots \\
&& + f(x_0, y_0, z_0, \cdots)

\end{eqnarray}$$