---
tags:
  - Statistics
---
[[One-Way Anova]] is about the [[Hypothesis Test]]. If we conclude that the means of the categorical are different we must find the model that best fit with this finding.

The model will be a [[Regression Analysis|Linear Model]]:
> [!R Lang]
> in `r` we can find the equivalent model for the anova with:
> ```R
> summary.lm(aov(df$dependent_var ~ df$independent_var))
>  ```

 ![[Pasted image 20231113173524.png|400]]

The *Intercept* will be the mean of the first category (alphabetical order, in this case `df$gardenA`).
The *second param* (in this case `df$gardenB`) is the *difference between the mean of the second category with the first category*.

In this case, so:
$$\displaystyle \Huge \begin{eqnarray} 
mean(gardenA) &=& 3 \text{ (intercept)} \\
mean(gardenB) &=& 5 \text{ (intercept + df\$gardenB)} \\
\end{eqnarray}$$

The Standard errors are calculated based on [[Standard Error of the mean]]. For the Intercept is the plain SE for the mean, and for the others will be the [[Standard error of the difference between two mean]]

> [!R Lang]
> The practical way in `r` to find the means should be
> ```R
> tapply(df$dependent_var, df$independent_var, mean)
>  ```
