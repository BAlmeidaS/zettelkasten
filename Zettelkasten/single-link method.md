---
tags:
  - machine-learning
---
A type of [[Hierarchical clustering]].

It employs the [[nearest neighbor distance]] to measure the [[Similarity function|dissimilarity]] between two groups.

The data points are represented as vertices in the space. A pair $\displaystyle \large x_1$ and $\displaystyle \large x_2$ are connected at level $\displaystyle \large \Delta$  if the distance between them is $\displaystyle \large d_{x_1, x_2} \le \Delta$.

Given these points:
![[Pasted image 20240229145748.png|400]]

*First* we define the [[Similarity function|dissimilarity]] matrix, with the distance between these points - in this case, [[euclidean distance]]:
![[Pasted image 20240229145928.png|300]]

