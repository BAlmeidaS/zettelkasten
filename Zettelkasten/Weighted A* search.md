An [[Informed Search]] algorithm.

It is a [[Best-first search]] that uses as evaluation function:

$\Large f(n) = path\_cost(n) + W * heuristic(n)$

$\Large path\_cost(n)$ is the total cost from the $\Large initial\ node$ until the node $\Large n$
$\Large W$ is the weight of the heuristic

[[A* search]] is good but expands too much nodes. If we allow sub-optimal results.

---
last update: 09-10-2023
tags: