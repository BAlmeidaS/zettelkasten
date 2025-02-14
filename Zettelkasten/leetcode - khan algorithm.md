---
tags: 
aliases:
  - how to check if a graph is a DAG
---
**Khan's Algorithm**

Algorithm useful too *check* if a *graph* is a DAG

The idea is calculate the *in-degree* of each node using the *adjacency list*, resulting in the following dictionary:
$$\displaystyle \Huge \begin{eqnarray} 
\{
\\ & \quad node_1: in\_degree(node_1)
\\ & \quad node_2: in\_degree(node_2)
\\ & \quad ...
\\
\}
\end{eqnarray}$$

Than, get all the $\displaystyle \large node_i$ that have *in-degree = 0*, and *stack them*.
Set a visits counter as 0.

Iterate while this stack have items:
	1. pop the stack
	2. visits counter ++
	3. for each neighbour of the $\displaystyle \large node$ popped from the stack
		1. reduce it $\displaystyle \large in\_degree$ in 1 (*we are kinda removing the degrees 0 from the graph*)
		2. if the new $\displaystyle \large in\_degree$ of the neighbour is 0, add it on the stack

At the end, if the visits counter were the same as the number of nodes on the graph, *there is no cycle*. Otherwise, *the graph have cycles*.

The same outcome can be draw by seeing the, in the *in-degree* dictionary, there will be nodes with degree > 0 at the end if there is a cycle.

---

It is possible to validate if it is a DAG by using [[Depth-first search|DFS]] as well.

The trick is keep a set called *path* and add nodes while you go deep, and removing when you return

```python
def is_DAG(adj_list: dict[int, list[int]]) -> bool:
	path = set()
	seen = set()
	
	def dfs_without_cycle(node):
		if node in path:
			return False
		
		if node in seen:
			return True
	
		path.add(node)
		seen.add(node)
	
		for neigh in adj_list[node]:
			if not dfs_valid(neigh):
				return False
	
		path.remove(node)
		return True
	
	
	for node in adj_list.keys():
		if node not in seen and not dfs_without_cycle(n):
			return False
	return True
```


