---
tags:
  - deep-learning
---
A type of [[loss function]] where the loss is calculated using three objects: anchor $\displaystyle \large A$, positive $\displaystyle \large P$ and negative $\displaystyle \large N$. The goal is making the *positive being close to the anchor* and *the negative far from the anchor*.
![[Pasted image 20240722161925.png]]

Considering $\displaystyle \large A, P, N$ as [[embedding]] and using the [[Modulus of a vector|norm]], or a [[distance function]] $\displaystyle \large d$:
$$\displaystyle \Huge \begin{eqnarray} 
\Vert f(A) - f(P) \Vert^2
&\le&
\Vert f(A) - f(N) \Vert^2
\\[5pt]
&\text{or}&
\\[5pt]
d(A, P) &\le& d(A, N) 
\end{eqnarray}$$

by moving things on the equation we came up to:
$$\displaystyle \Huge \begin{eqnarray} 
\Vert f(A) - f(P) \Vert^2
-
\Vert f(A) - f(N) \Vert^2
\le 0
\end{eqnarray}$$

To avoid the trivial solution of $\displaystyle \large f$ returning always zero, we say that must be smaller than an $\displaystyle \large -\alpha$ rather then $\displaystyle \large 0$, and by convention we move to the other side:
$$\displaystyle \Huge \begin{eqnarray} 
\Vert f(A) - f(P) \Vert^2
-
\Vert f(A) - f(N) \Vert^2
\le 0 - \alpha
\\[7pt]
\Vert f(A) - f(P) \Vert^2
-
\Vert f(A) - f(N) \Vert^2 - \alpha
\le 0 
\end{eqnarray}$$
$\displaystyle \large \alpha$ is called *the margin*

The *triplet [[loss function]] is defined with **3 objects***:
$$\displaystyle \Huge \begin{eqnarray} 
\mathcal{L}(A, P, N) = \max(
\Vert f(A) - f(P) \Vert^2
-
\Vert f(A) - f(N) \Vert^2 - \alpha
, 0)
\end{eqnarray}$$

So the [[Cost function]]:
$$\displaystyle \Huge \begin{eqnarray} 
J = \sum^n_{i=1} \mathcal{L}(A^i, P^i, N^i)
\end{eqnarray}$$

>[!tip]
>So if your dataset has 10,000 objects, the idea is generating these *triplets*, with one anchor, one positive and one negative object. And you should chose triplets that are *hard to train on*, examples where $\displaystyle \large N$ is close to $\displaystyle \large A$, so:
>$$\displaystyle \Huge \begin{eqnarray} 
>d(A, P) \approx d(A, N)
>\end{eqnarray}$$
