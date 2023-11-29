---
tags:
  - Statistics
---
The linear predictor is the model to be fit from the data. It has, at least, as many parameters as it has [[Explanatory variable|explanatory variables]] and they are *estimated from the data*.

It can have more parameters than variables, example is *intercept* and in *Anova* when the *variables are correlated - covariates*.

in math terms, the linear predictor is defined as $\displaystyle \large \eta$ (eta) and its value for a record $\displaystyle \large i$ is defined as:
$$\displaystyle \Huge \eta_i = \sum^p_{j=1}x_{ib}\beta_{j}$$

>[!R lang]
> The linear predictor can always be interpreted with:
> ```R
> summary.lm(...)
> ```

One of the advantages of [[Generalised linear models|GLM]] is that we can compare different models with *one unique* measurement among them, the measurement of [[Deviance]].

*To determine the fit of a given model, a GLM evaluates the [[GLM - linear predictor|linear predictor]] for each value of the response variable, the back-transforms the predicted value to compare it with the observed value of y. The parameters are then adjusted, and the model refitted on the transformed scale in an iterative procedure until the fit stops improving.*