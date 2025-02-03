---
tags:
  - Statistics
aliases:
  - r-squared
  - r^2
  - variation explained
---
The degree of fit, $\displaystyle \large r^2$, quantifies the degree of fit of a [[Regression Analysis|Linear Model]]
$$\displaystyle \Huge \begin{eqnarray} 
r^2 &=& 1 - \dfrac{SSE}{SSY} = \dfrac{SSR}{SSY} 
\\\\\ r^2 &\in&[0,1]

\end{eqnarray}$$
([[Sum of squares errors|SSE]], [[SSY]], [[SSR]])

In other words, **$\displaystyle \large r^2$ is the percentage of the *variation* that the model could explain.**

![[Pasted image 20231111183012.png|500]]

Another way to grasp is by using using [[Sum of squares errors|Sum of Squares]] here called as *variation* $\displaystyle \large Var$
$$\displaystyle \Huge \begin{eqnarray} 
r^2 
&=& \dfrac{SS(mean) - SS(fit)}{SS(mean)}
\\\\
&=& \dfrac{Var(mean) - Var(fit)}{Var(mean)}
\end{eqnarray}$$

Being, $\displaystyle \large Var(mean)$ as *the variance around the mean* and $\displaystyle \large Var(fit)$ the *variance around the fit*:
$$\displaystyle \Huge \begin{eqnarray} 
r^2 &=& 
\dfrac{ \sum{(y_i- \bar{y})} - \sum{(y_i- \hat{y}_i)} }{\sum{(y_i- \bar{y})} }
\\\\&=&
1 - \dfrac{ \sum{(y_i- \hat{y}_i)} }{\sum{(y_i- \bar{y})} }
\end{eqnarray}$$

---

- **Definition**: It measures the proportion of variance in the dependent variable that is predictable from the independent variables.
- **Use**: It gives you an overall idea of how well your model explains the variability of the response data.
- **Limitation**: It always increases as you add more [[Explanatory variable|independent variable]] to your model, regardless of whether those [[Explanatory variable|independent variable]] are actually meaningful. This can be misleading, especially with a large number of variables, as it might suggest a better fit than is truly the case - solution: [[Adjusted R-squared]]
---

>[!hint] The interpretation of r-squared
> if $\displaystyle \large r^2$ is 0.6 (or 60%) we understand as **x-variable explain 60% of the the variation of the y-variable**:
> ![[Pasted image 20250202204901.png]]
> alternatively:
> - *60% of the sum of squares of the y-variable can be explained by the x-variable*
> - *there is a 60% reduction in the [[Variance]] when we take the x-variable into account*:

The square root of this quantity is $\displaystyle \large r$ in [[Pearson's correlation]] and $\displaystyle \large \rho$ in [[Sperman's rank correlation]]
