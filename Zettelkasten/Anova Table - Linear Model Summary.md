---
tags:
  - Statistics
aliases:
  - Anova Table
---
A table that shows all the core components of a [[Regression Analysis|Linear Model]]:
>[!R lang]
>```R
>model <- lm(df$dependent_var ~ df$indep_var_1 + df$indep_var_2)
># summary of the linear model
>summary(model) 
># anova table
>summary.aov(model)
>```

| Source     | Sum of Squares                 | [[Degrees of Freedom]]                         | Mean Squares | [[Degree of Fit - Linear Regression]] |
| ---------- | ------------------------------ | ---------------------------------------------- | ------------ | ----------- |
| Regression | [[SSR]]                        | $\displaystyle \large num\_of\_slopes$         | *regression variance*             |   $\displaystyle \large \dfrac{regression\ variance}{error\ variance}$          |
| Error      | [[Sum of squares errors\|SSE]] | $\displaystyle \large n - 1 - num\_of\_slopes$ | *error variance*              |             |
| Total      | [[SSY]] ([[SSY = SSR + SSE]])  | $\displaystyle \large n - 1$                   |              |             |

$\displaystyle \large num\_of\_slopes$ stands for the number of [[Explanatory variable]] in the model. The real math is the $\displaystyle \large df_{regression} = total\ num\ of\ paramater - 1$, but the "total num of params" is the total number of slopes + intercept (that we do not want, thus, the $\displaystyle \large -1$).

In this context,  $\displaystyle \large Mean\ Squares = \dfrac{Sum\ of\ Squares}{Degrees\ of\ Freedom}$, so:
$$\displaystyle \Huge \begin{eqnarray} 
regression\ variance &=& \dfrac{SSR}{num\_of\_slopes} \\\\
error\ variance &=& \dfrac{SSE}{n - 1 - num\_of\_slopes} \\
\end{eqnarray}$$

Finally the *F Ratio* is the [[Test Statistic]] for the [[Regression Analysis|Linear Model]]

The [[p-value]] is calculated using the *f distributions* based on both [[Degrees of Freedom]]

> [!R lang]
> The critical value of *F ratio*, for an $\displaystyle \large \alpha=0.05$ can be found with
> ```R
> qf(0.95, regression_d.f., error_d.f.)
> ```
> or, the **p-value** can be calculated with
> ```R
> 1 - pf(f_ratio, regression_d.f., error_d.f.)
> ```

The *summary* ends with the [[Standard Error of the Regression Slope]] and the [[Standard Error of the Intercept]]