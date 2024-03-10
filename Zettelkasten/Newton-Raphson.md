---
tags:
  - Calculus
---
To solve an equation, or to find where $\displaystyle \large f(x) = 0$, we can use the *newton-raphson* method. It is an *iterative method* based on, getting the [[function]], get its [[derivative]] and using the *Newton-Raphson [[iteration]] formula*:
$$\displaystyle \Huge \begin{eqnarray} 
x_{n+1} = x_n - \dfrac{f(x_n)}{f^\prime(x_n)}
\end{eqnarray}$$

This formula is derived from the first-order of [[taylor series]].

>[!example]
>if we want to find a solution for $\displaystyle \large y = x^3 - 2x + 2$, we must do:
>$$\displaystyle \Huge \begin{eqnarray} 
>y&=&x^3-2x+2 \\
>\dfrac{\partial y}{\partial x} &=& 3x^2-2
>\\\\
>\text{newton raphson:} & & \text{(initial guess x = 2)}\\
>i=0, x=2 &\rightarrow& y(x_i) = -2,& \frac{\partial y}{\partial x} = 10 \\
>i=1, x=2 &\rightarrow& y(x_i) = -0.23,& \frac{\partial y}{\partial x} = 7.7 \\
>i=2, x=2 &\rightarrow& y(x_i) = -0.005,& \frac{\partial y}{\partial x} = 7.4 \\
>\end{eqnarray}$$

This method has a problem that *depending on the function it can lead to no solution*, not converging (by oscillating) or even converging in another result farther from the point.

>[!hint] Python + scipy
>*scipy* has a newton-raphson implemented:
>```python
>from scipy import opt
>```
