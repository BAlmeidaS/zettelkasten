---
tags:
  - Statistics
---
The *best-fit* slope is found by *rotating the line* until the [[Sum of squares errors]] (SSE) is minimised. So we can get when its [[derivative]] *is equal to 0* (using [[Chain Rule]]):
$$\displaystyle \Huge \begin{eqnarray} 
SSE &=& \sum(y-a-bx)^2 \\
\dfrac{dSSE}{db} &=& -2\sum x(y-a-bx) \\
&=& -2\sum yx-ax-bx^2 \\
&=& 0 \\
\sum xy - \sum ax - \sum bx^2 &=& 0 \\ \\
(a = \bar{y} - b\bar{x}, \text{ best fit passes through}(\bar{x}, \bar{y})) \\
\sum xy - \left[ \dfrac{\sum y}{n} -b\dfrac{\sum x}{n} \right]\sum x -b \sum x^2 &=& 0 \\
&\ldots& \\
b &=& \dfrac{\sum xy - \dfrac{\sum x\sum y}{n}}{\sum x^2 - \dfrac{(\sum x)^2}{n}}

\end{eqnarray}$$

from the [[Correct sums]] ([[SSXY]] and [[SSX]]), we can reduce to:
$$\displaystyle \Huge \begin{eqnarray} 
b &=& \dfrac{SSXY}{SSX} \\
\end{eqnarray}$$

---

The same explanation can be found in [[how to find the best fit of linear regression]], but it does not pass through $\displaystyle \large \bar{x}$ and $\displaystyle \large \bar{y}$. There as well it defines how to find the best intercept.