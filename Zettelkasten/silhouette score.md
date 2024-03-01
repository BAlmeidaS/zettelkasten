---
tags:
  - machine-learning
---
*Silhouette score* is a way to compute [[Clustering evaluation]]. The idea is looking into the internal features of the clusters found. How similar to objects of a cluster are (*cohesion*) compared to other clusters (*separation*).

It can be defined as:
$$\displaystyle \Huge \begin{eqnarray} 
s(x) = \dfrac{b(x) - a(x)}{\max{\{a(x), b(x)\}}}
\end{eqnarray}$$

the functions $\displaystyle \large b$ and $\displaystyle \large a$ rely on a [[distance function]].
- $\displaystyle \large b(x)$ : the smallest mean distance of $\displaystyle \large x$ to all the other points not from $\displaystyle \large x$'s cluster
$$\displaystyle \Huge \begin{eqnarray} 
b(x) = \min_{I \ne J} \left(\dfrac{1}{|C_j|}\sum_{y \in C_j} d(x, y)\right)
\text{, given } x \in C_i
\end{eqnarray}$$
- $\displaystyle \large a(x)$ : the mean distance of $\displaystyle \large x$ to all the other points inside $\displaystyle \large x$'s cluster