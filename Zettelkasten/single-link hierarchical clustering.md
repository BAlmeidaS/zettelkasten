---
tags:
  - machine-learning
---
A type of [[Hierarchical clustering]].

It employs the [[nearest neighbor distance]] to measure the [[Similarity function|dissimilarity]] between two groups, so the distance will always be defined as:
$$\displaystyle \Huge \begin{eqnarray} 
D_{nn}(C_1, C_2) &=& \min_{x \in C_1,\ y \in C_2}d(x, y)
\end{eqnarray}$$

The data points are represented as vertices in the space. A pair $\displaystyle \large x_1$ and $\displaystyle \large x_2$ are connected at level $\displaystyle \large \Delta$  if the distance between them is $\displaystyle \large d_{x_1, x_2} \le \Delta$. Thus, it aims to *connect clusters that have the shortest **min** distance*.

>[!example] an example of the algorithm
>Given these points:
>![[Pasted image 20240229145748.png|400]]
>
>*First* we define the [[Similarity function|dissimilarity]] matrix, with the distance between these points - in this case, [[euclidean distance]]:
>![[Pasted image 20240229145928.png|300]]
>
>The min distance in this case is between $\displaystyle \large x_1$ and $\displaystyle \large x_2$, so they will be connected, and the *distance of the other points to this cluster will be the min distance between them and $\displaystyle \large x_1$ and $\displaystyle \large x_2$*
>$$\displaystyle \large \begin{eqnarray} 
>D(\{x_1,x_2\}, x_3) = \min \{d(x_1, x_3), d(x_2, x_3)\} = 2.24\\
>D(\{x_1,x_2\}, x_4) = \min \{d(x_1, x_4), d(x_2, x_4)\} = 3.35\\
>D(\{x_1,x_2\}, x_5) = \min \{d(x_1, x_5), d(x_2, x_5)\} = 3\\
>\end{eqnarray}$$
>![[Pasted image 20240229150250.png|300]]
>	
>*Then*, we keep connecting the points with the min distance. Now, will be $\displaystyle \large x_3$ and $\displaystyle \large x_4$
>![[Pasted image 20240229150710.png|300]]
>
>Finally, $\displaystyle \large \{x_3, x_4\}$ and $\displaystyle \large x_5$
>![[Pasted image 20240229150802.png|300]]
>
>Final [[dendogram]]:
>![[Pasted image 20240229150849.png|400]]
