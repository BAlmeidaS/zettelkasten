---
tags:
  - deep-learning
aliases:
  - skip connection
---
The main goal of *Residual Blocks* are to avoid [[vanishing gradient problem]] that deep [[Neural networks]] have. *ResNet* is a famous network to implement it with [[Convolutional Neural Network|CNNs]].

The idea is to create a connection between a previous information on the network with a later information, and "connection" is called *skip connection.

![[Pasted image 20240717192753.png|350]]

$$\displaystyle \Huge \begin{eqnarray} 
z_1 &=& W_1\cdot a_0 + b_1
\\
a_1 &=& g(z_1)
\\[10pt]

z_2 &=& W_2\cdot a_1 + b_2

\end{eqnarray}$$
But $\displaystyle \large a2$ *will not be*, solely based on $\displaystyle \large z_2$, rather, *with skip connection* it will be:
$$\displaystyle \Huge \begin{eqnarray} 
a_2 &=& g(z_2 + a_0)
\end{eqnarray}$$

And the *connection of this 4 layers ($\displaystyle \large z_1, a_1, z_2, a_2$) is what we call a **residual block***.

**However**, there is one caveat, *$\displaystyle \large a_2$ and $\displaystyle \large a_0$ must have the same dimension*.

**If the dimensions are not equal a new matrix must be added, and this matrix will be learned**
$$\displaystyle \Huge \begin{eqnarray} 
a_2 &=& g(z_2 + W_{s} \cdot a_0)
\\[8pt]
dim(W_s) &=& dim(a_2) \times dim(a_0)
\end{eqnarray}$$

>[!tip] 
>Residual blocks try to solve the problem of adding more layers resulting in worse performance on train set:
> ![[Pasted image 20240717193834.png|500]]

>[!important] why it works?
>The idea is that if $\displaystyle \large W_2$ and $\displaystyle \large b_2$ are zero, so, $\displaystyle \large a_2 = g(a_0)$, which in general is $\displaystyle \large g(a_0) = a_0$.
>*which means* that the network now has the *capability to learn that a layer is useless*.


