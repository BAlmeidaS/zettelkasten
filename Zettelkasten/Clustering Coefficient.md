---
tags:
  - computer-science
---
*Clustering Coefficient* evaluates the *local structure around the [[Vertices|vertice]]*. It measure how connected the neighbours are.

$$\displaystyle \Huge \begin{eqnarray} 
e_v &=& \dfrac
{\#(\text{edges among neighbouring nodes})}
{\binom{k_v}{2}
} \\
e_v &\in& [0, 1]
\end{eqnarray}$$

- $\displaystyle \large k_v$ is the [[Node Degree]] of [[Vertices|Node]] $\displaystyle \large v$
- $\displaystyle \large \#(\text{edges among neighbouring nodes})$: Edges that connect one neighbour to another

![[Pasted image 20240620203204.png]]

>[!hint]
>Clustering coefficient counts the number of *triangles in the ego-network (network around given node)* 
>![[Pasted image 20240620203357.png|550]]
>For social networks, this is an important measure because *usually a fiend of my friend has high potential to be my friend as well*

[[Graphlets]] are the generalisation of this coefficient, but counting different forms.




