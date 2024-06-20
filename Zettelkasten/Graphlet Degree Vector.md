---
tags:
  - math
aliases:
  - GDV
---
A count vector of [[Graphlets]] rooted at a given [[Vertices|vertice]]. It is a vector of size $\displaystyle \large n$.

By defining the maximum degree of [[Graphlets]] to be used, you define the size of the vector.

- If the maximum degree is 2, the vector will have length 1 (only one graphlet)
- If the maximum degree is 3, the vector will have length 4 
- If the maximum degree is 5, the vector will have length 73 

Considering 2 to 5 nodes graphlets, we *capture the interconnectivity of the node with a distance of 4 [[hops]], into a vector of 73 coordinates*. Thus, a very strong *topology* meaning!

---

Let's say that we are defining the GDV for graphlets of degree $\displaystyle \large 3$. So the vector will have 4 numbers.
1. Let's say that this is the Graph $\displaystyle \large G$ and we want to calculate the GDV for the vertice $\displaystyle \large v$:
![[Pasted image 20240620205816.png|160]]

2. The 4 graphlets that exist till degree 3 are this 4:
![[Pasted image 20240620205916.png|250]]

3. The number of times that the node $\displaystyle \large v$ participates in each graphlets can be count like:
![[Pasted image 20240620210017.png|400]]

4. The vector is defined as this numbers:
![[Pasted image 20240620210105.png|200]]
