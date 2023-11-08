---
tags:
  - Statistics
---
It is the "[[Non-parametric Method|non-parametric]]" version of [[Pearson's correlation]], it calculates $\displaystyle \large \rho$ and it measures *monotonic* relationships rather than just *linear*.

It just assume that the variables are *ordinal*, so it has a ranking between the values, not necessarily 2 is the "double" of 1, but certainly is bigger.

[[Null Hypothesis|H0]]: There is no *monotonic relationship* between the variables
[[Alternative Hypothesis|H1]]: There is a monotonic relationship between the variables - depending on the test, we check by $\displaystyle \large \neq$  (two tailed), $\displaystyle \large r > 0$ (one tailed positive relation) or $\displaystyle \large r < 0$ (one tailed negative relation)

In `R` you can run `cor.test(df$col_a, df$col_b, method="spearman")`
