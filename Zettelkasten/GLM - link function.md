---
tags:
  - Statistics
---
The transformation to be after the [[GLM - linear predictor]] to get the result in the same "scale" of the [[Response variable]]. The function to do this is the *link function*.

The *link function $\displaystyle \large g$ relates the mean value of $\displaystyle \large y$ to its linear predictor $\displaystyle \large \eta$ *:
$$\displaystyle \Huge \eta=g(\mu)$$

*This is not $\displaystyle \large y$!* The value of $\displaystyle \large \eta$ is obtained by transforming the value of $\displaystyle \large y$ by the *link function*, and the predicted value of $\displaystyle \large y$ is obtained by applying the inverse link function to $\displaystyle \large \eta$.

*An important criterion in the choice of link function is to ensure that the fitted values stay within reasonable bounds*. If the response is a percentage, the link function will guarantee that the return will be between 0 and 1, and so on.

**The most appropriate link function is the one which produces the minimum residual deviance**. By using different link functions, the performance of a variety of models can be compared. The total [[Deviance]] is the same in each case, and we can evaluate how the changes on the [[GLM - linear predictor|linear predictor]] are behaving.
