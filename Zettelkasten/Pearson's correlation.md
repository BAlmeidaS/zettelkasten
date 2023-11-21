---
tags:
  - Statistics
---
It measures the linear [[Correlation]] between two variables $\displaystyle \large x$ and $\displaystyle \large y$.

It assumes that:
1. both variables are normally distributed
2. Relationship between variables is linear
3. Also assume that has no [[Heteroscedasticity]] - or it has Homoscedasticity

The `cor.test` in `R`, measures if there is a correlation and the p-value of it.
While just `cor` give you the raw correlation

[[Null Hypothesis|H0]]: There is no linear correlation or $\displaystyle \large r = 0$
[[Alternative Hypothesis|H1]]: There is linear correlation - depending on the test, we check by $\displaystyle \large \neq$  (two tailed), $\displaystyle \large r > 0$ (one tailed positive relation) or $\displaystyle \large r < 0$ (one tailed negative relation)

*Person test* is running a [[Student's t test|t test]] under the hood

>[!R Lang]
>```R
># computer the correlation
>cor(df$col1, df$col2)
># run the test
>cor.test(df$col1, df$col2)
>```
