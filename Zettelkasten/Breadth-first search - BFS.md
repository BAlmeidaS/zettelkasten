An [[Uninformed Search]] algorithm

It expands the search layer by layer.

It expands the search contours as the perimeter of a circle. It is super memory heavy (space complexity exponential)

Can be implemented with an [[Early Goal Test]] - which is an enhancement.

It uses a [[FIFO]] queue

| Criterion | BFS |
| --------- | --- |
| [[Completeness]]? | Yes |
| [[Cost optimality]]? | Yes |
| [[Time complexity]] | $\Large O(b^d)$ |
| [[Space complexity]] | $\Large O(b^d)$ |
$\large b$ is the [[branching factor]]
$\large d$ is the depth of the shallowest solution


![[bfs.gif|300]]


![[Pasted image 20231008200453.png]]

---
last update: 09-10-2023
tags:
