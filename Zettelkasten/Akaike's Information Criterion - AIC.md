---
tags:
  - Statistics
---
*Unexplained variation* is bound to go down with every parameter added to the model. The limit we have a parameter for each data point ([[Types of simplification over Statistics Model|Saturated Model]]).

$\displaystyle \large AIC$ gives the usefulness of each parameter - [[Occam's Razor]]. $\displaystyle \large AIC$ penalises each parameter for being added (by default of $\displaystyle \large 2$), and only allow the parameter to stay if it pays itself.

When [[Model Simplification - Model Complexity|comparing models]] **the smaller the AIC the better the model**.
$$\displaystyle \Huge AIC = \text{deviance} +2p $$

Being $\displaystyle \large p$ the number of parameters.