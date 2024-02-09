---
tags:
  - Calculus
aliases:
  - local linearization
  - linear approximation
  - first-order approximation
---
*local linearization* generalises the idea of [[tangent plane]] to *any* [[multivariable function]], also known as *first-order approximation*.

**local linearization** *approximates one function near a point based on the information you can get from its [[partial derivatives]] at that point.*

We can calculate in a *vector form* using [[dot product]] and [[gradient]]:
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
\\\\
L_f(\boldsymbol{x}) &=& 
f(\boldsymbol{x_0}) +
\nabla f(\boldsymbol{x_0})(\boldsymbol{x} - \boldsymbol{x_0})
\end{eqnarray}$$

*local linearization* $\displaystyle \large L_f(\boldsymbol{x})$, being:
- $\displaystyle \large f(\boldsymbol{x_0})$, the **constant term**
- $\displaystyle \large \nabla f(\boldsymbol{x_0})(\boldsymbol{x} - \boldsymbol{x_0})$, the **linear term**

*local linearization* has:
1. the same value of $\displaystyle \large f$ at the point $\displaystyle \large \boldsymbol{x_0}$.
$$\displaystyle \Huge \begin{eqnarray} 
f(\boldsymbol{x}) = L_f(\boldsymbol{x})
\end{eqnarray}$$
2. the partial derivatives are equal on the point $\displaystyle \large \boldsymbol{x}$:
$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{\partial L_f(x_0, y_0,\dots)}{\partial x} = 
\dfrac{\partial f(x_0, y_0, \dots)}{\partial x} 
\end{eqnarray}$$

It is a *linear* function because:
![[Pasted image 20240131163911.png]]
![[Pasted image 20240131163920.png]]

>[!hint] 
>*local linearization* can be a way to approximate a function that you don't know, but you could approximate it to one point (red-point) and calculate/estimate its gradient.
>
>The approximation says that as you move away from $\displaystyle \large x_0$, your corresponding change is equal to your distance away from $\displaystyle \large x_0$ times the gradient of your function at $\displaystyle \large x_0$.