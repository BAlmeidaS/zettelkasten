---
tags:
  - deep-learning
---
The [[back-propagation]] algorithm applied on [[Recurrent Neural Network|RNNs]].

The idea is to move in the opposite direction of the *feed forward* from [[Recurrent Neural Network|RNN]], instead of up and right, going left and down. In the same fashion of [[loss function for RNNs]], the idea is that the [[partial derivatives]] of the loss, are the sum of each loss at time t:

$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{\partial\mathcal{L}^{(T)}}{\partial W} = \sum^T_{t=1}\dfrac{\partial\mathcal{L}^{(T)}}{\partial W} \bigg|_{(t)}
\end{eqnarray}$$

