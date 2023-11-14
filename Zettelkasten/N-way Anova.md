---
tags:
  - Statistics
aliases:
  - n-way
  - two-way
  - three-way
  - 2-way
  - 3-way
  - Higher-order anova
---
In [[Analyse of Variance|Anova]] and [[Factorial Experiment]], we can have *two-way*, *three-way*, or even *higher-order anova*. This means basically Anova with 2 or more [[Explanatory variable|explanatory variables]].

> [!R Lang]
> in `r` we can use:
> ```R
> two_way_anova_model <- aov(df$dep_var ~ df$ind_var_1 * df$ind_var_2)
> # this will create two-way interaction like ind_var_1:ind_var_2
> 
> three_way_anova_model <- aov(df$dep_var ~ df$ind_var_1 * df$ind_var_2 * df$ind_var_3)
> # this will create TWO-way INTERACTIONS like ind_var_1:ind_var_2, ind_var_1:ind_var_2 and ind_var_2:ind_var_3
> # this will also create THREE-way INTERACTIONS ind_var_1:ind_var_2:ind_var_3
>  ```
