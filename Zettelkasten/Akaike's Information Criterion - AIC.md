---
tags:
  - Statistics
---
*Unexplained variation* is bound to go down with every parameter added to the model. The limit we have a parameter for each data point ([[Types of simplification over Statistics Model|Saturated Model]]).

$\displaystyle \large AIC$ gives the usefulness of each parameter - [[Occam's Razor]]. $\displaystyle \large AIC$ penalises each parameter for being added (by default of $\displaystyle \large 2$), and only allow the parameter to stay if it pays itself.

When [[Model Simplification - Model Complexity|comparing models]] **the smaller the AIC the better the model**.
$$\displaystyle \Huge AIC = \text{deviance} +2p $$

Being $\displaystyle \large p$ the number of parameters.

---
Regarding `R`

The `AIC()` function and the starting AIC value reported by the `step()` function in R can indeed be different, and this discrepancy is usually due to the way the `step()` function operates and what it reports.

1. **AIC Function**: The `AIC()` function directly calculates the Akaike Information Criterion for the model you provide. It uses the formula:
    AIC=−2×log⁡(likelihood)+2×number of parametersAIC=−2×log(likelihood)+2×number of parameters
    
    This gives the AIC value for the model as it currently stands.
    
2. **Step Function**: The `step()` function in R is used for stepwise model selection, typically in a linear model. It can be used for both forward selection and backward elimination. The starting AIC value reported by `step()` is the AIC of the initial model provided to it.
    
    - However, the `step()` function sometimes includes an extra penalty term in its AIC calculation for the number of parameters. This can especially be the case with certain types of models or when certain options are set in the `step()` function.
    - Additionally, the `step()` function may handle certain constants or aspects of the model differently, which can affect the AIC calculation.
3. **Consistency in Comparisons**: When comparing AIC values, it's important to ensure that they are calculated in the same way. If you are using the AIC for model selection purposes, either stick with the `AIC()` function or the AIC values reported by `step()`, but do not mix them.