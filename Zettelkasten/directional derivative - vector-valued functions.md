---
tags:
  - Calculus
---
General case of [[directional derivative|directional derivatives]].  The *directional derivative* is defined as $\displaystyle \large D_vf$

If you have some [[multivariable function]], $\displaystyle \large f: \mathbb{R}^n \rightarrow \mathbb{R}^m$, and some [[vector]] $\displaystyle \large \vec{v}$ in the [[domain of a function|domain]] (*n* dimensions) and want to understand what happens *when we nudge the input of $\displaystyle \large f$ in a direction of $\displaystyle \large \vec{v}$*. 

In other words, what is the *vector rate change of $\displaystyle \large f$ while we change the inputs through $\displaystyle \large \vec{v}$*. 

Each component of $\displaystyle \large D_vF$ tells you how much the corresponding component of [[codomain of a function|codomain]] is changing as you move a tiny step from a given point in the direction of $\displaystyle \large \vec{v}$ within the [[domain of a function|domain]].

This will be the [[matrix multiplication]] of the [[Jacobian matrix]] with $\displaystyle \large \vec{v}$:
$$\displaystyle \Huge \begin{eqnarray} 
D_vf &=& J_f*\vec{v} \\
\end{eqnarray}$$

*The result is a [[vector]] $\displaystyle \large D_vf$*, and it gives the rate of change of each component of $\displaystyle \large f$ in the direction of $\displaystyle \large \vec{v}$, encapsulating how the function $\displaystyle \large f$ changes as a whole in that direction.

---

*usually the vector $\displaystyle \large \vec{v}$ is normalized to a [[unit vector]]*, but this is not a restriction, it is just good practice to ensure a consistent interpretation of the directional derivative as a rate of change per unit length.