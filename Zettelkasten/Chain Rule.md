---
tags:
  - Calculus
---
Consider $\displaystyle \large (f \circ g)(x)$ the composition function of $\displaystyle \large f(g(x))$,

its [[derivative]] can be calculated using the *chain rule*:

$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{d(f\circ g)(x)}{dx}  &=& 
\dfrac{df}{dg} \dfrac{dg}{dx} 
\\\\
(f\circ g)^\prime(x) &=& f^\prime(g(x))*g^\prime(x) \\
\end{eqnarray}$$

>[!note] example
>$$\displaystyle \Huge \begin{eqnarray} 
f(x) &=& sin(x^2) \\
\text{calling S the function $g(x)=x^2$},\\
f &=& sin\circ S\\\\
f^\prime(x) &=& (sin \circ S)^\prime(x) \\
&=& sin^\prime(S(x))*S^\prime(x) \\
&=& cos(x^2)*2x
\end{eqnarray}$$

