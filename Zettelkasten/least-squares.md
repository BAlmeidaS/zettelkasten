---
tags:
  - Statistics
---
The *best-fit* slope is found by *rotating the line* until the [[Sum of squares]] (SSE) is minimised. So we can get when its [[derivative]] *is equal to 0* (using [[chain rule]]):
$$\displaystyle \Huge \begin{eqnarray} 
SSE &=& \sum(y-a-bx)^2 \\
\dfrac{dSSE}{db} &=& -2\sum x(y-a-bx) \\
&=& -2\sum yx-ax-bx^2 \\
&=& 0 \\
\sum xy - \sum ax - \sum bx^2 &=& 0 \\
(a = \bar{y} - b\bar{x}) \\
\sum xy - \left[ \dfrac{\sum y}{n} -b\dfrac{x}{n} \right]\sum x -b \sum x^2 &=& 0

\end{eqnarray}$$