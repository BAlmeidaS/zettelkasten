---
tags:
  - deep-learning
---
*Back propagation* is an algorithm to compute the gradients, making the information from the cost flowing backward to the network, by using the [[Chain Rule]]

$$\displaystyle \Huge \begin{eqnarray} 
\boldsymbol{z}^{(n)} &=& \boldsymbol{W}^{(n)} * \boldsymbol{a}^{(n-1)} + \boldsymbol{b}^{(n)}
\\
\boldsymbol{a}^{(n)} &=& \sigma(\boldsymbol{z}^{(n)})
\\
C_k &=& \sum_i(a_i^{(last)} - y_i)^2

\end{eqnarray}$$