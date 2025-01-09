---
tags:
  - Statistics
aliases:
  - affine
---
If we apply a [[linear transformation]] over a dataset, the [[Variance]] will change in the following way:

Given a dataset $\displaystyle \large D$, it's variance can be defined:
$$\displaystyle \Huge \begin{eqnarray} 
Var[D] = E[(D-\mu)(D-\mu)^T]
\end{eqnarray}$$

If we apply a [[linear transformation]] $\displaystyle \large A$ to the dataset D, we have:
$$\displaystyle \Huge \begin{eqnarray} 
Var[AD + b] 
&=& E[(AD + b - A\mu - b)(AD + b - A\mu - b)^T] \\
&=& E[(AD-A\mu)(AD-A\mu)^T] \\
&=& E[A(D-\mu)(D-\mu)^TA^T] \\
&=& AE[(D-\mu)(D-\mu)^T]A^T \\
&=& AVar[D]A^T
\end{eqnarray}$$
