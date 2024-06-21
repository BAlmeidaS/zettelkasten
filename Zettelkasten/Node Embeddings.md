---
tags:
  - deep-learning
aliases:
  - encoding decoding graphs
---
*Nodes embedding* are a type of [[embedding]] for [[Vertices|Nodes]] in a [[Graphs|Graph]]. The idea is defining a function $\displaystyle \large f$ that maps the node $\displaystyle \large u$ to its embedding representation $\displaystyle \large z_u$:
$$\displaystyle \Huge \begin{eqnarray} 
f: node \rightarrow \mathbb{R}^d
\end{eqnarray}$$

A way to define this function is using the framework *encoding and decoding graphs*. This will be reduce the *Graph [[Representation Learning]]* into two operations: *Encoding and Decoding*





Given a node $\displaystyle \large u$, find a function $\displaystyle \large f: node \rightarrow \mathbb{R}^d$



The idea here is presenting a *framework* to create *node [[embedding]]*.



The *main goal* is if [[Vertices|Nodes]] are similar in the original [[Graphs|Graph]], so *they must be close in the embedding space* (using dot product):
$$\displaystyle \Huge \begin{eqnarray} 
similarity(u, v) \approx z_u^T\cdot z_v
\end{eqnarray}$$
$\displaystyle \large u, v$: are [[Vertices|vertices]] of the graph

To do this, we must find a [[Similarity function]] in the original network.

Also, we must define an [[encoder of node graphs]] which map the nodes to their embedding (low-dimensional vector):
$$\displaystyle \Huge \begin{eqnarray} 
enc(u) = z_u
\end{eqnarray}$$

On the other hand, a *decoder* also must be defined:
$$\displaystyle \Huge \begin{eqnarray} 
dec(z_u) = u
\end{eqnarray}$$

With that, the decoder must be as close as it possible from the original similarity
$$\displaystyle \Huge \begin{eqnarray} 
similarity(u, v) \approx 
dec(enc(u), enc(v))
\end{eqnarray}$$


