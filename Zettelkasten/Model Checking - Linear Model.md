---
tags:
  - Statistics
---
On `R` we can plot the [[Regression Analysis|Linear Model]] trying to understand how well it fits:

>[!R lang]
>```R
>model <- lm(...)
>par(mfrow=c(2,2))
>plot(model)
>```

![[Pasted image 20231111184054.png]]

**The top two graphs are the most important ones**

*the top-left* - shows the [[Deviation|residuals]]. Ideally the point should look like "the sky at night", without any type of bias. It is a problem if the scatter increases of decreases along the x.

*the top-right* - Is to check if the [[Deviation|residuals]] are normally distributed. It is a problem when there is an S-shaped or banana-shaped.

*the bottom-left*: Like the top-left but in different scale, it is the squared root of the residuals. Again the problem is if the points have a triangle distribution (◄ or ►)

*the bottom-right*: It highlights [[Influence - Linear Model|influential points]]. Another way to see the same info is `influence.measures(model)`

**Important takeaway: ALWAYS do model checking, don't end up on the summary(model)**