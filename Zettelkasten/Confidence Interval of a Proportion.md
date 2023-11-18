---
tags:
  - Statistics
---
If you want to calculate the [[Confidence Interval]] of a propotion, one thing you can do is running a [[Binomial test|prop test]] of one-sample in R (in practice it will check if the proportion is 50%). With that you can get the CI over the mean that you want.

>[!R lang]
>With the following code you are going the CI of 95% of your proportion
>```R
>prop.test(490, 1000, conf.level = 0.9)
>```