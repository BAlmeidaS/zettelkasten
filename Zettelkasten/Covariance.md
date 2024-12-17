---
tags:
  - Statistics
aliases: []
---
The way that two [[Random Variable]] ([[Numerical variables]]) vary together, the way they *co-vary*
$$\displaystyle \Huge \begin{eqnarray} 
Cov(x, y) &=& E[(x-\bar{x})(y-\bar{y})] \\
&=& \dfrac{1}{n-1}\sum\limits^n_{i=1}(x_i - \bar{x})(y_i - \bar{y})
\end{eqnarray}$$

When:
- $\displaystyle \large Cov(x,y) = 0$ we say that the variables, x and y, are **independent***.
- $\displaystyle \large Cov(x,y) > 0$ if $\displaystyle \large x$ increase, y increases.
- $\displaystyle \large Cov(x,y) < 0$ if $\displaystyle \large x$ increase, y decreases.


Being $\displaystyle \large E[z]$ the [[Expected Value]].

$$\displaystyle \Huge \begin{eqnarray} 
cov(x, y) &=& E(xy) - E(x\bar{y}) - E(\bar{x}y) + E(\bar{x}\bar{y}) \\
&=& E(xy) - \bar{y}E(x) - \bar{x}E(y) + \bar{x}\bar{y} \\
&=& E(xy) - \bar{y}\bar{x} - \bar{x}\bar{y} + \bar{x}\bar{y} \\
&=& E(xy) - \bar{y}\bar{x} \\
cov(x,y) &=& E(xy) - E(x)E(y) \\
\end{eqnarray}$$

When, $\displaystyle \large x$ and $\displaystyle \large y$ are *uncorrelated*, $\displaystyle \large cov(x,y) = 0$, so $\displaystyle \large E(xy) = E(x)E(y)$.

---

Using the [[Correct sums]] ([[SSXY]]), we have:
$$\displaystyle \Huge \begin{eqnarray} 
cov(x, y) &=& \text{SSXY}\sqrt{\dfrac{1}{(n-1)^2}} \\
\end{eqnarray}$$