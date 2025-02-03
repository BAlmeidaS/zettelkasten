---
tags:
  - Statistics
---
Using `r` often you will see two types of [[Degree of Fit - Linear Regression|r-squared]].

***Adjusted R-squared** is usually a **better choice** than [[Degree of Fit - Linear Regression|r^2]] for evaluating the overall effectiveness*

[[Degree of Fit - Linear Regression|r-squared]] always increases (or stays the same) when more independent variables are added to a regression model, even if those variables have little to no explanatory power.

**Adjusted R-sqiared**, however, *introduces a penalty for adding variables that do not improve the model significantly*. It adjusts for the number of predictors, preventing [[overfitting]].

$$\displaystyle \Huge \begin{eqnarray} 
r^2_{adj} = 1 - \left(\dfrac{(1 - r^2)(n-1)}{n-p-1}\right)
\end{eqnarray}$$
- $\displaystyle \large r^2$ is the [[Degree of Fit - Linear Regression|r-squared]] calculated
- $\displaystyle \large n$ is the number of *observations* / *datapoints*
- $\displaystyle \large p$ the number of [[Explanatory variable|independent variables]] used on the regression


