---
tags:
  - machine-learning
---
*Gradient descent* is the most important [[iteration]] *optimization* algorithm to *estimates where a function outputs its lowest values*. Extensively used in [[Neural networks]].

It does not by setting the [[gradient]] as 0, but to *numerically approximating towards the result*.

To *minimize a function, we can follow the **negative** of the [[gradient]] and go in the direction of the **steepest descent**.

The pure form of the algorithm is defined as:
$$\displaystyle \Huge \begin{eqnarray} 
x_{n+1} = x_n - \alpha\nabla f(x_n)
\end{eqnarray}$$
Starting from a initial guess $\displaystyle \large x_0$ we keep improving little by little till we find a *local minimum*.
![[Pasted image 20240311182516.png|300]]
_the iteration process of Gradient Descent starting on $\displaystyle \large x_0$_

>[!example]
>One example is, let's find the best polynomial degree 5 that approximate $\displaystyle \large sin(x)$ in the interval $\displaystyle \large -3 < x < 3$.
>so, $\displaystyle \large p(x) = a_0 + a_1x + a_2x^2 + a_3x^3 + a_4x^4 + a_5x^5$.
>Then we have to find a function to minimise (to use gradient descent), one option is to minimise the [[least-squares]]:
>$$\displaystyle \Huge \begin{eqnarray} 
>a &=& 1 \
>\end{eqnarray}$$

