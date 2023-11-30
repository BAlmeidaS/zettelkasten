---
tags:
  - Statistics
---
In this case the [[Response variable]] follows the [[Bernoulli distribution]].

The idea here is fitting a [[logistic regression]] with the data.

>[!R lang]
>1. create a single vector containg 0s and 1s (or two factors)
>2. use `glm(y ~ x1*x2, family=binomial, data=df)`
>3. link function is generally made by tryiung both links and selecting the link that gives the lower [[Deviance]].
>4. 