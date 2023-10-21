---
tags:
  - Russel-n-Norvig-chap-3
---
An [[Uninformed Search]] algorithm

Can be implemented as a [[Best-first search]] using the [[path-cost]] as the evaluation function of the best first search.

| Criterion | Dijkstra |
| --------- | --- |
| [[Completeness]]? | Yes |
| [[Cost optimality]]? | Yes |
| [[Time complexity]] | $\displaystyle \Large O(b^{\lfloor1+C^\star/\epsilon\rfloor})$ |
| [[Space complexity]] | $\displaystyle \Large O(b^{\lfloor1+C^\star/\epsilon\rfloor})$ |
$\large b$ is the [[branching factor]]
$\large C^\star$ is the cost of the optimal path

It uses [[Priority Queue]] in its implementation

![[Pasted image 20231008202637.png]]
