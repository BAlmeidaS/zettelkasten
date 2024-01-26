---
tags:
  - Calculus
---
For [[multivariable function]] (or even [[vector-valued function]]) we can calculate *partial derivatives*, which are basically [[derivative|derivatives]] *with respect to one variable (and treat the rest as constants)*:

$$\displaystyle \Huge \begin{eqnarray} 
\text{if} f&:&\mathbb{R}^n \rightarrow \mathbb{R} \\
\dfrac{\partial f(x_0,x_1,...)}{\partial x_0} &=& \lim_{h \to 0} \dfrac{f(x_0+h, x_1, \dots) - f(x_0, x_1, \dots)}{h}
\end{eqnarray}$$

>[!example] example
>$$\displaystyle \Huge \begin{eqnarray} 
>f(x,y,z) &=& sin(x)e^{yz^2} \\\\
>
>\dfrac{\partial f}{\partial x} &=& cos(x)e^{yz^2}\\\\
>\dfrac{\partial f}{\partial y} &=& sin(x)e^{yz^2}z^2\\\\
>\dfrac{\partial f}{\partial z} &=& sin(x)e^{yz^2}2yz\\
>
>\end{eqnarray}$$

