---
tags:
  - computer-science
aliases:
  - decrease and coquer
---
A divide-and-conquer algorithm works by _**recursively**_ breaking the problem down into *two or more subproblems* of the same or related type, until these subproblems become simple enough to be solved directly. Then the results of subproblems are combined to form the final solution.

*Divide-and-conquer* algorithm is naturally implemented in the form of [[Recursion]]. *Divide-and-conquer* break the problem down into **two or more** subproblems, rather than a single subproblem.

>[!note]
*decrease and conquer* is when the problem is divided in *one simpler subproblem*

#### Framework
It consists of three steps:
1. **Divide.** Divide the problem SS into a set of subproblems: 
$$\displaystyle \Huge \begin{eqnarray} 
\{S_1, S_2,\dots, S_n\} \text{ where }  n \ge 2
\end{eqnarray}$$
	_i.e._ there are usually more than one subproblem.

2. **Conquer.** Solve each subproblem recursively. 

3. **Combine.** Combine the results of each subproblem.

![[Pasted image 20250226201811.png|450]]


#### Bottom-up and Top-down

*Divide and coquer* have two ways to be solved:

- *Top-down*: each step divides the sub problem, and then it conquers and merge

>[!example] example of top-down - Merge Sort
>Merge sort being performed with a *top-down approach*:
>![[Pasted image 20250226202211.png|500]]
>1. In the first step, we divide the list into two sublists.  (**Divide**)  
>     
>2. Then in the next step, we _**recursively**_ sort the sublists in the previous step.  (**Conquer**)  
>     
>3. Finally we merge the sorted sublists in the above step repeatedly to obtain the final list of sorted elements.  (**Combine**)


- *Bottom-up*: it divides completely the problem until the base cases, and then it merges until it get the initial state

>[!example] example of bottom-up - Merge Sort
>Merge sort being performed with a *bottom-up approach*:
>![[Pasted image 20250226202402.png|500]]
>In the **bottom up** approach, we divide the list into sublists of a single element at the beginning. Each of the sublists is then sorted already. Then from this point on, we merge the sublists two at a time until a single list remains.
