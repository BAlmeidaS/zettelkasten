In a [[leetcode - khan algorithm|DAG]], the longest possible simple path (i.e., without cycles) has at most N-1 edges because:

1. The graph has no cycles.
2. The longest possible path can only visit each node once.
3. This means no path can exceed N-1 edges.

>[!note] do not confuse with N-1 edges to create a tree
>To be a tree a graph must have $\displaystyle \large N-1$ edges and all the nodes of the graph must be connected.
>However, here what we are saying is, the *path* must have at maximum $\displaystyle \large N-1$

**Bellman-Ford Algorithm** uses a [[dynamic programming|dynamic approach]] rather than a purely [[greedy algorithm|greedy approach]]. 

Each step relaxes **all edges** to progressively refine the shortest path estimates, ensuring that even negative weight edges are correctly accounted for.

*Because of the first affirmation, we say that _Bellman-Ford_ stabilise after $\displaystyle \large N-1$ iterations per node*.

### Bellman-Ford Algorithm
1. **Start at the source node**, setting its distance to `0` and all others to `∞`.
2. **Relax all edges** `N-1` times (where `N` is the number of nodes):
    - For each edge `(u, v, w)`, update `dist[v]` if `dist[u] + w < dist[v]`.
3. **Check for negative cycles** by trying to relax the edges once more (after `n-1` iterations) - if any distance updates, a negative cycle exists! *Thus, Bellman-Ford will not find the answer*, BUT, **it will detect the negative cycle**.


Time Complexity : $\displaystyle \large O(V * E)$
Space Complexity : $\displaystyle \large O(V^2)$
