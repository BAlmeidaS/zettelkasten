---
tags:
  - machine-learning
aliases:
  - min-max scaling
  - min-max normalisation
---
Normalization *scales and centers the data between 0 and 1*, which helps when the algorithm assumes data to be on a similar scale.

$$\displaystyle \Huge \begin{eqnarray} 
x^\prime &=& \dfrac{x - min(x)}{max(x) - min(x)}
\end{eqnarray}$$