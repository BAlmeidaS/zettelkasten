---
tags:
  - Statistics
---
The linear predictor is the model to be fit from the data. It has, at least, as many parameters as it has [[Explanatory variable|explanatory variables]] and they are *estimated from the data*.

It can have more parameters than variables, example is *intercept* and in *Anova* when the *variables are correlated - covariates*.

>[!R lang]
> The linear predictor can always be interpreted with:
> ```R
> summary.lm(...)
> ```

One of the advantages of [[Generalised linear models|GLM]] is that we can compare different models with *one unique* measurement among them, the measurement of [[Deviance]].