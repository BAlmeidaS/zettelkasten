---
tags:
  - Calculus
---
Given the [[multivariable function]] $\displaystyle \large f$. The *gradient* is define by the collection of the [[partial derivatives]]:
$$\displaystyle \Huge \begin{eqnarray} 
\nabla f(x_0, x_1, \dots) &=& 
\begin{bmatrix}  
\dfrac{\partial f(x_0, x_1, \dots)}{\partial x_0} \\ 
\dfrac{\partial f(x_0, x_1, \dots)}{\partial x_1} \\ 
\vdots
\end{bmatrix}
\end{eqnarray}$$

a simplified version is 
$$\displaystyle \Huge \begin{eqnarray} 
\nabla f &=& 
\begin{bmatrix}  
\dfrac{\partial f}{\partial x_0} \\\\
\dfrac{\partial f}{\partial x_1} \\\\
\vdots
\end{bmatrix}
\end{eqnarray}$$

It has *two interpretations* that are the two sides of the same coin:
1. The gradient is a [[vector]] that gives *the direction you should travel to **increase the value of $\displaystyle \large f$** most rapidly* - *direction of steepest ascent*.
2. It is a *normal vector* to the *level curves*

>[!hint] Visual explanation
>![[Pasted image 20240126232209.png]]
>
>- In *black* is the function $\displaystyle \large f(x,y)=x^2+y^2$, notice that it can assume many values, depending on the height ($\displaystyle \large z$), thus, if defines many circles.
>- in *red* we have the plane (x,y,*1*). In this plane, the function is $\displaystyle \large f(x,y) = 1$
>- in *blue* we have the plane (x,y,*2*). In this plane, the function is $\displaystyle \large f(x,y) = 2$
>- the *gradient* of the function is $\displaystyle \large \nabla f(x,y) = \begin{bmatrix}  2x \\ 2y \end{bmatrix}$
>- The *arrows are the gradients*. Notice that they are normal to the function in the plane! (compliant with 2)
>- The *blue arrows are bigger than the red arrows*, because this is the direction that $\displaystyle \large f$ increases! (compliant with 1)

![[Pasted image 20240129181403.png]]