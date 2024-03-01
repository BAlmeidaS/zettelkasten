---
tags:
  - machine-learning
---
*Silhouette score* is a way to compute [[Clustering evaluation]]. The idea is looking into the internal features of the clusters found. How similar to objects of a cluster are (*cohesion*) compared to other clusters (*separation*).

It can be defined as:
$$\displaystyle \Huge \begin{eqnarray} 
s(x) = \dfrac{b(x) - a(x)}{\max{\{a(x), b(x)\}}}
\end{eqnarray}$$

the functions $\displaystyle \large b$ and $\displaystyle \large a$ rely on a [[Similarity function|dissimilarity function]].
- $\displaystyle \large b(x)$ : the smallest mean distance of $\displaystyle \large x$ to all the other points not from $\displaystyle \large x$'s cluster
$$\displaystyle \Huge \begin{eqnarray} 
b(x) = \min_{I \ne J} \left(\dfrac{1}{|C_J|}\sum_{y \in C_J} d(x, y)\right)
\text{, given } x \in C_I
\end{eqnarray}$$

- $\displaystyle \large a(x)$ : the mean distance of $\displaystyle \large x$ to all the other points inside $\displaystyle \large x$'s cluster
$$\displaystyle \Huge \begin{eqnarray} 
a(x) = \dfrac{1}{|C_I| - 1}\sum_{x_2 \in C_I, x \ne x_2} d(x, x_2)
\text{, given } x \in C_I
\end{eqnarray}$$

The *silhouette score goes from $\displaystyle \large -1$ to $\displaystyle \large 1$*. **Being $\displaystyle \large 1$ the best value, and $\displaystyle \large -1$ the worst.

>[!hint]
>- $\displaystyle \large s(i) = 1$ : The point is well clustered
>- $\displaystyle \large s(i) = 0$ : The point is very *close to the decision boundary of 2 neighbouring clusters*.
>- $\displaystyle \large s(i) = -1$ : The point has been placed in the wrong cluster

To calculate the score for the **whole dataset we use the [[Average]] of the $\displaystyle \large s(x)$ for all of its points**