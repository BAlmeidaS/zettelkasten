---
tags:
  - Statistics
---
If you want to calculate the [[Confidence Interval]] of the [[Average|Mean]] over a sample, one thing you can do is running a [[Student's t test|t test]] of one-sample in R (in practice it will check if the mean is zero). with that you can get the CI over the mean that you want.

>[!R lang]
>With the following code you are going to find the mean of col and its CI 90%
>```R
>t.test(df$col, conf.level = 0.9)
>```
