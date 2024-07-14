---
tags:
  - deep-learning
aliases:
  - Conditional language model
---
[[Recurrent Neural Network|RNNs]] might have multiple [[Types of RNN|types]], most of them are very much straightforward to conceive, however, *many to many with different sizes* is the most different one.

![[Pasted image 20240708144700.png|500]]

The main idea here is, after the end of the input sentence, $\displaystyle \large x^{<T_x>}$, the last output is used as input and a lopping starts using the last word generated (and the context accumulated) to generate the next word, until the *end of sequence* token is generated.

![[Pasted image 20240714192716.png]]
The first part (*green*) is known as the *encoder*.
The second part (*purple*) is known as the *decoder*.

>[!note]
>Sometimes this architecture is known as *conditional language model*, mainly because *purple* is conditioned to *green*. In other words, it will generate sequences based on the context observed on green.
>$$\displaystyle \Huge \begin{eqnarray} 
>p(
>y^{<1>}, \cdots, y^{<T_y>}
>\mid
>x^{<T_1>},\cdots, x^{<T_x>}
>)
>\end{eqnarray}$$

Considering that the outputs $\displaystyle \large y^{<i>}$ are the result of a [[softmax function|softmax]], we usually *don't* want to take the [[Arg Max]] of each $\displaystyle \large y^{<i>}$, in other words doing a type of [[Greedy Best-first search|greedy search]], because this can lead to *sub-optimal* solutions. Instead, we want the most likely *whole sentence*:
$$\displaystyle \Huge \begin{eqnarray} 
\arg \max_y p(y^{<1>}, \cdots, y^{<T_y>} \mid \boldsymbol{x})
\end{eqnarray}$$

A simple approach uses [[Beam Search to find the most likely sentence]].