---
tags:
  - deep-learning
aliases:
  - many-to-many rnn
  - one-to-many rnn
  - many-to-one
---
[[Recurrent Neural Network|RNNs]] might differ by the size of the input $\displaystyle \large T_x$ in comparison to the the size of the output $\displaystyle \large T_y$.

### One-to-one
$$\displaystyle \Huge \begin{eqnarray} 
T_x=T_y=1
\end{eqnarray}$$
![[Pasted image 20240708144150.png|120]]

Just a normal [[Neural networks]] and *not a RNN*.

### One-to-many
$$\displaystyle \Huge \begin{eqnarray} 
T_x=1, T_y > 1
\end{eqnarray}$$
![[Pasted image 20240708144143.png|300]]
>[!example] 
>Music Generation, Video Generation

### Many-to-one
$$\displaystyle \Huge \begin{eqnarray} 
T_x=1, T_y > 1
\end{eqnarray}$$
![[Pasted image 20240708144420.png|300]]

>[!example] 
>Sentiment classification, some type of regression or classification on the sequence

### Many-to-many - same size
$$\displaystyle \Huge \begin{eqnarray} 
T_x = T_y
\end{eqnarray}$$
![[Pasted image 20240708144559.png|300]]

>[!example] 
>Name entity recognition, any type of detection on the nodes


### Many-to-many - different sizes
$$\displaystyle \Huge \begin{eqnarray} 
T_x \ne T_y
\end{eqnarray}$$

![[Pasted image 20240708144700.png|400]]

>[!example] 
>Machine translation
