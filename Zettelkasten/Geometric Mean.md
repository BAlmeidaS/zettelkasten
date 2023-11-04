---
tags:
  - Statistics
---
Unlike the arithmetic mean which adds values, the geometric mean multiplies them.

It is useful for *processes that change multiplicatively* rather than additively.

$$\displaystyle \Huge \hat{y}=\sqrt[n]{\prod y}$$

*The geometric mean can be found by multiplying all the numbers in the given data set and take the nth root for the obtained result.*

**Another way to work out is by using logarithms**
$$\displaystyle \Huge \begin{eqnarray} 
\hat{y} &=& exp(mean(log(\vec{y}))) \\ \\
\hat{y} &=& e^{\dfrac{\sum\limits^{n}ln(y_i)}{n}}
\end{eqnarray}$$