---
tags:
  - Russel-n-Norvig-chap-3
---
What [[Iterative-deepening search]] is to [[Depth-first search - DFS]], IDA* is to [[A* search]]

The cutoff is the $\Large f\_cost(cost+heuristic)$. Each Iteration it will consider nodes only below the cutoff, and we will evoke many times IDA* increasingly gradually its cutoff until it finds the best solution.
