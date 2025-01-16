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

Considering a [[orthonormal basis]] over $\displaystyle \large R^D$, $\displaystyle \large B_0 = \{b_1, ...., b_D\}$, every vector on the [[vector space]] can be written with this basis:
$$\displaystyle \Huge \begin{eqnarray} 
(1) \qquad x_n = \sum^D_{i=1}\beta_{in}b_i
\end{eqnarray}$$

so, $\displaystyle \large \beta_{in}$ can be interpreted as the [[The orthogonal projection into 1D subspaces| orthogonal projection of]] $\displaystyle \large x_n$ onto the 1-dimension [[vector subspace|subspace]] spanned by $\displaystyle \large b_i$,
$$\displaystyle \Huge \begin{eqnarray} 
\beta_{in} = x_n^Tb_i
\end{eqnarray}$$

Considering, another [[orthonormal basis]] $\displaystyle \large B = \{b_1, ..., b_m\}, m \lt D$ (*which is the equivalent of cutting $\displaystyle \large B_0$*), then $\displaystyle \large B$ defines a [[vector subspace]] and the [[The orthogonal projection into ND subspaces|orthogonal projection]] of $\displaystyle \large X$ onto this subspace $\displaystyle \large \tilde{X}$ is
$$\displaystyle \Huge \begin{eqnarray} 
\tilde{X} = B \overbrace{B^TX}^{\text{CODE}}
\end{eqnarray}$$
the *CODE* are the *coordinates of $\displaystyle \large X$ with respect to the basis $\displaystyle \large B$*.

**The goal of PCA is to find this [[orthonormal basis]] $\displaystyle \large B$** that has the lowest error when compared to the original orthonormal basis $\displaystyle \large B_0$.

Any $\displaystyle \large \tilde{x}_n$ can be written as,
$$\displaystyle \Huge \begin{eqnarray} 
(2) \quad \tilde{x}_n = 
\overbrace{
\sum^m_{i=1}\beta_{in}b_i 
}^{\text{lives on m dimension subspace}}
+
\underbrace{\sum^D_{i=m+1} \beta_in}_{\text{ lives on d - m dimension subspace}} \quad\in\mathbb{R}^D
\end{eqnarray}$$

$\displaystyle \large (2)$ is the expansion of $\displaystyle \large (1)$. The second subspace (d-m dimension subspace), is [[orthogonal complement of a subspace|orthogonal complement]] of the first one.

**PCA _ignores_ the second term**, and it is related to "the error" that we want to minimise. More than that, $\displaystyle \large b_1, ..., b_m$ span the **principal subspace**.

by definition (since PCA ignores the second term), $\displaystyle \large \tilde{x}_n$ lives on a space of $\displaystyle \large D$ dimensions but it is represented with only $\displaystyle \large m$ coordinates $\displaystyle \large (\beta_1, ..., \beta_m)$.

##### The reconstruction error

*The average squared reconstruction error $\displaystyle \large J$* is defined as,
$$\displaystyle \Huge \begin{eqnarray} 
J = \dfrac{1}{N} \sum^N \lvert \lvert x_n - \tilde{x}_n \rvert \rvert ^ 2
\end{eqnarray}$$

By computing the [[partial derivatives]] of $\displaystyle \large J$ with respect to the parameters of $\displaystyle \large J$, which are the $\displaystyle \large \beta_{in}$s and $\displaystyle \large b_i, i=1,...,m$. By using [[Chain rule - general form]]:
$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{\partial J}{\partial b_i} = 
\dfrac{\partial J}{\partial \tilde{x}_n} \dfrac{\partial \tilde{x}_n}{\partial b_i}
\\\\

\dfrac{\partial J}{\partial \beta_{in}} = 
\dfrac{\partial J}{\partial \tilde{x}_n} \dfrac{\partial \tilde{x}_n}{\partial \beta_{in}}

\end{eqnarray}$$




