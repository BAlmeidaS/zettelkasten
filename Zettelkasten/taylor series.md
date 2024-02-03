---
tags:
  - Calculus
---
The *taylor series* or *taylor expansion* is a way to approximate a *single-variable* [[function]] near to a point $\displaystyle \large a$ using its [[derivative|derivatives]] and [[high-order derivatives]].

$$\displaystyle \Huge \begin{eqnarray} 
f(x) \approx f(a) 
+ f^{\prime}(a)(x-a) 
+ \dfrac{f^{\prime\prime}(a)}{2!}(x-a)^2
+ \dfrac{f^{\prime\prime\prime}(a)}{3!}(x-a)^3
\end{eqnarray}$$

or more generally:
$$\displaystyle \Huge \begin{eqnarray} 
f(x) = \sum^\infty_{n=0}\dfrac{f^{(n)}(a)}{n!}(x-a)^n
\end{eqnarray}$$

*The taylor expansion of any [[polynomial]] is the [[polynomial]] itself*

We can say *n-order approximation* when we use until the $\displaystyle \large n$th derivative.

*Remember that taylor function work VERY poorly when functions are not well-behaved*. Check the comparison between the approximations of $\displaystyle \large cos(x)$ and $\displaystyle \large \dfrac{1}{x}$
![[Peek 2024-02-02 21-10.gif|400]]

---
[Visualising Taylor Series](https://www.coursera.org/learn/multivariate-calculus-machine-learning/ungradedWidget/SgnFT/visualising-taylor-series)
  