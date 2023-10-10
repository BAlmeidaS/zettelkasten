---
tags:
  - Russel-n-Norvig-chap-3
---
An [[Informed Search]] algorithm.

It is a [[Best-first search]] that uses as evaluation function with the heuristic:

$\Large f(n) = heuristic(n)$

It uses [[Priority Queue]] in its implementation

| Criterion | BFS |
| --------- | --- |
| [[Completeness]]? | Yes, in finite spaces |
| [[Cost optimality]]? | No |
| [[Time complexity]] | $\Large O(\lvert V \rvert)$, with [[Good heuristics in search space]]: $\Large O(b*m)$|
| [[Space complexity]] | $\Large O(\lvert V\rvert)$, with [[Good heuristics in search space]]: $\Large O(b*m)$|
$\large b$ is the [[branching factor]]
$\large m$ is the maximum depth of the search tree


![[Pasted image 20231009093705.png]]
