Given a set of nodes, and a previous graph configuration, we want to know if a pair of nodes are connected (directly or indirectly).

>[!hint]
>Initially, I thought the easiest way is to keep *a set for each "cluster"* and see if the pair are in the same cluster.
>
>It turns out that this is a *bad idea*, mainly because, if later appears an edge connecting this two cluster, the union operation is expensive $\displaystyle \large O(n)$. Even if I optimise by getting the add the smallest into the larger.

The Idea is to create a class, called **UnionFind**. This class will have two methods:
- *union*
- *find*

The main idea is, the class will keep an *array* that has all the *parent nodes* for each node. They are initialised with their own values 
![[Pasted image 20250214173609.png]]

When two nodes are connected (via union function), we update one of their parent nodes.
>[!example]
>![[Pasted image 20250214173844.png]]


*Union* will be optimised using *union by rank*:
	We will keep track of rank of the sets. When a union is performed, the largest rank must be chosen as the parent node of the other node. 
	If they are the same, we increase the rank of one of them (does not matter which, since they are the same) and we use this one as the parent for the other node.

>[!example] Union - union by rank
> in the following example, we want to connect 0 with 5, since 5 has a lower rank, 0 will be the master of 5:
> ![[Pasted image 20250214175228.png]]


*Find* will be optimised using *path compression*:
	every time that a find is performed, we update all the chain with the parent of the final node
	
>[!example] Find - path compression
>let's say that it is *extremely unbalanced the tree* and a find(5) is performed:
> ![[Pasted image 20250214175123.png]]

### Python Implementation

Implementation with both optimisations

```python
class UnionFind:
	def __init__(self, size):
		self.root = [i for i in range(size)] # parent nodes init [0, 1, 2, ...]
		self.rank = [1] * size

	def find(self, x):
		if x == self.root[x]:
			return x
		# path compression using recursion:
		self.root[x] = self.find(self.root[x])
		
		return self.root[x]

	def union(self, x, y):
		root_x = self.find(x)
		root_y = self.find(y)

		if root_x != root_y:
			# union by rank:
			if self.rank[root_x] > self.rank[root_y]:
				self.root[root_y] = root_x 
			elif self.rank[root_x] < self.rank[root_y]:
				self.root[root_x] = root_y
			else:
				self.root[root_y] = root_x
				self.rank[root_x] += 1

	def connected(self, x, y):
		return self.find(x) == self.find(y)
```

Time complexity:
- Constructor : $\displaystyle \large O(n)$
- Find : $\displaystyle \large O(\alpha(n))$
- Union : $\displaystyle \large O(\alpha(n))$
- Connected : $\displaystyle \large O(\alpha(n))$

$\displaystyle \large \alpha(N)$ : $\displaystyle \large \alpha$ refers to the *Inverse Ackermann function*. In practice, it is constant! 
- $\displaystyle \large O(\alpha(n)) = O(1)$ on average.
