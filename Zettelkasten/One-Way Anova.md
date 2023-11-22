---
tags:
  - Statistics
---
It is a test that we use when there is one [[Categorical variable]] as [[Explanatory variable]].

The idea is to *validate if different categories (levels) of the categorical variable have an impact on the [[Response variable|dependent variable]]*. For that, we will compare the total mean of the distribution with the means of each individual category and try to conclude if it is better to handle the data in isolation, or in total

It is a [[Parametric Method]] that assumes:
- Normality: Data in each group should be normal distributed
- Homogeneity of Variances: The variances in each group should be similar

[[Null Hypothesis|H0]]: There is no difference between the group means
[[Alternative Hypothesis|H1]]: At least one group mean is different from the others

The sum of Squares in y, [[SSY]], will be divided in [[SSA]] and [[Sum of squares errors|SSE]]:
$$\displaystyle \Huge SSY = SSA + SSE$$

The [[Test Statistic]] will be the **F-Ratio** from the [[Anova Table - Linear Model Summary|Anova Table]], between *the mean square of SSA* and *the mean square of Error*.

Then we can calculate the p-value with `1 - pf(f-ratio, d.f._ind_var, d.f._error)`

> [!R Lang]
> in `r` we can use:
> ```R
> anova_model <- aov(df$dependent_var ~ df$independent_var)
> summary(anova_model)
> plot(anova_model)
>  ```

