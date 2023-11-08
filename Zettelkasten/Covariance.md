---
tags:
  - Statistics
aliases: []
---
The way that two [[Random Variable]] ([[Continuous variable]]) vary together, the way they *co-vary*
$$\displaystyle \Huge \begin{eqnarray} 
cov(x, y) &=& E[(x-\bar{x})(y-\bar{y})]
\end{eqnarray}$$

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

from the [[corrected sum of squares and products]], we have:
$$\displaystyle \Huge \begin{eqnarray} 
cov(x, y) &=& \text{SSXY}\sqrt{\dfrac{1}{(n-1)^2}} \\
\end{eqnarray}$$

which provides a short cut for the [[Correlation]] coefficient
$$\displaystyle \Huge \begin{eqnarray} 
r &=& \dfrac{\text{SSXY}}{\sqrt{\text{SSX}*\text{SSY}}} \\

\end{eqnarray}$$






