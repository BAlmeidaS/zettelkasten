---
tags:
  - Statistics
---
A test to *compare variances* of 2 distributions.

**When the variances are different, don't compare the means**

```R
var.test(x, y)
```

This `var.test` will give you the p-value of the two distributions having the same variance

> [!Math]
> The p-value in the context of F-test envolves F-distributions based on *degrees of freedom*.
> The easiest way to calculate in R is to define the comulative probability of the F distribution using `pf`:
> ```R
> 1 - pf( var(x) / var(y), degrees_of_freedom(x), degrees_of_freedom(y) )




