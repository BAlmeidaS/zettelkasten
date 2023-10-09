An [[Informed Search]] algorithm.

It is a [[Best-first search]] that uses as evaluation function:

$\Large f(n) = path\_cost(n) + heuristic(n)$

$\Large path\_cost(n)$ is the total cost from the $\Large initial\ node$ until the node $\Large n$

It uses [[Priority Queue]] in its implementation

| Criterion | BFS |
| --------- | --- |
| [[Completeness]]? | Yes, in finite spaces |
| [[Cost optimality]]? | Yes, if heuristic is at least [[Admissible Heuristic]] |
| [[Time complexity]] | $\Large O(\lvert V \rvert)$, with [[Good heuristics in search space]]: $\Large O(b*m)$|
| [[Space complexity]] | $\Large O(\lvert V\rvert)$, with [[Good heuristics in search space]]: $\Large O(b*m)$|
$\large b$ is the [[branching factor]]
$\large m$ is the maximum depth of the search tree




![[Pasted image 20231009093705.png]]

---
last update: 09-10-2023
tags: