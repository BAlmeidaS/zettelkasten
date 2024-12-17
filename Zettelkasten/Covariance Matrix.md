---
tags:
  - Statistics
---
A *Covariance Matrix*, defined as $\displaystyle \large \Sigma$, is a matrix that contains all [[Covariance|covariances]] from each pair of features of a dataset, and the [[Variance]] of the features.

#### Definition

Given a dataset $\displaystyle \large \boldsymbol{X}$, with $\displaystyle \large n$ observation and $\displaystyle \large d$ variables:
$$\displaystyle \Huge \begin{eqnarray} 
\boldsymbol{X} 
= \begin{bmatrix}  X_1 \\ X_2 \\ \vdots \\ X_n \end{bmatrix}
= \begin{bmatrix} 
x_{11} & x_{12} & \dots & x_{1d} \\
x_{21} & x_{22} & \dots & x_{2d} \\
\vdots &  \vdots &  \ddots & \vdots \\
x_{n1} & x_{n2} & \dots & x_{nd} \\
\end{bmatrix}
\end{eqnarray}$$

The *covariance matrix* $\displaystyle \large \Sigma$ is defined as:
$$\displaystyle \Huge \begin{eqnarray} 
\Sigma_{ij} = Cov(X_i, X_j) = \dfrac{1}{n-1}
\sum^n_{k=1}
(x_{k,i} - \bar{x}_i)
(x_{k,j} - \bar{x}_j)
\end{eqnarray}$$

where:
- $\displaystyle \large \bar{\boldsymbol{X}}$ is the mean of each column/variable: $\displaystyle \large \bar{\boldsymbol{X}}_j = \dfrac{1}{n}\sum^n_{i=1}x_{ij}$ 
- $\displaystyle \large \boldsymbol{X} - \bar{\boldsymbol{X}}$ is the matrix obtained by subtracting the column means from each row

The *covariance matrix* $\displaystyle \large \Sigma$ is :
- [[symmetric matrix]] and *squared* $\displaystyle \large d \times d$
- *Positive Semi-Definite*, which means $\displaystyle \large z^T\Sigma z \ge 0$  for any positive vector $\displaystyle \large z$.
- *Diagonal entries*: are the [[Variance]] of the variables
- *Off-Diagonal entries*: are the [[Covariance]], they can be positive, negative, or zero, depending on the relationship between the variables


$$\displaystyle \Huge \begin{eqnarray} 
\Sigma := \begin{bmatrix} 
Var(X_1) & Cov(X_1, X_2) &  \dots & Cov(X_1, X_d) \\
Cov(X_2, X_1) & Var(X_2) & \dots & Cov(X_1, X_d) \\
\vdots &  \vdots &  \ddots & \vdots \\
Cov(X_d, X_1) & Cov(X_d, X_d) & \dots & Var(X_d) \\
\end{bmatrix}
\end{eqnarray}$$
