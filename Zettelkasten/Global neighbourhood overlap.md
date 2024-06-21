---
tags:
  - machine-learning
  - computer-science
aliases:
  - Katz index
---
*Global neighbourhood overlap* is a possible feature to measure how much two [[Vertices]] are *close to be connected*, to predict [[Edge-level Task - Graph Neural Networks|if a new edge should be added]].

Kind of evolving [[Local neighbourhood overlap]], *Global* looks to the entire graph.

- *Katz index*: count the number of [[path on a graph|paths]] of all lengths between a given pair of nodes
	- using [[Powers of Adjacency Matrix]] we can compute how many paths of size $\displaystyle \large l$ are
	- The *katz index*  $\displaystyle \large S$ is defined as: $$\displaystyle \Huge \begin{eqnarray} 
S_{v_1v_2} = \sum^{\infty}_{i=1}\beta^i A^i_{v_1v_2}
\end{eqnarray}$$
       where $\displaystyle \large \beta$  is a discount factor, between 0 and 1
	- In closed form:	$$\displaystyle \Huge \begin{eqnarray} 
S = \sum^{\infty}_{i=1}\beta^i A^i = (I - \beta A)^{-1} - I
\end{eqnarray}$$
