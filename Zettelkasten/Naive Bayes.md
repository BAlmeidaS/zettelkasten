---
tags:
  - Russel-n-Norvig-chap-12
---
Naive Bayes is called Naive because it assumes all [[Random Variable]]s are [[Conditional Independence]] (independent) given the $\displaystyle \large Cause$
$$\displaystyle \Huge \begin{eqnarray} 
P(Cause, Effect_1, Effect_2, \dots) &=& P(Cause)*\prod_iP(Effect_i|Cause) \\
\end{eqnarray}$$
So given the observed effects $\displaystyle \large e$ and the unobserved variables $\displaystyle \large Y$
$$\displaystyle \Huge \begin{eqnarray} 
P(Cause\mid e) &=& \alpha\sum_yP(Cause, e, y) \\
&=& \alpha(\sum_yP(Cause)*P(y\mid Cause))*\prod_iP(e_i\mid Cause) \\
&=& \alpha P(Cause)*\sum_yP(y\mid Cause)*\prod_iP(e_i\mid Cause) \\
& &\ \ \ \ \ \ \ \ \ \ \  \text{(sum over y is = 1)} \\
\\
P(Cause\mid e) &=& \alpha P(Cause)*\prod_iP(e_i\mid Cause) \\
\end{eqnarray}$$

---

It is called Naive because, the correct way to calculate $\displaystyle \large P(a\mid b,c,d)$ is
$$\displaystyle \Huge \begin{eqnarray} 
P(a\mid b,c,d) &=&  
\dfrac{P(a)*P(b,c,d|a)}{P(b,c,d)}
\end{eqnarray}$$

P(b,c,d)
The more variables we add as evidence, the more intractable is the formula, it ha