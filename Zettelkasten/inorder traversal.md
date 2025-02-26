---
tags:
  - computer-science
aliases:
  - dfs inorder
---
One way to visit the nodes in [[Depth-first search]]. 

The order to visit the nodes on an **inorder traversal** is:
$$\displaystyle \Huge \begin{eqnarray} 
\text{Left} 
\rightarrow
\text{Root} 
\rightarrow
\text{Right} 
\end{eqnarray}$$

##### Algorithm
- Recursively visit the **left subtree** first, then visit the **current node**, and finally the **right subtree**.

```mathematica
    A
   / \
  B   C
 / \
D   E
```

*Inorder*: `D B E A C`

![[Pasted image 20250226170812.png]]

```python
def inorder(node):
	if node is none:
		return []

	return (
		inorder(node.left)
		+ [node.val] 
		+ inorder(node.right)
	)
```