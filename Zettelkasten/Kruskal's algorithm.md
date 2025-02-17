*Kruskal's Algorithm* is an algorithm to produces [[Minimum Spanning Tree]]

The algorithm goes as follows:
1. *Sort Ascending* all the edges by their weight
2. Add edges in that order into the MST. *Skip the edges that produce cycles!*
3. Repeat step 2 until *N-1* edges. Being N the number of nodes.

![[KruskalDemo.gif]]
>[!abstract] why *N-1* edges?
>A tree using *N* nodes has *N-1* edges, regardless if it is a Minimum spanning tree. If it has more, it has cycles! If it has less, it is not fully connected

This is a [[greedy algorithm]]!

#### Time Complexity
$$\displaystyle \Huge \begin{eqnarray} 
O(E * \log E)
\end{eqnarray}$$
 - Sorting in the first step take this time complexity
 - The 2 step, in the worst case, will take $\displaystyle \large O(E*\alpha(V)) = O(E)$


#### Space Complexity
$$\displaystyle \Huge \begin{eqnarray} 
O(V)
\end{eqnarray}$$
- for the spanning tree.
- Depending on the sort algorithm some extra space might be required.
