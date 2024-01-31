---
tags:
  - Calculus
---
It is an "extension" of [[local linearization]]. Here the goal is to *approximate a [[multivariable function]] to a quadratic function* using its [[partial derivatives]]. 
![[Pasted image 20240131200748.png|300]]
_blue is the original function, light-gray is the quadratic approximation_

The *quadratic approximation* will be defined as $\displaystyle \large Q(x,y,\dots)$.

The idea is having more than the *first* [[partial derivatives|partial derivative]] equal on the approximation, but also the *second* [[partial derivatives|partial derivative]]. For instance, example with 2-variables:
$$\displaystyle \Huge \begin{eqnarray} 
Q_{xx}(x_0,y_0) &=& f_{xx}(x_0, y_0) \\
Q_{xy}(x_0,y_0) &=& f_{xy}(x_0, y_0) \\
Q_{yy}(x_0,y_0) &=& f_{yy}(x_0, y_0) \\
\end{eqnarray}$$
To do this, the quadratic approximation must be:
$$\displaystyle \Huge \begin{eqnarray} 
Q(x,y) &=& f(x_0,y_0) \\
       & & + f_x(x_0,y_0)(x-x_0) \\
       & & + f_y(x_0,y_0)(y-y_0) \\
       & & + \dfrac{1}{2}f_{xx}(x_0,y_0)(x-x_0)^2 \\
       & & + f_{xy}(x_0,y_0)(x-x_0)(y-y_0) \\
       & & + \dfrac{1}{2}f_{yy}(x_0,y_0)(y-y_0)^2 \\
\end{eqnarray}$$

