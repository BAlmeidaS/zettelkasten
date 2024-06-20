---
tags:
  - math
---
*Adjacency Matrix* is a form to represent [[Graphs]]. The idea is to create a matrix where:
- the columns and rows are nodes
- the cells represent if the nodes are connected

$$\displaystyle \Huge \begin{eqnarray} 
dim(A) &=& N \times N \\
A_{ij} &=& 1, \text{ if there is an edge from node i to j} \\
A_{ij} &=& 0, \text{ otherwise}
\end{eqnarray}$$

For [[Undirected Graphs]], Adjacency Matrix is *symmetric*; Whereas, for [[Directed Graphs]], they are not.

**Adjacency Matrix are extremely [[sparse vector|sparse]]** 

---

[[Node Degree]] can be calculated as the summation across a given row or colum:
$$\displaystyle \Huge \begin{eqnarray} 
k_i &=& \sum_{i=1}^{N}A_{ij} &=& \sum_{j=1}^{N}A_{ij}
\end{eqnarray}$$
For *Undirected graphs*, the over *columns* are the [[In-degree and Out-degree|in-degree]] and over *rows* are the [[In-degree and Out-degree|out-degree]]
$$\displaystyle \Huge \begin{eqnarray} 
k_i^{in} &=& \sum_{j=1}^{N}A_{ij} \\
k_j^{out} &=& \sum_{i=1}^{N}A_{ij}
\end{eqnarray}$$
---


>[!example] Example - undirected graph
>![[Pasted image 20240620155243.png|200]]
>$$\displaystyle \Huge \begin{eqnarray} 
>A = \begin{bmatrix} 
>0 & 1 & 0 & 1 \\ 
>1 & 0 & 0 & 1 \\ 
>0 & 0 & 0 & 1 \\ 
>1 & 1 & 1 & 0 \\ 
>\end{bmatrix}
>\end{eqnarray}$$

>[!example] Example - directed graph
>![[Pasted image 20240620155611.png|200]]
>$$\displaystyle \Huge \begin{eqnarray} 
>A = \begin{bmatrix} 
>0 & 0 & 0 & 1 \\ 
>1 & 0 & 0 & 0 \\ 
>0 & 0 & 0 & 0 \\ 
>0 & 1 & 1 & 0 \\ 
>\end{bmatrix}
>\end{eqnarray}$$

