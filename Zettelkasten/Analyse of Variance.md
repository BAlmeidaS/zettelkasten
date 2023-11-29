---
tags:
  - Statistics
aliases:
  - Analyse of Variance
  - ANOVA
---
A [[Statistics]] technique that we use when *all the [[Explanatory variable|explanatory variables]] are [[Categorical variable|categorical]]*.

In this context, *explanatory variables are called **factors** and each factor has **two or more levels** (categories).

If we have:
- *1 Factor with 3 or more levels*: [[One-Way Anova]]
- *1 Factor with 2 levels*: [[Student's t test]] gives the same answer than [[Analyse of Variance|Anova]].
- *2 or more Factor*: [[Factorial Experiment]]

> [!R Lang]
> Models can be compared using the function anova
> ```R
> m1 <- lm(...)
> m2 <- lm(...)
> anova(m1, m2)
>  ```
>  Returns a table with a [[One-Way Anova]] test, if p-value is low, than m2 is worse than m1, otherwise they are the same. The one with the highest value of D.F. (DF or Res.DF) is the the simplest one, and if it is not worse, should be the one chosen.


