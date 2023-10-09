An [[Uninformed Search]] algorithm

It expands the search in depth till it finds the last one, than it returns for the others not explored

It expands the search contours as the radius of a circle. Therefore, It uses way less memory than [[Breadth-first search]]

Though is neither complete nor cost optimal ([[Iterative-deepening search]] fixes these):
- It is not complete because it can end up in cycles.
- Not cost optimal because it can find any solution.

It is implemented with an [[Late Goal Test]]

It uses a [[LIFO]] queue

| Criterion | BFS |
| --------- | --- |
| [[Completeness]]? | No |
| [[Cost optimality]]? | No |
| [[Time complexity]] | $\Large O(b^m)$ |
| [[Space complexity]] | $\Large O(b*m)$ |
$\large b$ is the [[branching factor]]
$\large m$ is the maximum depth of the search tree

![[dfs.gif|300]]

pseudo-code on [[Iterative-deepening search]] disregarding the $\large l$

---
last update: 09-10-2023
tags:
