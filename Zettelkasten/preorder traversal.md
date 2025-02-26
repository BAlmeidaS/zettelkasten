---
tags:
  - computer-science
aliases:
  - dfs preorder
---
One way to visit the nodes in [[Depth-first search]]. 

The order to visit the nodes on a **preorder traversal** is:
$$\displaystyle \Huge \begin{eqnarray} 
\text{Root} 
\rightarrow
\text{Left} 
\rightarrow
\text{Right} 
\end{eqnarray}$$

##### Algorithm
- Visit the **current node** first, then recursively visit the **left subtree**, followed by the **right subtree**.

```mathematica
    A
   / \
  B   C
 / \
D   E
```

*Preorder*: `A B D E C`

![[Pasted image 20250226171051.png]]

```python
def preorder(node):
	if node is none:
		return []

	return (
		[node.val] 
		+ preorder(node.left)
		+ preorder(node.right)
	)
```