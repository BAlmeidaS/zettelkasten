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
\text{we must solve}, \\\\
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

>[!example] 
>let's say that we have the [[multivariable function]] $\displaystyle \large f(x,y) = x^2 y$ and we want to find the maximum of this function around a circle defined as  $\displaystyle \large x^2 + y^2 = a^2$.
> 
> To solve this problem we can use *lagrange multiplier*.
> *First*, solve the *first equation*:
> $$\displaystyle \Huge \begin{eqnarray} 
> \nabla f &=& \lambda \nabla g \\\\
> \begin{bmatrix}  2xy \\ x^2 \end{bmatrix}
> &=&
> \lambda \begin{bmatrix}  2x \\ 2y \end{bmatrix}
> \\ \\
> \text{from the first element,}
> \\
> 2xy &=& \lambda 2x\\
> y &=& \lambda
> \\ \\
> \text{from the second element,}
> \\
> x^2 &=& \lambda 2y \\
> &=& 2y^2 \\
> x &=& \pm \sqrt{2}y
> \end{eqnarray}$$
>
> *Second*, using the *second equation*:
> $$\displaystyle \Huge \begin{eqnarray} 
> g(x,y,\dots) &=& 0 \\\\
> x^2+y^2 &=& a^2 \\
> &=& 3y^2 \\
> y &=& \pm \dfrac{a}{\sqrt{3}}
> 
> \end{eqnarray}$$
>
>so, there are 4 solutions to x and y:
>$$\displaystyle \Huge \begin{eqnarray} 
>solutions:\\
>& \dfrac{a}{\sqrt{3}} \begin{bmatrix} \sqrt{2} \\ 1 \end{bmatrix}, \\
>& \dfrac{a}{\sqrt{3}} \begin{bmatrix} -\sqrt{2} \\ 1 \end{bmatrix}, \\
>& \dfrac{a}{\sqrt{3}} \begin{bmatrix} \sqrt{2} \\ -1 \end{bmatrix}, \\
>& \dfrac{a}{\sqrt{3}} \begin{bmatrix} -\sqrt{2} \\ -1 \end{bmatrix}, \\
>\end{eqnarray}$$
>
>From this solutions we must plug again on the function $\displaystyle \large f(x,y) = x^2y$:
>$$\displaystyle \Huge \begin{eqnarray} 
>f\left(
>\dfrac{a\sqrt{2}}{\sqrt{3}}, 
>\dfrac{a}{\sqrt{3}} 
>\right)
>&=&
>\dfrac{2a^3}{3\sqrt{3}}
>\\
>f\left(
>\dfrac{-a\sqrt{2}}{\sqrt{3}}, 
>\dfrac{a}{\sqrt{3}} 
>\right)
>&=&
>\dfrac{2a^3}{3\sqrt{3}}
>\\
>f\left(
>\dfrac{a\sqrt{2}}{\sqrt{3}}, 
>\dfrac{-a}{\sqrt{3}} 
>\right)
>&=&
>\dfrac{-2a^3}{3\sqrt{3}}
>\\
>f\left(
>\dfrac{-a\sqrt{2}}{\sqrt{3}}, 
>\dfrac{-a}{\sqrt{3}} 
>\right)
>&=&
>\dfrac{-2a^3}{3\sqrt{3}}
>\\
>\end{eqnarray}$$
>
>And so we have the *maximum value* $\displaystyle \large \dfrac{2a^3}{3\sqrt{3}}$, and for free we got also the minimum value.
>
>This is the result:
>![[Pasted image 20241206200909.png]]
