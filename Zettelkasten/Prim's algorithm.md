*Prim's Algorithm* is an algorithm to produces [[Minimum Spanning Tree]] of a [[Weighted Graphs|Weighted Undirected Graph]].

The algorithm goes as follows:
1. **Start with any node** as the initial MST.
2. **Repeatedly add the minimum-weight edge** that connects any node in the MST to a node outside the MST.
3. **Repeat step 2 until all N nodes** are included in the MST.

![[PrimAlgDemo.gif]]

It is a [[greedy algorithm]]. It's proof is related to [[Minimum Spanning Tree|cut property]].


Time Complexity: $\displaystyle \large O(E*log(V))$
Space Complexity: $\displaystyle \large O(V)
$