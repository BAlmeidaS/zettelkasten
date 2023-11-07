---
tags:
  - Statistics
---
It measures which a distribution has [[Long Tail distributions|long tails]] on one side. The degree of skew of a distribution $\displaystyle \large \gamma_1$

[[Normal Distribution]] has $\displaystyle \large skew = 0$.

$$\displaystyle \Huge \begin{eqnarray} 
skew &=& \gamma_1 = \dfrac{m_3}{s_3} \\ \\
m_3 &=& \dfrac{\sum(y-\bar{y})^3}{n} \\
s_3 &=& sd(y)^3 = \left(\sqrt{s^2}\right)^3 \\
\end{eqnarray}$$

The standard error of skew is, defined as,
$$\displaystyle \Huge SE_{y_1} = \sqrt{\dfrac{6}{n}}$$

*Negatives values of $\displaystyle \large \gamma_1$* means skew to the *left* - (tail is on the left).
*Positives values of $\displaystyle \large \gamma_1$* means skew to the *right* - (tail is on the right).

---

We use $\displaystyle \large SE_{\gamma_1}$ to validate if the skew is really different than 0, using [[Student's t test|t test]]:

if $\displaystyle \large \left|\dfrac{\gamma_1}{SE_{\gamma_1}}\right| < 2$ ,(this 2 came from the [[Student's t = 2 rule of thumb]]), so this distribution has no strong skewness. Otherwise, we know that there is a skewness and we must check the signal of $\displaystyle \large \gamma_1$ to know to what side is the tail.