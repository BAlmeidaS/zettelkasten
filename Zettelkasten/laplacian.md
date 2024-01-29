---
tags:
  - Calculus
aliases:
  - laplacian
  - laplacian operator
---
The *laplace operator* is basically the double [[partial derivatives]] for each variable. Can be defined in two ways using [[Vector nabla|nabla]] and [[dot product]]

$$\displaystyle \Huge \begin{eqnarray} 
\Delta f &=& \nabla^2f=\nabla\cdot\nabla f 
\\\\
\Delta f(x_0, x_1, \cdots,x_n)&=& \sum^n_{i=1}\dfrac{\partial^2f}{\partial x_i^2}
\\\\
\Delta f > 0 &\rightarrow& \text{local minimum}
\\
\Delta f < 0 &\rightarrow& \text{local maximum}
\end{eqnarray}$$

>[!hint] intuition
>$\displaystyle \large \Delta f = 0$, means that, on average, the neighbour points are *equal* to the point itself
>$\displaystyle \large \Delta f > 0$, means that, on average, the neighbour points are *greater than* the point itself
>$\displaystyle \large \Delta f < 0$, means that, on average, the neighbour points are *lesser than* the point itself

