---
tags:
  - Statistics
---

Very similar with [[chi-squared test]], but you must use it when **one or more of the expected frequencies are less than 5**

[[Null Hypothesis|H0]]:  *The two categories are independent* / There is no significant association between the categorical variables
[[Alternative Hypothesis|H1]]:  *The two categories are dependent on each other* / There is a significant association between the categorical variables

> [!R Lang]
> ```R
> fisher.test(contigency.table)
> # or
>fisher.test(df$col_a, df$col_b)
>```
