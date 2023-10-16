---
tags:
  - Russel-n-Norvig-chap-3
aliases:
  - RBFS
---
The idea is a combination between [[Depth-first search]] and [[Greedy Best-first search]]. You keep doing DFS optimized by the total_cost (from Greedy Best FS), once you find a node that costs more than expected, you unwinds back and try a different path.

![[Pasted image 20231009121158.png]]

![[Pasted image 20231009121106.png]]
