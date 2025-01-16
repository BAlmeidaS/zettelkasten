---
tags:
  - Linear-algebra
aliases:
  - orthogonal decomposition
  - orthogonal decomposition theorem
  - i
---
The *orthogonal decomposition* of a [[vector]] $\displaystyle \large x \in \mathbb{R}^n$ is the sum of a vector in a [[vector subspace]] $\displaystyle \large V \in \mathbb{R}^n$  and a vector in the [[orthogonal complement of a subspace|orthogonal complement]] $\displaystyle \large V^\perp \text{ to } V$.

#### definition

The *orthogonal decomposition theorem* states that, if $\displaystyle \large V$ is a [[vector subspace|subspace]] of $\displaystyle \large \mathbb{R}^n$, than every vector $\displaystyle \large x$ in $\displaystyle \large \mathbb{R}^n$ can be written as:
$$\displaystyle \Huge \begin{eqnarray} 
&&x = \tilde{x} + z\\
\\ where, &&x \in V \text{ and } z \in V^\perp
\end{eqnarray}$$

Moreover, given an [[orthonormal basis]] of $\displaystyle \large V$, $\displaystyle \large \boldsymbol{u} = \{u_1, ..., u_n\}$, then:
$$\displaystyle \Huge \begin{eqnarray} 
\tilde{x} &=& 
\dfrac{\langle x, u_1 \rangle}{\langle u_1,u_1 \rangle} u_1 + 
\dfrac{\langle x, u_2 \rangle}{\langle u_2,u_2 \rangle} u_2 + 
\dots
+ \dfrac{\langle x, u_n \rangle}{\langle u_n,u_n \rangle} u_n
\end{eqnarray}$$

Thus, $\displaystyle \large \tilde{x}$ is the [[The orthogonal projection into ND subspaces|orthogonal projection]] of $\displaystyle \large x$ in onto the subspace $\displaystyle \large V$