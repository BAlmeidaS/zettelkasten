---
tags:
---
A more academic approach might be found here : [[Dijkstra's algorithm - Uniform-cost Search]]

---

*Dijkstra's Algorithm* uses a [[greedy algorithm|greedy approach]]. Each step selects the _minimum weight_ from the currently reached vertices (considering the shortest known distance to those vertices) to find the *shortest path to other vertices*.

Algorithm:
1. **Start at the source node**, setting its distance to `0` and all others to `∞`.
2. **Pick the node with the smallest known distance** (initially the source).
3. **Update distances** to its neighbouring nodes if a shorter path is found.
4. **Mark the node as visited** and never revisit it.
5. **Repeat steps 2–4** until all nodes are visited or the target is reached.

In order to perform *step 2* use [[Google - Review - Heap or Priority Queue|heaps]] or keep the distances with an *array structure*

>[!example]
>![[Pasted image 20250217185453.png]]


*Dijkstra's algorithm only work with **positive weights***.
