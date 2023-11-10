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

The parameters have the *maximum likelihood* with the data. In other words, *find the values of the slope and intercept that make the data most likely*. The math behind is on [[least-squares]]. 

The *difference* between the *fitted line and the original data point* is called [[Deviation|Residual]] (in red):
![[Pasted image 20231110164148.png|400]]

The [[Maximum Likelihood]] model is defined as *the model that minimises the sum of the squares of the residuals*.

Being a residual $\displaystyle \large d_i$ defined as:
$$\displaystyle \Huge \begin{eqnarray} 
d_i &=& y_i - \hat{y_i} \\
d_i &=& y_i - (a+xb_i)  \\
&=& y_i - a - bx_i \\
\end{eqnarray}$$

>[!R Lang]
>in `R` we can use `lm(df$resp_var~df$explan_var)`
>we read like *resp_var is modelled as a function of explan_var*

