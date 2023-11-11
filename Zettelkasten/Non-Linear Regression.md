---
tags:
  - Statistics
---
*Non-linear Regressions* are similar to [[Regression Analysis|Linear Model]] but using non-linear transformation. One example can be the transformation:
$$\displaystyle \Huge y=a-be^{-cx}$$

>[!R lang]
>The main difference in `R` is the we will use `nls` (instead of lm) that stands for *nonlinear least squares*.
>Also, `nls` need a `start=`  parameter with some initial values for the model params (in the example: a, b and c)

