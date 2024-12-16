---
tags:
  - deep-learning
---
Given an [[Recurrent Neural Network|RNN]] the *attention method* is often referred to [[Sequence to Sequence models]], though it can be used in *any RNN architecture*.

Here it will be defined using a simple [[Bidirectional RNN]] (but it could be unidirectional, GRU, LSTM, ...).

It will "kinda" of follow the [[Sequence to Sequence models|encode / decode]] structure from Seq2Seq, but the input won't merely be the context of the last encode layer, rather it will be the whole encode, 

![[Pasted image 20240715182827.png]]

The goal is to learn *each one of this $\displaystyle \large \alpha_{ij}$*, which is the *amount of attention that node $\displaystyle \large j$ is paying to node $\displaystyle \large i$*.

$\displaystyle \large \alpha$ will be a [[softmax function|softmax]] for each node $\displaystyle \large j$ on the *decode*, and it will be built using a small neural network, with the *context aggregated $\displaystyle \large c$ and the last word $\displaystyle \large y_{last}$.

$$\displaystyle \Huge \begin{eqnarray} 
\alpha_{i,j} = 
\dfrac{ e^{z_{i,j}} }{ \sum\limits^{Tx}_ke^{z_{i,k}} }
\end{eqnarray}$$

and $\displaystyle \large z_{i,j}$ is gotten from the small neural net
![[Pasted image 20240715193908.png|500]]

The final context is built calculating the [[dot product]] of the alphas and the original context *from the encode*
![[Pasted image 20240716111428.png|600]]

The *downside is that the amount of $\displaystyle \large \alpha$s is $\displaystyle \large T_x * T_y$ , so it is quadratic time to tune this whole number of parameters.*