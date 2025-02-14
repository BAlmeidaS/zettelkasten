---
tags:
  - Russel-n-Norvig-chap-3
---
An [[Uninformed Search]] algorithm

Can be implemented as a [[Best-first search]] using the [[path-cost]] as the *evaluation function*
of the best first search.

It uses [[Priority Queue]] in its implementation. And it *cannot contain negative weights on the edges*!

>[!note]
>Dijkstra's aims to solve the question *Given a weighted graph and a source vertex in the graph, find the ****shortest paths**** from the source to all the other vertices in the given graph.*

| Criterion            | Dijkstra                                                       | Worst-case |
| -------------------- | -------------------------------------------------------------- | ---------- |
| [[Completeness]]?    | Yes                                                            |            |
| [[Cost optimality]]? | Yes                                                            |            |
| [[Time complexity]]  | $\displaystyle \Large O(b^{\lfloor1+C^\star/\epsilon\rfloor})$ |            |
| [[Space complexity]] | $\displaystyle \Large O(b^{\lfloor1+C^\star/\epsilon\rfloor})$ |            |
$\large b$ is the [[branching factor]]
$\large C^\star$ is the cost of the optimal path


![[Pasted image 20231008202637.png]]