[[Bayesian Network|Bayes Nets]] that contain *discrete and continuous* variables ([[Bayes net with continuous variables]])

![[Pasted image 20231017102954.png|600]]

In this example $\displaystyle \large P(Cost\mid Harvest,Subsidy)$ will be defined as:
- The discrete parent $\displaystyle \large Subsidy$ is handles by enumeration
- The continuous parente $\displaystyle \large Harvest$ is governed by a [[Canonical distribution]] - let's say [[Gaussian]], so a $\displaystyle \large \mu$ and $\displaystyle \large \sigma$ 

Suppose the $\displaystyle \large Subsidy$ is binary, so we will end up with two distributions:
$$\displaystyle \Huge \begin{eqnarray} 
P(c\mid h, subsidy) &=& \mathcal{N}(c;\mu_t,\sigma_t^2) \\
P(c\mid h, \lnot subsidy) &=& \mathcal{N}(c;\mu_f,\sigma_f^2) \\
\end{eqnarray}$$
![[Pasted image 20231017104039.png|600]]

Then regarding buys, we need to transform this continuous value of cost in a discrete value. A common approach is using [[logistic function]] or a [[probit function]].