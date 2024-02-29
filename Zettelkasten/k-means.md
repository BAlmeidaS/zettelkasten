---
tags:
  - machine-learning
---
*K-means* is a [[Partitional clustering]], more specifically a [[centre-based clustering]].

Number of cluster $\displaystyle \large k$ is fixed.

*Each cluster has a centroid*.

The goal is to minimise the [[objective function]]:
$$\displaystyle \Huge \begin{eqnarray} 
E = \sum^k_{i=1}\sum_{x \in C_i}d(x, \mu(C_i))
\end{eqnarray}$$

- $\displaystyle \large C_i$ is a cluster
- $\displaystyle \large \mu(C_i)$ is the centroid of the cluster
- $\displaystyle \large x$ is a cluster point 
- the function $\displaystyle \large d$, is any [[distance function]]

It is called k-means, because in each step it reset the centroid to minimise the **mean** distance for all of its points.

>[!summary] algorithm
>1. Random pick a number k of cluster centres (*initial seeds*)
>2. Assign every object to its nearest cluster centre using some [[distance function]]
>3. For each cluster update centre to the **mean**.
>4. Repeat 2 and 3 until either:
>	a. error < threshold
>	b. no change in cluster assignments




