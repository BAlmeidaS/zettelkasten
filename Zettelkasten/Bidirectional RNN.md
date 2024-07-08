---
tags:
  - deep-learning
aliases:
  - BRNN
---
A type of [[Recurrent Neural Network|RNNs]] where the context is processed in both ways, obviously with the addition of *one more weight matrix*.

![[Pasted image 20240708161103.png|400]]

While $\displaystyle \large a_\rightarrow$ computes in the default way the words, the other $\displaystyle \large a_\leftarrow$ starts by the last word and try to predict using the last word, the second last, and so on.

Using [[Multiple weights simplification notation]]:
$$\displaystyle \Huge \begin{eqnarray} 
\hat{y}^{<t>} = g(W_y*[a_\rightarrow^{<t>}, a_\leftarrow^{<t>}] + b_y)
\end{eqnarray}$$