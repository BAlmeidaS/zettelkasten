---
tags:
  - Calculus
---
For [[multivariable function|multivariable functions]], imagine that each variable of the function depends on an external variable, often referred as $\displaystyle \large t$.

So, $\displaystyle \large x_0$ can be expressed as function on $\displaystyle \large t$, $\displaystyle \large f_{x_0}(t) = x_0$.
The same to $\displaystyle \large x_1$, and so.

In such case, the *total* [[derivative]] is calculated as the sum of the [[partial derivatives]] in respect of that variable, using [[Chain Rule]]:
$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{df}{dt} &=& 
\dfrac{\partial f}{\partial x_0}\dfrac{\partial x_0}{\partial t} +
\dfrac{\partial f}{\partial x_1}\dfrac{\partial x_1}{\partial t} +
\cdots
\end{eqnarray}$$

>[!example]
>$$\displaystyle \large \begin{eqnarray} 
>f(x,y,z) &=& sin(x)e^{yz^2} \\
>\text{given,}&& x = t-1; y=t^2;z=\dfrac{1}{t} \\\\
>
>\dfrac{f(x,y,z)}{dt} &=& cos(x)e^{yz^2}*1 + z^2sin(x)e^{yz^2} * 2t +2yzsin(x)e^{yz^2}*-t^{-2} \\
>
>&&\text{(replacing x,y,z to its representations using t...)}\\
>
>\dfrac{f(x,y,z)}{dt} &=& cos(t-1)e
>
>
>\end{eqnarray}$$

The [[chain rule - vector form]] is also an option!