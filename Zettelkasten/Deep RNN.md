---
tags:
  - deep-learning
aliases:
  - DRNN
---
An [[Recurrent Neural Network|RNN]] might contain an arbitrary number of layers, leading to many contexts being processed, each one with their on *weight matrix*

![[Pasted image 20240708161242.png|400]]

The weights are shared on the same line, so, for the second line, to calculate the second cell
$$\displaystyle \Huge \begin{eqnarray} 
a^{[2]<2>} = f(W_a^{[2]}*[a^{[2]<1>}, a^{[1]<2>}] + b_a^{[2]})
\end{eqnarray}$$

Notice where each $\displaystyle \large a$ is related to
![[Pasted image 20240708185132.png|300]]

