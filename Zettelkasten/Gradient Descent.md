---
tags:
  - machine-learning
---
*Gradient descent* is the most important [[iteration]] *optimisation* algorithm to *estimates where a function outputs its lowest values*. Extensively used in [[Neural networks]].

It does not by setting the [[gradient]] as 0, but to *numerically approximating towards the result*.

To *minimize a function, we can follow the **negative** of the [[gradient]] and go in the direction of the **steepest descent**. The [[gradient]] of the function is often called [[Grad of F]].

Important to notice that *Gradient descent works well on [[multivariable function]]*

The pure form of the algorithm is defined as:
$$\displaystyle \Huge \begin{eqnarray} 
x_{n+1} = x_n - \alpha\nabla f(x_n)
\end{eqnarray}$$

$\displaystyle \large \alpha$ is known as the step size, and *the algorithm relies on the right decision of $\displaystyle \large \alpha$*.

Starting from a initial guess $\displaystyle \large x_0$ we keep improving little by little till we find a *local minimum*.
![[Pasted image 20240311182516.png|300]]
_the iteration process of Gradient Descent starting on $\displaystyle \large x_0$_

>[!example]
>One example is, let's find the best polynomial degree 5 that approximate $\displaystyle \large sin(x)$ in the interval $\displaystyle \large -3 < x < 3$.
>so, $\displaystyle \large p(x) = a_0 + a_1x + a_2x^2 + a_3x^3 + a_4x^4 + a_5x^5$.
>Then we have to find a function to minimise (to use gradient descent), one option is to minimise the [[least-squares]]:
>$$\displaystyle \Huge \begin{eqnarray} 
>f(a_0,\cdots, a_5) = \int^3_{-3}(p(x) - sin(x))^2dx
>\end{eqnarray}$$
>starting by random $\displaystyle \large a_0, \cdots, a_n$, this is the evolution of it:
>![[074f7d79729339289fdae362de9f4434009cdb02.gif|200]]

### Limitations
- It finds only [[local minima]], instead of guaranteed [[local minima|global minima]]
- Depends too much on step size $\displaystyle \large \alpha$. A good choice here is the difference of converge very fast, slowly, or even diverge.
- only works if the function is [[differentiable]] everywheere
![[Pasted image 20240311184058.png]]


