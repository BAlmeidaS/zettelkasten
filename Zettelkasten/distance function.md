---
tags:
  - machine-learning
---
A *distance function*, is a function that measure the distance of two points $\displaystyle \large x$ and $\displaystyle \large y$, since it follow these 4 properties:

1. Nonnegative
$$\displaystyle \Huge \begin{eqnarray} 
f(x, y) \ge 0
\end{eqnarray}$$
2. reflexivity
$$\displaystyle \Huge \begin{eqnarray} 
f(x,y) = 0 \iff x = y
\end{eqnarray}$$
3. commutativity
$$\displaystyle \Huge \begin{eqnarray} 
f(x,y) = f(y,x)
\end{eqnarray}$$
4. [[triangle inequality]]
$$\displaystyle \Huge \begin{eqnarray} 
f(x,y) \le f(x,z) + f(y, z)
\end{eqnarray}$$

---

*Distance* can be considered a *hard* definition, a softer definition would be [[Similarity function|dissimilarity function]]