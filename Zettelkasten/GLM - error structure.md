---
tags:
  - Statistics
---
There are many error that are **not** normally distributed (remember [[Model Checking - Linear Model|1 step one model check is normality of error]]) :
- errors that are strongly skewed
- errors that are [[Kurtosis|kurtotic]]
- errors that are strictly bounded -> [[Response Variable - Proportion Data]]
- errors that cannot lead to negative values -> [[Response Variable - Count Data]]

*One* way to deal with these type of error is with [[Non-parametric Method|non-parametric]] methods. *Another way* is with [[Generalised linear models|GLM]].

[[Generalised linear models|GLM]] allows specification of a variety of errors distributions:
- [[Poisson]] *errors* -> [[Response Variable - Count Data]]
- [[Binomial Distribution|Binomial]] *errors* -> [[Response Variable - Proportion Data]]
- [[Gamma Distribution|Gamma]] *errors* -> Data that shows a **constant** coefficient of variation
- [[Exponential Distribution|Exponential]] *errors* -> [[Response Variable - Age-at-death Data]]

>[!R lang]
>In `R` we can select the *family* of the *glm*:
>```R
>glm(y ~ z, family = poisson)
>glm(y ~ z, family = binomial)
> ```
> Which means that the response is Poisson or Binomial and the model has that type of error.



