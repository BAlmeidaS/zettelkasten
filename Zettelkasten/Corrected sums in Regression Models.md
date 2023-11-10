---
tags:
  - Statistics
---
In [[Regression Analysis|Linear Regression]] the best model is the one with *the minimum sum of squared errors* [[Sum of squares errors|SSE]] 

Defining [[Deviation|Residual]] of a point $\displaystyle \large i$ as $\displaystyle \large d_i$, we want the $\displaystyle \large min(\sum d_i)$.
$$\displaystyle \Huge \sum d^2 = \sum (y - a - bx) ^ 2$$

Using the [[Correct sums]] we can define:
- **explained variation** as [[SSR]]
- **unexplained variation** as [[Sum of squares errors|SSE]]

Using the [[Correct sums]] ([[SSXY]], [[SSX]]), the [[Maximum Likelihood]] estimate of the slope is (from [[least-squares]]):
$$\displaystyle \Huge b = \dfrac{SSXY}{SSX} $$

And using [[The famous five from linear models]]:
$$\displaystyle \Huge \begin{eqnarray} 
a &=& \bar{y}-b\bar{x} \\
&=& \dfrac{\sum y}{n}-b\dfrac{\sum x}{n} \\
\end{eqnarray}$$