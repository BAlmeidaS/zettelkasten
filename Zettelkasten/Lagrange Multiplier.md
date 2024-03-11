---
tags:
  - Calculus
---
*Lagrange Multipliers* is a *analytical method* to find local minimum (or maximum). It is useful *when you have a constrained in your space*.

You want to *optimise* a [[multivariable function]] $\displaystyle \large f(x,y,\dots)$ subject to one or more constrains $\displaystyle \large g(x,y,\dots)$ . The idea is *transforming a constrained optimisation problem into an unconstrained problem* by adding additional variables called *lagrange multipliers*, denoted by $\displaystyle \large \lambda$. Using [[gradient]] we have to:
$$\displaystyle \Huge \begin{eqnarray} 
\text{in order to maximize } f \\
\text{with contrainst } g \\
\\
\text{we must solve}, \\
\nabla f &=& \lambda \nabla g \\
g(x,y,\dots) &=& 0
\end{eqnarray}$$
This function can be unified in one single vector, and so, one system of equations to solve
$$\displaystyle \Huge \begin{eqnarray} 
\nabla\mathcal{L}(x, y, \dots,\lambda) = 
\begin{bmatrix} 
\frac{\partial f}{\partial x} - \lambda \frac{\partial g}{\partial x} \\
\frac{\partial f}{\partial y} - \lambda \frac{\partial g}{\partial y} \\
\vdots \\
-g(x,y,\dots)
\end{bmatrix}
= 0
\end{eqnarray}$$


One way to find the *Lagrange multipliers* is by using the [[Newton-Raphson]] method.


