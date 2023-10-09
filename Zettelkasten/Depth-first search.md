
An [[Uninformed Search]] algorithm

It expands the search in depth till it finds the last one, than it returns for the others not explored

It expands the search contours as the radius of a circle. It way less memory than breadth first search, though is neither complete nor cost optimal!

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