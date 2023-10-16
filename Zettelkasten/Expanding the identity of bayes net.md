Considering that the nodes of the [[Bayesian Network|Bayes Net]] are in [[Topological Order]]
$$\displaystyle \Huge \begin{eqnarray} 
P(x_1, \dots,x_n) &=& P(x_1\land\dots\land x_n) \\
&=& P(x_n\mid x_{n-1},\dots,x_1) &\ \ \{1\}\\
& & * P(x_{n-1}\mid x_{n-2},\dots,x_1) \\
& & \dots \\
& & * P(x_2\mid x_1) \\
& & * P(x_1) \\
\\
P(X_i\mid X_{i-1},\dots X_1) &=& P(X_i\mid Parents(X_i)) & \{2\}
\end{eqnarray}$$
$\displaystyle \large \{1\}$: [[product rule of probability]]
  $\displaystyle \large P(x_1,\dots,x_n) = P(x_n\mid x_{n-1},\dots,x_1)P(x_{n-1},\dots,x_1)$
  
$\displaystyle \large \{2\}$: Definition of [[Bayesian Network|Bayes Net]]
$\displaystyle \large  P(x_1, \dots,x_n)  = \prod^n_{i=1}P(x_i\mid parents(X_i)) \\ $
