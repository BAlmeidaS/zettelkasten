---
tags:
  - Statistics
---
Using [[Occam's Razor]], if the *simpler model does not explain significantly less of the variation in the response, then the simpler model is preferred*

> [!R Lang]
> Models can be compared using the function anova
> ```R
> m1 <- lm(...)
> m2 <- lm(...)
> anova(m1, m2)
>  ```
>  Returns a table with a [[One-Way Anova]] test, if *p-value is low (less than 0.05)*, than m2 is worse than m1, otherwise they are the same. The one with the highest value of D.F. (DF or Res.DF) is the the simplest one, and if it is not worse, should be the one chosen.

> [!R Lang]
> Other option is using the function `AIC`. With this one we simply get the one with the lower level.