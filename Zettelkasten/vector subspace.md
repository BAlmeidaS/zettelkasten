---
tags:
  - math
---
A *vector subspace* is a set $\displaystyle \large U$ in the original [[vector space]] $\displaystyle \large V$, where when we perform the [[vector space|vector space operations]] on the *subspace* we *never leave it*.

#### Definition

Let $\displaystyle \large (V, +, \cdot)$ be an $\displaystyle \large \mathbb{R}$-vector space and $\displaystyle \large U \subseteq V, U \ne \emptyset$.

Then, $\displaystyle \large Y = (U, +, \cdot)$ is called a *vector subspace of* $\displaystyle \large V$ if $\displaystyle \large U$ is a vector space with the vector space operations $\displaystyle \large +$ and $\displaystyle \large \cdot$ restricted to $\displaystyle \large U \times U$ and $\displaystyle \large \mathbb{R} \times U$:
$$\displaystyle \Huge \begin{eqnarray} 
(1)& \quad U \ne \emptyset, & \text{ in particular, } 0 \in U
\\
(2)& \text{closure of $U$:}
\\
& (2a)\quad \text{inner operation:} &\lambda\in\mathbb{R}\ \forall x\in U :& \lambda x \in U
\\
& (2b) \quad \text{outer operation:} &\forall x,y\in U :& x+y \in U
\end{eqnarray}$$

---

#### how to identify a subspace

- For every [[vector space]] $\displaystyle \large V$ the trivial subspace are: $\displaystyle \large V$ itself and $\displaystyle \large \{0\}$

- The solution of a linear equation system $\displaystyle \large \boldsymbol{A}\boldsymbol{x} = \boldsymbol{0}$ with $\displaystyle \large n$ unknowns $\displaystyle \large \boldsymbol{n} = [x_1, \dots, x_n]$ *is a subspace of $\displaystyle \large \mathbb{R}^n$

- The solution of a linear equation system with $\displaystyle \large \boldsymbol{b} \ne \boldsymbol{0}$, $\displaystyle \large \boldsymbol{Ax} = \boldsymbol{b}$ is *not* a subspace of $\displaystyle \large \mathbb{R}^n$

![[Pasted image 20250116163606.png]]