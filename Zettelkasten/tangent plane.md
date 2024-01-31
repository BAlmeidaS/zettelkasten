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
>[!hint]
>at the red-point, the function and the plane have the same value $\displaystyle \large L_f(x_0, y_0) = f(x_0, y_0)$

We can calculate the formula in a *vector form* and extend to $\displaystyle \large n$ inputs using [[dot product]] and [[Gradient]] - treat them as a [[linear transformation]]:

$$\displaystyle \Huge \begin{eqnarray} 
\text{given,} &\text{ }&
\boldsymbol{x} = \begin{bmatrix}  x \\ y \\ \vdots \end{bmatrix} 
\text{and } 
\boldsymbol{x_0} = \begin{bmatrix}  x_0 \\ y_0 \\ \vdots \end{bmatrix}
\\\\
L_f(\boldsymbol{x}) &=&
f(\boldsymbol{x_0}) +
\begin{bmatrix}  
\dfrac{\partial f(\boldsymbol{x_0})}{\partial x} \\
\dfrac{\partial f(\boldsymbol{x_0})}{\partial y} \\
\vdots
\end{bmatrix}
\cdot
\begin{bmatrix}  
x-x_0 \\
y-y_0 \\
\vdots
\end{bmatrix} 
\\
L_f(\boldsymbol{x}) &=& 
f(\boldsymbol{x_0}) +
\nabla f(\boldsymbol{x_0})(\boldsymbol{x} - \boldsymbol{x_0})
\end{eqnarray}$$

*local linearization* $\displaystyle \large L_f(\boldsymbol{x})$, being:
- $\displaystyle \large f(\boldsymbol{x_0})$, the **constant term**
- $\displaystyle \large \nabla f(\boldsymbol{x_0})(\boldsymbol{x} - \boldsymbol{x_0})$, the **linear term**

>[!hint] 
>*local linearization* can be a way to approximate a function that you don't know, but you could approximate it to one point (red-point) and calculate/estimate its gradient






