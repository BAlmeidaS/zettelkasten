---
tags:
  - Statistics
---
Crawley presents this digression on his book (page 55) of how to have a *better formula* to a computer to calculate the [[Sum of squares]] and, as a consequence, also [[Variance]].

---

The problem is to calculate many subtractions: $\displaystyle \large \sum(y-\bar{y})^2$.

$$\displaystyle \Huge (y-\bar{y})^2=y^2-2y\bar{y}+\bar{y}^2$$
so,
$$\displaystyle \Huge \begin{eqnarray} 
\sum(y-\bar{y})^2 &=& \sum y^2 - 2\bar{y}\sum y &+& n\bar{y}^2 \\
&=& \sum y^2 - 2\dfrac{\sum y}{n}\sum y\ &+& n[\dfrac{\sum y}{}]^2

\end{eqnarray}$$
