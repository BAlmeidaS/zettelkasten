---
tags:
  - Statistics
---
A situation in statistical modelling where the [[Variance]] of the [[Deviation|Residual]] is not the same with the mean of the [[Response variable]]. Or is not the same across all levels of the [[Explanatory variable]].

In simple terms, *heteroscedasticity* is when the spread or variability of a set of data changes across different values of another variable or over a certain range.

In my own words:
*So heteroscedasticity is when the variance is not the same across all the data. So, for some values of my explanatory variables, I have a spread bigger (or smaller) of my response variable in comparison with other values.*

![[Pasted image 20231105202400.png|500]]
(on the left is what we want to see: no trend in the residual with the fitted values)
(on the right there is a problem. A clear pattern of increasing residual as the fitted values get larger)

>[!R lang]
>During the course, we saw that many times when we observe heteroscedasticity, applying a `log transformation` on Y, helps to reduce:
>```R
>model <- lm(log(y) ~ x1 * x2 + I(x1^2), data=df)
>```
