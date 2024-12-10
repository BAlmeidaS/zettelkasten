---
tags:
  - Statistics
aliases:
  - Linear Regression
  - Linear Model
---
Regression Analysis is a [[Statistics|statistical]] method you use when both [[Response variable]] and [[Explanatory variable]] are [[Numerical variables|continuous variables]].

The simplest method is:
$$\displaystyle \Huge \begin{eqnarray} 
y &=& a + bx \\
a &\rightarrow& intercept \\
b &\rightarrow& slope
\end{eqnarray}$$

The parameters have the *maximum likelihood* with the data. In other words, *find the values of the slope and intercept that make the data most likely*. The math behind is on [[least-squares]].

We know that the *best fit passes through $\displaystyle \large (\bar{x}, \bar{y})$*.

The *difference* between the *fitted line and the original data point* is called [[Deviation|Residual]] (in red):
![[Pasted image 20231110164148.png|400]]

The [[Maximum Likelihood]] model is defined as [[how to find the best fit of linear regression|the model that minimises the sum of the squares of the residuals]] 

(see also [[Correct sums]])


>[!R Lang]
>in `R` we can use `lm(df$resp_var~df$explan_var)`
>we read like *resp_var is modelled as a function of explan_var*
>and we can use `predict` to use the model
>```R
>pol_lm <- lm(amount ~ time + I(time^2), df)
>summary(pol_lm)
>predict(pol_lm, data.frame(time=some_vec))
>```

*To analyse the quality of linear models **always remember of** [[Model Checking - Linear Model]]*

---

**The most common Linear models are**:
- [[Regression Analysis]] - this one!
- [[Analyse of Variance|ANOVA]]
- [[Analysis of Covariance|ANCOVA]]
