Tree are usually used to represent *hierarchical data*.
![[Pasted image 20250212150805.png]]

Trees have:
- one root
- multiple nodes

Nodes on a tree have:
- 1 parent
- multiple children

Nodes without children are called *leaf nodes* 

### Breadth-first traversal
look all the nodes in each level before going the deeper levels

### Depth-first traversal
look all the descendants of a node before moving to the next 


Concepts:
- *height* : (of the tree) length of the *longest path to a leaf*
- *depth* : (of the node) length of the *path to its root* 

# Types

## Binary Tree
- nodes have at maximum two children

![[Pasted image 20250212150231.png|300]]

## Binary Search Tree | BST

*Extension of binary trees*.

- $\displaystyle \large left\ children \le parent$
- $\displaystyle \large right\ children \ge parent$

![[Pasted image 20250212150511.png|300]]
## Other trees
[maybe looking before](https://www.thecrazyprogrammer.com/2019/09/types-of-trees-in-data-structure.html)

- AVL Tree
- Red-Black tree
- *N-ary tree* (binary tree is when n = 2)

# balanced vs unbalanced
![[Pasted image 20250212151046.png]]

# Traversals

![[Pasted image 20250212151207.png|250]]
### Preorder
- *root* -> *left* -> *right*
$$\displaystyle \Huge \begin{eqnarray} 
B,A,C 
\end{eqnarray}$$
### Inorder
- *left* -> *root* -> *right*
$$\displaystyle \Huge \begin{eqnarray} 
A,B,C
\end{eqnarray}$$
### Postorder
- *left* -> *right* -> *root*
$$\displaystyle \Huge \begin{eqnarray} 
A,C,B 
\end{eqnarray}$$

