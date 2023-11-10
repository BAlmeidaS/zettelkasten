---
tags:
  - Statistics
---
In a [[Regression Analysis]], each *residual, $\displaystyle \large d_i$, is the distance between $\displaystyle \large y_i$ and the fitted value $\displaystyle \large \hat{y_i}$*

So,
$$\displaystyle \Huge \begin{eqnarray} 
\sum d_i &=& \sum (y - a - bx) \\
(a = \bar{y} - b\bar{x}&,& \text{ best fit passes through}(\bar{x}, \bar{y})) \\
&=& \sum (y -\bar{y} + b\bar{x} - bx) \\
(\sum\bar{x} = nx) \\
&=& \sum y - n\bar{y} + bn\bar{x} - b\sum x \\
(\bar{x} = \dfrac{\sum x}{n}) \\
&=& \sum y - n \dfrac{\sum y}{n} + bn\dfrac{\sum x}{n} - b\sum x \\
&=& \sum y - \sum y + b\sum x - b\sum x \\
&=& 0
\end{eqnarray}$$
