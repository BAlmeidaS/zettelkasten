---
tags:
  - Statistics
aliases:
  - Shapiro test
  - Shapiro Wilk test
---
*Shapiro test*  is a to test if some data is normally distributed. A test to serve a similar goal of [[Quantile-Quantile plot|Q-Q plot]]

[[Null Hypothesis|H0]]: Distribution is normally distributed
[[Alternative Hypothesis|H1]]: Distribution is NOT normally distributed

>[!R Lang]
>```R
>shapiro.test(df$col)
>```

The [[Test Statistic]] is *w* (collect more information later)
