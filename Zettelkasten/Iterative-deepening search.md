---
tags:
  - Russel-n-Norvig-chap-3
---
An [[Uninformed Search]] algorithm

[[Depth-first search]] with steroids!

It solves the problem of completeness and cost optimally. How? Adding a depth limit to search, called $\large l$ , it goes till $\large l$ and considers that the "bottom" of the graph.

It is *iterative*, because the idea is to interactively adding l + 1 and running again and again the algorithm. The top part of the search tree will be checked many times but asymptotically the big O for time complexity is the same of the DFS.

It uses a [[LIFO]] queue

| Criterion | Iterative-deepening search |
| --------- | --- |
| [[Completeness]]? | Yes - if b and the state space is finite |
| [[Cost optimality]]? | Yes - if actions are all identical related to costs|
| [[Time complexity]] | $\Large O(b^l)$ |
| [[Space complexity]] | $\Large O(b*l)$ |
$\large b$ is the [[branching factor]]
$\large l$ is the depth limit

![[dfs.gif|300]]

![[Pasted image 20231009021334.png]]
