---
tags:
  - Russel-n-Norvig-chap-12
---

Also called **unconditional**

In a [[Joint Probability Distribution]] with many random variables, the probability of an event $\displaystyle \large \omega$ from one [[Random Variable]] $\displaystyle \large X_i$ happened, regardless the other random variables:

$$\displaystyle \Huge \begin{eqnarray}
&P(\omega)&,\ \omega \in X_i \\
\\
&P(\omega)& = 
\sum_{z}
P(\omega, z)
\end{eqnarray}$$

This process is called **marginalisation** or **summing out**

Applying [[product rule of probability]]
$$\displaystyle \Huge \begin{eqnarray}
&P(\omega)& = 
\sum_{z} P(\omega, z)
\\
&P(\omega)& = 
\sum_{z} P(\omega \mid z)*P(z)
\end{eqnarray}$$

