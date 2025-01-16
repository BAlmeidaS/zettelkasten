---
tags:
  - machine-learning
aliases:
  - PCA
---
A [[dimensionality reduction]] technique based on *Linear Algebra*.

The key idea behind *PCA* is to use [[The orthogonal projection into ND subspaces|orthogonal projections]] *to find lower dimension representations* of the data *retaining the maximum information as possible*.

##### Breakdown

Consider that you have the *dataset* $\displaystyle \large X$ with $\displaystyle \large n$ rows and $\displaystyle \large D$ features,
$$\displaystyle \Huge \begin{eqnarray} 
X = \{x_1,..., x_n\},\quad x_i \in\mathbb{R}^D
\end{eqnarray}$$

The objective is to find a *lower dimension representation* of X, that is as similar as possible.

Considering a [[orthonormal basis]] over $\displaystyle \large R^D$, $\displaystyle \large D = \{d_1, ...., d_n\}$, every vector on the [[vector space]] can be written with this basis:
$$\displaystyle \Huge \begin{eqnarray} 
x_n = \sum^D_{i=1}\beta_{in}d_i
\end{eqnarray}$$

so, $\displaystyle \large \beta_{in}$ can be interpreted as the [[The orthogonal projection into 1D subspaces| orthogonal projection of]] $\displaystyle \large x_n$ onto the 1-dimension [[vector subspace|subspace]] spammed by $\displaystyle \large d_i$,
$$\displaystyle \Huge \begin{eqnarray} 
\beta_{in} = x_n^Td_i
\end{eqnarray}$$

Considering, another [[orthonormal basis]] $\displaystyle \large B = \{b_1, ..., b_m\}, m \lt n$ , then $\displaystyle \large B$ defines a [[vector subspace]] and the [[The orthogonal projection into ND subspaces|orthogonal projection]] of $\displaystyle \large X$ onto this subspace $\displaystyle \large \tilde{X}$ is
$$\displaystyle \Huge \begin{eqnarray} 
\tilde{X} = B \overbrace{B^TX}^{\text{CODE}}
\end{eqnarray}$$

the *CODE* are the *coordinates of $\displaystyle \large X$ with respect to the basis $\displaystyle \large B$*.

**