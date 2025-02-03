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

>[!important] statistical relevance
The *statistical relevance* comes from running an [[F test]] comparing the *variance explained by the model* against the *variance left explained*.
>
>The easiest way to grasp this is by understanding as an F Test between the *y-hat and the [[Deviation|Residuals]]:
>```R
>model <- lm (y ~ x, data=df)
>
>y_hat <- fitted(model) # predicted values
>residuals <- residuals(model) # Errors distribution : (y - y-hat)
>
>var.test(y_hat, residuals) # F-test comparing explained vs. residual variance
>```
>
> *This is wrong but it is a way to remember!* It is wrong because the right way is to calculating the f-statistics manually, and plotting on the correct f-distribution.
> 
> In order to calculate manually and get the correct f-distribution, one must take into account the [[Degrees of Freedom]] of the model! But this turns out to be [[Calculating the f-statistics of a linear regression|a more complicated math]].

---

**The most common Linear models are**:
- [[Regression Analysis]] - this one!
- [[Analyse of Variance|ANOVA]]
- [[Analysis of Covariance|ANCOVA]]
