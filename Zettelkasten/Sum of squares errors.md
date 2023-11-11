---
tags:
  - Statistics
aliases:
  - Sum of Squares
  - SSE
---
The **unexplained variation** of a [[Regression Analysis|Linear Model]].

Perhaps the most important single quantity in all statistics. It has multiple interpretations but in its purest form is:
$$\displaystyle \Huge sum\_of\_squares = \sum\limits^n_{i=1}(y_i-\bar{y})^2$$

The unit depends on the unit of $\displaystyle \large y$ and it will be that one squared.

*sum of squares always increases with the addition of new data points* (or stays the same if the data point has the value exactly equal to the mean). Usually this is "bad thing", because it is not comparable since it depends on the size of the dataset.

---

*SSE* can also be defined using [[SSY]] and [[SSR]]:
$$\displaystyle \Huge \begin{eqnarray} 
SSE &=& SSY - SSR \\
\end{eqnarray}$$