---
tags:
  - Calculus
---
The [[Chain rule - general form]] can be vectored as, being the bold $\displaystyle \large \boldsymbol{x}$ the vector form $\displaystyle \large [x_0, x_1, \dots]$, using [[gradient]] and [[dot product]]: 
$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{df}{dt} &=& 
\dfrac{\partial f}{\partial \boldsymbol{x}}
\cdot
\dfrac{\partial \boldsymbol{x}}{\partial t}\\
\dfrac{df}{dt} &=& 
\nabla_f
\nabla_x
\end{eqnarray}$$

For many variables there must be the case that will be the [[Jacobian matrix|jacobian]] instead of the *gradient*


>[!example]
>$$\displaystyle \Huge \begin{eqnarray} 
>given,\ f(\boldsymbol{x}(\boldsymbol{u}(t))) & & \\
>f(\boldsymbol{x}) &=& f(x_1, x_2) \\
>\boldsymbol{x(u)} &=&
>\begin{bmatrix}  
>x_1(u_1, u_2) \\ 
>x_2(u_1, u_2) \\ 
>\end{bmatrix} \\
>\boldsymbol{u(t)} &=& 
>\begin{bmatrix}  
>u_1(t) \\ 
>u_2(t) \\ 
>\end{bmatrix}
>\\\\
>\dfrac{df}{dt} &=&
>\dfrac{\partial f}{\partial \boldsymbol{x}} 
>\dfrac{\partial \boldsymbol{x}}{\partial \boldsymbol{u}} 
>\dfrac{\partial \boldsymbol{u}}{\partial t} \\
>&=& \nabla_f^T\cdot J_x\cdot\nabla_u \\
>&=& 
>\begin{bmatrix}  
>\dfrac{\partial f}{\partial x_1},
>\dfrac{\partial f}{\partial x_2}
>\end{bmatrix}
>\cdot
>\begin{bmatrix}  
>\dfrac{\partial x_1}{\partial u_1} &
>\dfrac{\partial x_1}{\partial u_2} \\
>\dfrac{\partial x_2}{\partial u_1} &
>\dfrac{\partial x_2}{\partial u_2}
>\end{bmatrix}
>\cdot
>\begin{bmatrix}  
>\dfrac{\partial u_1}{\partial t} \\
>\dfrac{\partial u_2}{\partial t}
>\end{bmatrix}
>\end{eqnarray}$$

