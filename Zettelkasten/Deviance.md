---
tags:
  - Statistics
---
The *deviance* is a general name of *model fit*.
$$\displaystyle \Huge deviance = -2 * ln(likelihood)$$

The log likelihood depends on the *model* defined on the [[Generalised linear models|GLM]].

For [[Regression Analysis|Linear Models]] since the model has *constant variance* and *normal errors* the [[Variance]] is **EQUAL** to the *Deviance*.

For other methods, *deviance* is mapped:

| Model      | Deviance                                              | Error    | Link       |
| ---------- | ----------------------------------------------------- | -------- | ---------- |
| linear     | $\displaystyle \large \sum(y-\bar{y})^2)$             | Gaussian | identity   |
| log linear | $\displaystyle \large 2\sum y\log(\dfrac{y}{\hat{y}})$ | Poisson  | log        |
| logistic   | $\displaystyle \large 2\sum y\log\left(\dfrac{y}{\hat{y}}\right)+(n-y)\log\left(\dfrac{n-y}{n-\hat{y}}\right)$  | binomial | logit           |
| gamma      | $\displaystyle \large 2\sum\dfrac{y-\hat{y}}{y} - log\left(\dfrac{y}{\hat{y}}\right)$            | gamma    | reciprocal |



