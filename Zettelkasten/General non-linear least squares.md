---
tags:
  - math
  - Statistics
---
The goal here is similar to [[least-squares]] and [[how to find the best fit of linear regression]]. Although, the function here is not linear!

Thus, given a function $\displaystyle \large y$ of some variable $\displaystyle \large x$, and the function has $\displaystyle \large k$ parameters, $\displaystyle \large a_k$:
$$\displaystyle \Huge \begin{eqnarray} 
y(x;a_k),\ k = 1\dots m
\end{eqnarray}$$
These parameters $\displaystyle \large a_k$ define a non-linear relation between $\displaystyle \large x$ and $\displaystyle \large y$.
>[!example] example of non linear function with k = 2
> $$\displaystyle \Huge \begin{eqnarray} 
> y(x; a_1, a_2) = (x-a_1)^2 + a_2
> \end{eqnarray}$$

The goal is to *find the best $\displaystyle \large a_k$ parameters that better explain the relation of all the datapoints*, in other words, all the tuples $\displaystyle \large (y_i, x_i)$. 

Or we can be even more specific and fit the parameters to the triple tuple $\displaystyle \large (y_i, x_i, \sigma_i)$, where $\displaystyle \large \sigma_i$ is the uncertainty of the value $\displaystyle \large y_i$ given $\displaystyle \large x_i$.

As on [[how to find the best fit of linear regression]], we want to find the min of $\displaystyle \large \chi^2$, being it the squared error of each points normalised by the uncertainty (if there is no $\displaystyle \large \sigma_i$ consider it 1).

$$\displaystyle \Huge \begin{eqnarray} 
given, \\
&\chi^2 = \sum^n_{i=1}\dfrac{[y_i-y(x_i;a_k)]^2}{\sigma^2}
\\
\text{the goal is finding:}\\
&\nabla\chi^2 = 0
\end{eqnarray}$$

Since the function is not linear, we will do it [[iteration|iteratively]] rather then *analytics* as we did on [[how to find the best fit of linear regression]]. So:
$$\displaystyle \Huge \begin{eqnarray} 
a_{k_{next}} = a_{k_{cur}} - constant * \nabla\chi^2
\end{eqnarray}$$

To find the [[Grad of F|Grad of chi-square]] one needs to differentiate with respect to each $\displaystyle \large a_k$ (*pay attention that is not differentiate the function **BUT** the $\displaystyle \large \chi^2$*):
$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{\partial \chi^2}{\partial a_k}
= \sum^n_{i=1}-2\dfrac{[y_i-y(x_i;\boldsymbol{a})]}{\sigma^2}*\dfrac{\partial y(x_i;\boldsymbol{a})}{\partial a_k}
\end{eqnarray}$$


