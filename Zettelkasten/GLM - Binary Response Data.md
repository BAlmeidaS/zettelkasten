---
tags:
  - Statistics
---
In this case the [[Response variable]] follows the [[Bernoulli distribution]].

The idea here is fitting a [[logistic regression]] with the data.

>[!R lang]
>1. create a single vector containg 0s and 1s (or two factors)
>2. use `glm(y ~ x1*x2, family=binomial, data=df)`
>3. test significance by deletion of terms from the model and compare the changes in deviance with chi-squared -> [[Model Simplification - Model Complexity|model simplification]] using `anova` and `chi`

After, [[Interpreting results of logistic regression]].

Regarding the prediction,
>[!R lang]
>We can in R use the logistic regression to predict the probability $\displaystyle \large \in (0, 1)$ using the fitted model with `type="response"`:
>```R
>logist_m = glm(..., family="binomial")
>predict(logist_m, df, type="response")
>```
