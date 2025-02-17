---
tags:
  - math
  - computer-science
aliases:
  - MST
  - cut
  - cut property
---
a **spanning tree _T_** of an  [[Undirected Graphs]] _G_ is a subgraph that is a [[Google - Review - Trees|Tree]] which includes **all of the vertices of _G_**. It uses only edges from the original graph.

![[Pasted image 20250216183518.png]]

### Minimum Spanning Tree

Given a *[[Weighted Graphs|Weighted]] Undirected Graph*, we can define as *Minimum Spanning Tree* [[Minimum Spanning Tree|MST]], a *spanning tree* with the **minimum possible total edge weight**. It might exist more than one MST:

![[Pasted image 20250216184438.png]]

*How to construct MST? [[Kruskal's algorithm]]*

MST are connected with the **Cut Property**:

A *Cut* in a graph is **a partitition of vertices of a graph into 2 disjoint subsets**:
-  Given a graph $\displaystyle \large G = (V, E)$, a *cut* is a partition of the vertex set $\displaystyle \large V$ into two subsets $\displaystyle \large S$ and $\displaystyle \large T$ such that:
	- $\displaystyle \large S \cup T = V$ 
	- $\displaystyle \large S \cap T = \emptyset$  
- The *cut-set* (or cut edges) consists of all edges that have one endpoint in $\displaystyle \large S$ and the other in $\displaystyle \large T$
- the *size of a cut* is the sum of the weights (or number of edges in unweighted graphs) of edges in the cut-set.

>[!note] Cut Property
> for any cut $\displaystyle \large C$ of the graph, if the weight of an edge $\displaystyle \large E$ in the *cut-set* of $\displaystyle \large C$ is *strictly smaller than the weights of all the other edges of the cut-set*, then **this edge belongs to all MSTs of the graph**.

>[!example] Example - Cut Property
> in the examples above, the cut-set,
>$$\displaystyle \Huge \begin{eqnarray} 
>\{(b,c), (a,c), (a,d), (e,d)\}
>\end{eqnarray}$$
>(that Isolates $\displaystyle \large \{a,b,e\}$ from $\displaystyle \large \{c,d\}$) has as the smallest edge:
>$$\displaystyle \Huge \begin{eqnarray} 
>(b,c) \rightarrow W(b,c) < \min (W(a,c), W(a,d), W(e,d))
>\end{eqnarray}$$
>Thus, $\displaystyle \large (b,c)$ will be in all MSTs from this graph.



