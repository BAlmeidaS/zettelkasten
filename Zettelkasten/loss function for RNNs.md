---
tags:
  - deep-learning
---
Related to [[Recurrent Neural Network|RNNs]] the [[loss function|loss]] will be the *sum of all losses for each time step on the example*

being $\displaystyle \large \mathcal{L}$ any loss function related to the problem ([[Cross-entropy]], [[Mean squared Error|MSE]], ...):

$$\displaystyle \Huge \begin{eqnarray} 
\mathcal{L}(\hat{y}, y) = \sum^{T_y}_{t=1} \mathcal{L}(\hat y^{<t>}, y^{<t>})
\end{eqnarray}$$

