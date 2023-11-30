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

We prefer:
- a model with $\displaystyle \large n-1$ paramaters to a model with $\displaystyle \large n$ parameters
- a model with $\displaystyle \large k-1$ [[Explanatory variable]] to a model with $\displaystyle \large k$.
- a linear model to a curved model
- a model without a hump
- a model without interactions between variables

This means, we want to:
- remove non-significant interaction terms
- remove non-significant quadratic or non-linear terms
- remove non-significant explanatory variables
- group together factor levels that do not differ from one another
- set non-significant slopes of continuous explanatory variables to zero

Steps of model simplification are:
1. Fit the [[Types of simplification over Statistics Model|Maximal Model]]
2. Begin model simplification - check the parameters using `summary` - **Remember that order matters if variables are correlated!**
3. Deletion cause an *in*significant increase in [[Deviance]] (checked via *anova method*)? Use method `update -` to remove var and `update +` to add
	1. Yes? Remove and check the parameters again
	2. No? Put the term back
4. Keep removing terms from the model

> [!R Lang]
> ```R
> model <- lm(...)
> # removing features
> model2 <- update(model, ~. -col)
> ```
> 
> Other option is using the function [[Akaike's Information Criterion - AIC]]. With this one we simply get the one with the lower level.
> ```R
> step(model)
> ```

