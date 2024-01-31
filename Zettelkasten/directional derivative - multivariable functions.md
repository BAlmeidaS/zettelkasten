---
tags:
  - Calculus
---
This is the simplest case of [[directional derivative|directional derivatives]]. 

If you have some [[multivariable function]], $\displaystyle \large f: \mathbb{R}^n \rightarrow \mathbb{R}$, and some [[vector]] $\displaystyle \large \vec{v}$ in the [[domain of a function|domain]] (*n* dimensions) and want to understand what happens *when we nudge the input of $\displaystyle \large f$ in a direction of $\displaystyle \large \vec{v}$*. In other words, what is the *rate at which $\displaystyle \large f$ will change while the inputs moves through $\displaystyle \large \vec{v}$*.

The *directional derivative* is defined as $\displaystyle \large D_vf$

This will be the [[dot product]] of the [[gradient]] with $\displaystyle \large \vec{v}$:
$$\displaystyle \Huge \begin{eqnarray} 
D_vf &=& \nabla_{\vec{v}}f \\
     &=& \nabla f \cdot\vec{v} \\
     &=& \sum^n_{i=0} \vec{v}_i * \dfrac{\partial f(x_0, x_1, \cdots)}{\partial x_i}
\end{eqnarray}$$

---

*usually the vector $\displaystyle \large \vec{v}$ is normalized to a [[unit vector]]*, but this is not a restriction, it is just good practice to ensure a consistent interpretation of the directional derivative as a rate of change per unit length.