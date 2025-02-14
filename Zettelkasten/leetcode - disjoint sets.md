Given a set of nodes, and a previous graph configuration, we want to know if a pair of nodes are connected (directly or indirectly).

>[!hint]
>Initially, I thought the easiest way is to keep *a set for each "cluster"* and see if the pair are in the same cluster.
>
>It turns out that this is a *bad idea*, mainly because, if later appears an edge connecting this two cluster, the union operation is expensive $\displaystyle \large O(n)$. Even if I optimise by getting the add the smallest into the larger.

The Idea is to create a class, called **UnionFind**. This class will have two methods:
- *union*
- *find*

The main idea is, the class will keep an *array* that has all the *master nodes* for each node. When two nodes are connected (via union function), we update one of their master nodes.

*Union* will be optimised using *union by rank*:
	We will keep track of rank of the sets. When a union is performed, the largest rank must be chosen as the master node of the other node. 
	If they are the same, we increase the rank of one of them (does not matter which, since they are the same) and we use this one as the master for the other node.

*Find* will be optimised using *path compression*:
	every time that a find is performed, we update all the chain with the master of the final node

```python
	
```
