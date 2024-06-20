---
tags:
  - math
aliases:
  - average node degree
---
Is the *number of edges* connected to a certain *Node* from a [[Graphs]], usually is represented as a letter $\displaystyle \large k$
$$\displaystyle \Huge \begin{eqnarray} 
k_a: \text{node degree of node $a$}

\end{eqnarray}$$

>[!example] 
>In the following example, $\displaystyle \large k_a = 4$
>![[Pasted image 20240620134731.png|300]]

>[!tip]
>The *average degree* is just the average node degree for every node:
>$$\displaystyle \Huge \begin{eqnarray} 
> \bar{k} &=& \dfrac{1}{n}\sum_{i=1}^{N}k_i \\
> \bar{k} &=& \dfrac{2E}{N}
>\end{eqnarray}$$

Have a *self reference* (or loop) on a node *adds 2 to the degree*, because *both endpoints attach to the same node*.

>[!example] 
>In the following example, $\displaystyle \large k_c = 6$ and $\displaystyle \large k_a = 4$ 
>![[Pasted image 20240620135318.png|200]]
