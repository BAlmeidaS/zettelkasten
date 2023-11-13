---
tags:
  - Statistics
aliases:
  - student's t test
  - t test
---
We use *student's t test* with 3 constants / assumptions:
1. The samples are independents
2. The [[Variance]] is constant (**The most important assumptioni for t test**)
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