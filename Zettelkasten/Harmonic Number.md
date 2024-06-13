---
tags:
  - math
---
The *Harmonic Number* is defined as $\displaystyle \large H_n$ and is the *n-th harmonic number*.

$$\displaystyle \Huge \begin{eqnarray} 
H_n = \sum^{n}_{k=1}\dfrac{1}{k}
\end{eqnarray}$$
The n-th harmonic number has also an [[integral]] representation:
$$\displaystyle \Huge \begin{eqnarray} 
H_n = \int^1_0 \dfrac{1-x^n}{1-x}dx
\end{eqnarray}$$

Harmonic number is defined as the area under the *reciprocals*. And the area (*blue rectangles*) is bigger than $\displaystyle \large log(n)$ (*yellow curve*), but usually is a good approximation (log(n))
![[Pasted image 20240613190130.png|600]]

$$\displaystyle \Huge \begin{eqnarray} 
H_n = \sum^{n}_{k=1}\dfrac{1}{k}
&\approx& log(n) 
\\ && \text{(or even better approximation...)} \\
&\approx& log(n) + \gamma
\\ && \text{(being $\gamma$ the Euler-Mascheroni Constant = 0.57721)} \\
&\approx& log(n) + 0.6
\end{eqnarray}$$