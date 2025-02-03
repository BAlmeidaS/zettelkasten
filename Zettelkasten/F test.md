---
tags:
  - Statistics
aliases:
  - F test
  - Fisher's F test
  - var test
  - f-test
---
A test to *compare variances* of 2 distributions.

[[Null Hypothesis|H0]]: Variances are not significantly different
[[Alternative Hypothesis|H1]]: Variances are different

*When the [[Variance|variances]] are different, don't compare the [[Average|means]]*

```R
var.test(x, y)
```

This `var.test` will give you the p-value of the two distributions having the same variance

> [!Math with R]
> The p-value in the context of F-test envolves F-distributions based on *degrees of freedom*.
> The easiest way to calculate in R is to define the comulative probability of the F distribution using `pf`:
> ```R
> 1 - pf( var(x) / var(y), degrees_of_freedom(x), degrees_of_freedom(y) )

the number above is the [[Test Statistic]] of the F-test


