---
tags:
  - Linear-algebra
aliases:
  - projection matrix for 1 dimension subspace
---
This is a generalisation of [[Vector projection]].

The goal here is, given a vector $\displaystyle \large x$ and a [[vector space|subspace]] $\displaystyle \large U$, where $\displaystyle \large b$ is its [[basis]], we want to find *orthogonal projection onto $\displaystyle \large U$, $\displaystyle \large \pi_U(x)$*.

![[Pasted image 20250115190526.png|500]]

Since $\displaystyle \large \pi_x$ is an element of U, we can define as
$$\displaystyle \Huge \begin{eqnarray}
\pi_u(x) = \lambda b
\end{eqnarray}$$
and the vector that is the difference between the projection and $\displaystyle \large x$ is orthogonal to $\displaystyle \large b$ following the defined [[inner product]],
$$\displaystyle \Huge \begin{eqnarray} 
\langle b, \pi_u(x) - x \rangle = 0
\end{eqnarray}$$


*with the above definition we have:*
$$\displaystyle \Huge \begin{eqnarray} 
&& \langle b, \pi_u(x) - x \rangle = 0
\\ \iff &&
\langle b, \pi_u(x) \rangle - \langle b,x \rangle = 0
\\ \iff &&
\langle b, \lambda b\rangle - \langle b,x \rangle = 0
\\ \iff &&
\lambda \lvert \lvert b \rvert \rvert^2 - \langle b, x \rangle = 0
\\ \iff &&
\lambda = \dfrac{\langle b,x \rangle}{\lvert \lvert b \rvert \rvert ^ 2}
\end{eqnarray}$$
so, 
$$\displaystyle \Huge \begin{eqnarray} 
\pi_u(x) &=& \lambda b
\\ &=&
\dfrac{\langle b, x \rangle}{\lvert \lvert b \rvert \rvert^2} b
\end{eqnarray}$$

if we define the [[inner product]] as the [[dot product]]:
$$\displaystyle \Huge \begin{eqnarray} 
\pi_u(x) &=& 
\dfrac{b^Txb}{\lvert \lvert b \rvert \rvert^2} = 
\dfrac{bb^T}{\lvert \lvert b \rvert \rvert^2}x
\end{eqnarray}$$

this is the **projection matrix**:
$$\displaystyle \Huge \begin{eqnarray} 
\text{projection matrix} = \dfrac{bb^T}{\lvert \lvert b \rvert \rvert^2}
\end{eqnarray}$$

$$\displaystyle \Huge \begin{eqnarray} 
\begin{bmatrix}  & 1 \\ \end{bmatrix}
\end{eqnarray}$$

**See that the projection matrix only depends on $\displaystyle \large b$**.
With only the $\displaystyle \large b$ vector we can *define a projection matrix that allows us to project **any** vector $\displaystyle \large x \in \mathbb{R^k}$.

The *projection matrix* is:
- symmetric
$$\displaystyle \Huge \begin{eqnarray} 
bb^T = (bb^T)^T
\end{eqnarray}$$
- squared 
$$\displaystyle \Huge \begin{eqnarray} 
dim(bb^T) = k \times k
\end{eqnarray}$$

>[!note]
>if the vector $\displaystyle \large b$ is [[unit vector]] than we get even simpler results:
>$$\displaystyle \Huge \begin{eqnarray} 
>\lambda &=& b^Tx 
>\\
>\pi_u(x) &=& bb^Tx
>\end{eqnarray}$$

The projection $\displaystyle \large \pi_u(x)$ is *still a vector in $\displaystyle \large \mathbb{R}^d$, but it can be defined using only $\displaystyle \large \lambda$, since we have the vector $\displaystyle \large b$.

>[!example]
>![[Pasted image 20250115194116.png|500]]
