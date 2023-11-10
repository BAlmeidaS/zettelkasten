---
tags:
  - Statistics
---
Regression Analysis is a [[Statistics|statistical]] method you use when both [[Response variable]] and [[Explanatory variable]] are [[Continuous variable|continuous variables]].

The simplest method is:
$$\displaystyle \Huge \begin{eqnarray} 
y &=& a + bx \\
a &\rightarrow& intercept \\
b &\rightarrow& slope
\end{eqnarray}$$

The parameters have the *maximum likelihood* with the data. In other words, *find the values of the slope and intercept that make the data most likely*. The math is defined on the [[least-squares]]



>[!R Lang]
>in `R` we can use `lm(df$resp_var~df$explan_var)`
>we read like *resp_var is modelled as a function of explan_var*

