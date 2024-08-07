---
tags:
  - deep-learning
aliases:
  - RNNs
---
Type of [[Neural networks|Neural Network]] where the goal is to process sequential data by leveraging temporal or sequential patterns.

The idea is that *a type of signal is shared between each execution* and this information is propagated through the examples. Also, the core idea is that the [[Parameters of the Model|Parameters]] *are shared* between the examples. 

![[Pasted image 20240708134614.png]]
$\displaystyle \large a^{<t>}$ is the activation of the neuron and is also called as the hidden state - usually $\displaystyle \large a^{<0>}$ is defined as a vector of zeros 
$\displaystyle \large x^{<t>}$ is the input $\displaystyle \large t$
$\displaystyle \large y^{<t>}$ is the prediction $\displaystyle \large t$

$$\displaystyle \Huge \begin{eqnarray} 
a^{<t>} &=& g_1(
W_{aa}*a^{<t-1>}
+ W_{ax}*x^{<t>}
+ b_a
) 
\\[6pt]
y^{<t>} &=& g_2(
W_{ya}*a^{<t>}
+ b_y
) 
\end{eqnarray}$$

Because of the [[Multiple weights simplification notation]], $\displaystyle \large a^{<t>}$ is defined often as: 
$$\displaystyle \Huge \begin{eqnarray} 
a^{<t>} &=& g_1(
W_a[a^{<t-1>}, x^{<t>}]
+ b_a
) 
\end{eqnarray}$$

Full image with the operations:
![[Pasted image 20240708141701.png]]

A particular useful case for *RNNs* (apart from [[Types of RNN]]) is *sequence generation*, where based on the previous token, the model will try to generate the next token.

Finally, *RNN* suffer a lot by the [[vanishing gradient problem]]