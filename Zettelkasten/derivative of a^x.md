---
tags:
  - math
  - Calculus
---
The [[derivative]] of $\displaystyle \large a^x$, being $\displaystyle \large a$ any number (like $\displaystyle \large 2^x$).

First of all, we have that:
$$\displaystyle \Huge \begin{eqnarray} 
a = e^{\ln a} 
\end{eqnarray}$$

So, using the [[Chain Rule]]:
$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{d}{dx} [a^x] 
&=& \dfrac{d}{dx} [(e^{\ln a})^x] \\
&=& \dfrac{d}{dx} [e^{x*\ln a}] \\
\text{using chain rule:} \\
&=& e^{x*\ln a} * \ln a \\
&=& (e^{\ln a})^x * \ln a \\
&=& a^x * \ln a \\
\end{eqnarray}$$

Thus,
$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{d}{dx} [a^x] &=& a^x * \ln a
\end{eqnarray}$$
