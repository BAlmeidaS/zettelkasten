---
tags:
  - Statistics
aliases:
  - wald test
---
*Wald Test* is commonly applied to [[logistic regression]] to evaluate weather an [[Explanatory variable|independent variable]] has a significant effect on the *dependent variable*.

In [[logistic regression]], the [[logit function]] is defined as
$$\displaystyle \Huge \begin{eqnarray} 
log\left(\dfrac{p}{1-p}\right) = 
\beta_0 +
\beta_1X_1 + 
\cdots
\beta_nX_n
\end{eqnarray}$$

The *farther $\displaystyle \large \beta_i$ is from 0, the most important is that [[Explanatory variable|independent variable]] $\displaystyle \large X_i$.

---

To a specific [[Explanatory variable|independent variable]] $\displaystyle \large i$, *Wald Test* gives as [[Hypothesis Test]]
[[Null Hypothesis|H0]]:  $\displaystyle \large \beta_i = 0$
[[Null Hypothesis|H1]]:  $\displaystyle \large \beta_i \ne 0$

the [[Test Statistic]] is:
$$\displaystyle \Huge \begin{eqnarray} 
W = \dfrac{\beta_i}{SE(\beta_i)}
\end{eqnarray}$$
Being $\displaystyle \large SE$ the *Standard Error*. Considering *logistic regression*:
$$\displaystyle \Huge \begin{eqnarray} 
SE(\beta_i) &=& \sqrt{[(X^TWX)^{-1}]_{jj}}
\\\\
being,
\\
X &=&
\begin{bmatrix}
1 & X_{11} & X_{12} & \dots & X_{1n} \\
1 & X_{21} & X_{22} & \dots & X_{2n} \\
1 & X_{31} & X_{32} & \dots & X_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
1 & X_{m1} & X_{m2} & \dots & X_{mn}
\end{bmatrix}

\end{eqnarray}$$

Then the test statistical is calculated it is plot on a [[Normal Distribution|Gaussian]] $\displaystyle \large N(0, 1)$. 

So the test is [[Parametric Method|parametric]] because *it assumes that the $\displaystyle \large \beta_i$ comes from a normal distribution $\displaystyle \large W \sim N(0,1)$.

>[!note] more deeply
>In fact, all $\displaystyle \large \beta$s here are, in fact, $\displaystyle \large \hat\beta_i$. Meaning that they are an *approximation* of the true coefficient (that we don't know) $\displaystyle \large \beta_i$. Moreover, those $\displaystyle \large \hat\beta$ are estimated using [[Maximum Likelihood]] Estimation, so:
>$$\displaystyle \Huge \begin{eqnarray} 
>\hat\beta_i \sim N(\beta_i, Var(\hat\beta_i))
>\end{eqnarray}$$



