---
tags:
  - Statistics
---
A factorial experiment has *two or more factors* ([[categorical variable]] as [[Explanatory variable|independent variable]]) each *with two or more **levels*** (# of categories).

We can investigate statistical interaction in which the *response to one factor depends on the level of another factor*. Also, we must understand the interaction among the [[Explanatory variable|independent variable]], and put this on the analysis.

> [!R Lang]
> If the data has 2 or more categories we must consider the interaction between them, not only with the independent variable. Therefore, the right model is *not only*:
> $$\displaystyle \Huge ind\_var \sim dep\_var\_a + dep\_var\_b$$
> *but*, because it is a **FACTORIAL EXPERIMENT**:
> $$\displaystyle \Huge ind\_var \sim dep\_var\_a + dep\_var\_b + dep\_var\_a:dep\_var\_b $$
> The shorcut to create such model is using the operator `*`:
> ```R
> model <- aov(df$tgt ~ df$col_a * df$col_b)
> ```

We can conclude that:
- **Both Independent Variables and Their Interaction Are Significant**:
	If `var_a`, `var_b`, and the interaction term `var_a:var_b` all have low p-values, it suggests that both variables independently affect the dependent variable, and additionally, the effect of one variable depends on the level of the other variable.
- **Both Independent Variables Are Significant, But Their Interaction Is Not**:
	If `var_a` and `var_b` are significant (low p-values) but `var_a:var_b` is not (high p-value), it suggests that each variable independently influences the dependent variable, but the effect of one variable does not depend on the level of the other.
- **Both Independent Variables Are Not Significant, But Their Interaction Is**:
	If `var_a` and `var_b` are not significant (high p-values) but `var_a:var_b` is significant (low p-value), it indicates that the variables do not have a significant independent effect on the dependent variable, but there is a combined effect that depends on the interaction of the two variables.
- **Only One Independent Variable Is Significant**:
	If only `var_a` or `var_b` is significant, it suggests that only that variable has an independent effect on the dependent variable. The significance of the interaction term `var_a:var_b` would then inform whether the effect of this significant variable depends on the level of the other variable.

 
> [!R Lang]
> Always use `summary.lm` to understand which params has low p-value and will be used on the final model! If from the 12 params, only 5 has low p-value, only those 5 will be composed on the final model.
>
> ```R
> model <- aov(df$tgt ~ df$col_a * df$col_b)
> summary.lm(model)
> ```
