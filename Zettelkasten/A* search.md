---
tags:
  - Russel-n-Norvig-chap-3
aliases:
  - a star
---
An [[Informed Search]] algorithm.

It is a [[Best-first search]] that uses as evaluation function:

$\Large f(n) = path\_cost(n) + heuristic(n)$

$\Large path\_cost(n)$ is the total cost from the $\Large initial\ node$ until the node $\Large n$

It uses [[Priority Queue]] in its implementation

| Criterion | BFS |
| --------- | --- |
| [[Completeness]]? | Yes, in finite spaces |
| [[Cost optimality]]? | Yes, if heuristic is [[Admissible Heuristic]] |
| [[Time complexity]] | $\Large O(b^d)$ |
| [[Space complexity]] | $\Large O(b^d)$ |
$\large b$ is the [[branching factor]]
$\large d$ is the depth of the shallowest solution

With inadmissible heuristic, A* may or may not be cost-optimal - condition on last paragraph of 3.5.2 from Norvig's book.

![[Pasted image 20231009100751.png]]
