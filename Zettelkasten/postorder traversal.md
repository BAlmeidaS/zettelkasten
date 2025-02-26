---
tags:
  - computer-science
aliases:
  - dfs postorder
---

One way to visit the nodes in [[Depth-first search]]. 

The order to visit the nodes on a **postorder traversal** is:
$$\displaystyle \Huge \begin{eqnarray} 
\text{Left} 
\rightarrow
\text{Right} 
\rightarrow
\text{Root} 
\end{eqnarray}$$

##### Algorithm
- Recursively visit the **left subtree**, then the **right subtree**, and visit the **current node** last.

```mathematica
    A
   / \
  B   C
 / \
D   E
```

*Postorder*: `D E B C A`

![[Pasted image 20250226170705.png]]

```python
def postorder(node):
	if node is none:
		return []

	return (
		postorder(node.left)
		+ postorder(node.right)
		+ [node.val] 
	)
```