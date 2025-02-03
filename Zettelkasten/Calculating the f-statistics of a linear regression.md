---
tags:
  - Statistics
---
The problem to use directly [[F test]] to evaluate [[p-value]] of the [[Regression Analysis|Linear Regression]] is that it must take into account the [[Degrees of Freedom]].

The F-statistic is given by:

$$\displaystyle \Huge \begin{eqnarray} 
F =
\dfrac{Explained\ Variance (\text{mean regression sum of squares})}
{Unexplained\ Variance (\text{mean squared error})}
\end{eqnarray}$$
or:
$$\displaystyle \Huge \begin{eqnarray} 
f = \dfrac
{\dfrac{SS_{regression}}{df_{regression}}}
{\dfrac{SS_{residuals}}{df_{residuals}}}
\end{eqnarray}$$

Related to the *regression*:
$$\displaystyle \Huge \begin{eqnarray} 
SS_{regression} &=& \sum(\hat{y}_i - \bar{y})^2

\\
df_{regression} &=& num\_of\_params - 1
\end{eqnarray}$$

Related to the *residuals*:
$$\displaystyle \Huge \begin{eqnarray} 
SS_{regression} &=& \sum(y_i - \bar{y})^2

\\
df_{regression} &=& num\_of\_data\_points - num\_of\_params
\end{eqnarray}$$

Then we put on the *F-distribution curve* and calculate the [[p-value]] of that point (the area on the right divided by the total area)


