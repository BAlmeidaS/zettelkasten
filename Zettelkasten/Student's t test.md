---
tags:
  - Statistics
aliases:
  - student's t test
  - t test
  - t-test
---
We use *student's t test* with 3 constants / assumptions:
1. The samples are independents
2. The [[Variance]] is constant (**The most important assumption for t test**)
3. The errors are [[Normal Distribution|normally distributed]] 

It is a test to *compare means* of 2 distributions. 
[[Null Hypothesis|H0]]: Means are the same
[[Alternative Hypothesis|H1]]: Means are different

the [[Test Statistic]] is $\displaystyle \large t$:
$$\displaystyle \Huge \begin{eqnarray} 
t &=& \dfrac{\text{difference between the two mean}}{\text{SE of the difference}}
\\ \\
t &=& \dfrac{\bar{y}_A - \bar{y}_B}{SE_{\text{diff}}} 
\end{eqnarray}$$

$\displaystyle \large SE_{\text{diff}}$ can be defined using [[Variance of the Difference]] and will be the [[Standard error of the difference between two mean]]:
$$\displaystyle \Huge SE_{\text{diff}} = \sqrt{\dfrac{s_A^2}{n_A} + \dfrac{s_B^2}{n_B}}$$

---

We can run *t test* to understand if one variable can explain the mean of the other (when filtered). 

>[!R Lang]
>Let's say we have a `df` with radius of the tumor, and the class of the tumor. We can check if the mean of the radius is different by the class (Maligns cancers has bigger radius means?):
>```R
>t.test(df$radius ~ df$class)
>```
>Note that this is equivalent of splitting the data into two, and running the t.test with both.

Also, `R` already validate the variances on `t.test` and adapts the test if they do not match, before even running the proper test.