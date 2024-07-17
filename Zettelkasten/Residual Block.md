---
tags:
  - deep-learning
aliases:
  - skip connection
---
The main goal of *Residual Blocks* are to avoid [[vanishing gradient problem]] that deep [[Convolutional Neural Network|CNNs]] have. *ResNet* is a famous network to implement it massively.

The idea is to create a connection between a previous information on the network with a later information, and "connection" is called *skip connection.

![[Pasted image 20240717192753.png|350]]

$$\displaystyle \Huge \begin{eqnarray} 
z_1 &=& W_1\cdot a_0 + b_1
\\
a_1 &=& g(z_1)
\\[10pt]

z_2 &=& W_2\cdot a_1 + b_2

\end{eqnarray}$$
But $\displaystyle \large a2$ *will not be*, solely based on $\displaystyle \large z_2$
