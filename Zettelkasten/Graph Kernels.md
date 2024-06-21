---
tags:
  - computer-science
aliases:
  - bag of node degrees
  - Weisfeiler-Lehman Kernel
---
*Graph Kernels* measure similarity between two graphs. Design a graph feature vector $\displaystyle \large \phi(G)$, inspired in [[Bag-of-words]].

A simple approach will be a *bag-of-node-degrees*:
- an array with the number of nodes that exist for the mapped degrees:
$$\displaystyle \Huge \begin{eqnarray} 
\phi(G) = [
\#num\_nodes\_deggre\_1, 
\#num\_nodes\_deggre\_2, 
\dots
]
\end{eqnarray}$$

Of course, this *bag of something* can be evolved using [[Graphlets]], and with that we have *Graphlet Kernel* (with a main difference that in this case they might be neither connected nor rotted)
![[Pasted image 20240621172859.png|400]]

problem with this approach of Graphlets is that is an [[NP-hard]] problem

---

Other solutions is:
Weisfeiler-Lehman Kernel / Color Refinement (will not create a card for now)
