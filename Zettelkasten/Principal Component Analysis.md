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
(2) \quad \beta_{in} = x_n^Tb_i
\end{eqnarray}$$

Considering, another [[orthonormal basis]] $\displaystyle \large B = \{b_1, ..., b_m\}, m \lt D$ (*which is the equivalent of cutting $\displaystyle \large B_0$*), then $\displaystyle \large B$ defines a [[vector subspace]] and the [[The orthogonal projection into ND subspaces|orthogonal projection]] of $\displaystyle \large X$ onto this subspace $\displaystyle \large \tilde{X}$ is
$$\displaystyle \Huge \begin{eqnarray} 
\tilde{X} = B \overbrace{B^TX}^{\text{CODE}}
\end{eqnarray}$$
the *CODE* are the *coordinates of $\displaystyle \large X$ with respect to the basis $\displaystyle \large B$*.

**The goal of PCA is to find this [[orthonormal basis]] $\displaystyle \large B$** that has the lowest error when compared to the original orthonormal basis $\displaystyle \large B_0$.

Any $\displaystyle \large \tilde{x}_n$ can be written as,
$$\displaystyle \Huge \begin{eqnarray} 
(3) \quad \tilde{x}_n = 
\overbrace{
\sum^m_{i=1}\beta_{in}b_i 
}^{\text{lives on m dimension subspace}}
+
\cancel{
\underbrace{\sum^D_{i=m+1} \beta_in}_{\text{ lives on d - m dimension subspace}} 
}
\quad\in\mathbb{R}^D
\end{eqnarray}$$

$\displaystyle \large (3)$ is the expansion of $\displaystyle \large (1)$. The second subspace (d-m dimension subspace), is [[orthogonal complement of a subspace|orthogonal complement]] of the first one.

**PCA _ignores_ the second term**, and it is related to "the error" that we want to minimise. More than that, $\displaystyle \large b_1, ..., b_m$ span the **principal subspace**.

by definition (since PCA ignores the second term), $\displaystyle \large \tilde{x}_n$ lives on a space of $\displaystyle \large D$ dimensions but it is represented with only $\displaystyle \large m$ coordinates $\displaystyle \large (\beta_1, ..., \beta_m)$.

##### The reconstruction error

*The average squared reconstruction error $\displaystyle \large J$*, [[loss function]], is defined as,
$$\displaystyle \Huge \begin{eqnarray} 
J = \dfrac{1}{N} \sum^N \lvert \lvert x_n - \tilde{x}_n \rvert \rvert ^ 2
\end{eqnarray}$$

In order to *minimise the error*, we need to find when the [[Grad of F|grad]]  of J is zero.

By computing the [[partial derivatives]] of $\displaystyle \large J$ with respect to the parameters of $\displaystyle \large J$, which are the $\displaystyle \large \beta_{in}$s and $\displaystyle \large b_i, i=1,...,m$. Using [[Chain rule - general form]]:
$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{\partial J}{\partial b_i} = 
\dfrac{\partial J}{\partial \tilde{x}_n} \dfrac{\partial \tilde{x}_n}{\partial b_i}
\\\\

\dfrac{\partial J}{\partial \beta_{in}} = 
\dfrac{\partial J}{\partial \tilde{x}_n} \dfrac{\partial \tilde{x}_n}{\partial \beta_{in}}

\end{eqnarray}$$

By definition of [[Chain rule - general form]]:
$$\displaystyle \Huge \begin{eqnarray} 
(4)\quad \dfrac{\partial J}{\partial \tilde{x}_n} = -\dfrac{2}{N}(x_n - \tilde{x}_n)^T
\end{eqnarray}$$
while, using $\displaystyle \large (2)$ we have:
$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{\partial J}{\partial \beta_{in}} &=&
\dfrac{\partial J}{\partial \tilde{x}_n}
\dfrac{\partial \tilde{x}_n}{\partial \beta_{in}}
\\\\
&&\text{from (2) we have that,}
\\
\dfrac{\partial \tilde{x}_n}{\partial \beta_{in}} &=& b_i
\\
&&\text{so, by using (4)}
\\\\
\dfrac{\partial J}{\partial \beta_{in}} &=& 
\dfrac{\partial J}{\partial \tilde{x}_n} * b_i, &\quad i=1,..., M
\\&=& 
-\dfrac{2}{N}(x_n - \tilde{x}_n)^T * b_i, &\quad i=1,..., M
\\
&&\text{and by using (3)}
\\\\
\dfrac{\partial J}{\partial \beta_{in}} &=& 
-\dfrac{2}{N}(x_n - \sum^M_{j=1}\beta_{in}b_i)^T * b_i, &\quad i=1,..., M
\\
&&\text{since B is orthonormal base,}
\\
&&\text{the only j that matters is the $i$th}
\\
&&\text{$b_j \cdot b_i$ is not 0 only when j = i}

\\\\
\dfrac{\partial J}{\partial \beta_{in}} &=& 
-\dfrac{2}{N}(x_n^Tb_i - \beta_{in}b_i^Tb_i) 

\end{eqnarray}$$
(We remove the *summation* because of the [[inner product]] of [[Orthogonal]] vectors)

Since we want to minimise the error, the *derivative must be 0* with the respect of the parameters,
$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{\partial J}{\partial \beta_{in}} &=& 
-\dfrac{2}{N}(x_n^Tb_i - \beta_{in}b_i^Tb_i)  = 0
\iff \beta_{in} = x_n^Tb_i \quad (5)
\end{eqnarray}$$
and this returns to equation $\displaystyle \large (2)$. *$\displaystyle \large \beta_{in}$ must be the projection of $\displaystyle \large x$ over the vector $\displaystyle \large b_i$*.

##### Rephrasing the loss

Reinterpreting $\displaystyle \large \tilde{x}_n$:
$$\displaystyle \Huge \begin{eqnarray} 
\tilde{x}_n 
&=& \sum^m_{j=1} \beta_{jn}b_j 
&\qquad\text{using (3)}
\\
&=& \sum^m_{j=1} (x_n^Tb_j)b_j 
&\qquad\text{using (5)}
\\
&=& (
\overbrace{
\sum^m_{j=1} b_jb_j^T
}^{\text{projection matrix}}
) x_n
&\qquad\text{cause inner are symmetric}
\end{eqnarray}$$

Reinterpreting $\displaystyle \large x_n$:
$$\displaystyle \Huge \begin{eqnarray} 
x_n = (\sum^m_{j=1} b_jb_j^T)x_n + (\sum^D_{j=m+1} b_jb_j^T)x_n
\end{eqnarray}$$

The *error will be based on the second term*, which is the [[orthogonal complement of a subspace|orthogonal complement]] of the *principal subspace*:
$$\displaystyle \Huge \begin{eqnarray} 
&x_n-\tilde{x}_n &=\ & (\sum^D_{j=m+1}b_jb_j^T)x_n
\\
(6) & \quad &=& (\sum^D_{j=m+1}b_j^Tx_n)b_j & \quad\text{symmetry of inner}
\end{eqnarray}$$
So the loss $\displaystyle \large J$ might be rewritten as (using the concept of [[Covariance]]),
$$\displaystyle \Huge \begin{eqnarray} 
J &=& 
\dfrac{1}{N} \sum^N_{n=1} \lvert \lvert x_n - \tilde{x}_n \rvert \rvert ^ 2
\\ &=&
\dfrac{1}{N} \sum^N_{n=1} \lvert \lvert \sum^D_{j=m+1} (b_j^Tx_n) b_j \rvert \rvert ^ 2
\quad\text{using (6)}
\\ &=&
\dfrac{1}{N} \sum^N_{n=1} \sum^D_{j=m+1} (b_j^Tx_n)^2  
\qquad\text{B is an orthonormal basis ($b_j^2 = 1$)}
\\ &=&
\dfrac{1}{N} \sum^N_{n=1} \sum^D_{j=m+1} b_j^Tx_nx_n^Tb_j
\\ && \text{we assumed that we have *centered* data (mean = 0),}
\\ && \text{so the we can get the covariance of $x_n$, called S}
\\ &=& 
\sum^D_{j=m+1}  b_j^T \left( \dfrac{1}{N}  \sum^N_{i=1} x_nx_n^T \right) b_j
\\ &=& 
\sum^D_{j=m+1}  b_j^T S b_j
\end{eqnarray}$$

This expression might be rewritten using the [[trace operator]]:
$$\displaystyle \Huge \begin{eqnarray} 
J &=& 
\sum^D_{j=m+1}  b_j^T S b_j
\\ &=& 
trace\left(\sum^D_{j=m+1}  b_jb_j^T\right)S
\end{eqnarray}$$

>[!tip] proof of using trace
>$$\displaystyle \Huge \begin{eqnarray} 
>b_j = \begin{bmatrix}  b^1_j \\ b^2_j \\ \vdots \\ b^D_j \end{bmatrix}
>,\quad S = 
>\begin{bmatrix} 
>S_{11} & S_{12} & \dots & S_{1D} \\ 
>\vdots & \vdots & \ddots & \vdots \\
>S_{D1} & S_{D2} & \dots & S_{DD} \\ 
>\end{bmatrix}
>\end{eqnarray}$$
>so, because $\displaystyle \large b_j$ is an [[orthonormal basis]], the [[inner product]] between different basis vectors will be 0:
>$$\displaystyle \Huge \begin{eqnarray} 
>\sum_j b_jb_j^T 
>&=&
>\begin{bmatrix} 
>\sum_j b^1_jb^1_j & \sum_j b^1_jb^2_j & \dots & \sum_j b^1_jb^D_j \\
>\vdots & \vdots & \ddots & \vdots  \\
>\sum_j b^D_jb^1_j & \sum_j b^D_jb^2_j & \dots & \sum_j b^D_jb^D_j \\
>\end{bmatrix}
>\\\\
>&=&
>\begin{bmatrix} 
>\sum_j b^1_jb^1_j & 0 & \dots & 0 \\
>\vdots & \vdots & \ddots & \vdots  \\
>0 & 0 & \dots & \sum_j b^D_jb^D_j \\
>\end{bmatrix}
>\end{eqnarray}$$
>
>So, the multiplication with S will get only the diagonal, so the [[trace operator|trace]].

Moreover, $\displaystyle \large \sum^D_{j=m+1}b_jb_j^T$ is a [[The orthogonal projection into ND subspaces|projection matrix]] to the [[orthogonal complement of a subspace|orthogonal complement]] of the *principal subspace*.

*since S is the [[Variance]]*, this means that, the **loss is the [[Variance]] projected onto the orthogonal complement of the principal subspace**. Therefore, by *minimising* the loss is equivalent to *minimising the [[Variance]] of the data that lies on the orthogonal subspace*!

>[!important] 
>*PCA* retains as much [[Variance]] after projection the data into the subspace as possible!

##### finding the orthonormal basis

We have so that the [[loss function]] is (being $\displaystyle \large S$, the [[Covariance Matrix]]),
$$\displaystyle \Huge \begin{eqnarray} 
J=\sum^D_{j=m+1}  b_j^T S b_j
\end{eqnarray}$$

we want to find $\displaystyle \large b_1, b_2, ...$ , but they have a *constraint*, they have to be build an [[orthonormal basis]], so,
$$\displaystyle \Huge \begin{eqnarray} 
b_i^Tb_j = 0, i \ne j
\\
b_i^Tb_i = 1
\end{eqnarray}$$

The error to *project* the data onto one vector of the basis, let's call it $\displaystyle \large i$:
$$\displaystyle \Huge \begin{eqnarray} 
&&J = b_i^TSb_i, 
\\
\text{with a constraint, }&& b_i^Tb_i = 1
\end{eqnarray}$$
To solve this *optimisation* we will use [[Lagrange Multiplier|Lagrangian]]:
$$\displaystyle \Huge \begin{eqnarray} 
\mathcal{L} = b_i^TSb_i + \lambda(1-b_i^Tb_i)
\end{eqnarray}$$
To minimise we will get its [[partial derivatives]] and set them to 0:
$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{\partial \mathcal{L}}{\partial\lambda} &=& 1 - b_i^Tb_i = 0
\\
&\iff& b_i^Tb_i = 1 \text{ (recover the constraint)}
\\ \\
\dfrac{\partial \mathcal{L}}{\partial\lambda} &=& 1 - b_i^Tb_i = 0

\end{eqnarray}$$