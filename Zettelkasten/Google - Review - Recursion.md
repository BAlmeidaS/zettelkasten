A *recursive function* have the following properties:
1. *base case* : A terminating scenario
2. *recurrence relation* : reduces all cases towards the base case - the relationship between the result of a problem and the result of its subproblem

Optimisation of Recursion: [[leetcode - Memoisation]]

#### Time Complexity

$\displaystyle \large O(T)$ is typically the product of **the number of recursion** **_invocations_** (denoted as $\displaystyle \large R$) and **the time complexity of calculation** (denoted as $\displaystyle \large O(s)$) that incurs along with each recursion call:
$$\displaystyle \Huge \begin{eqnarray} 
O(T) = R*O(s)
\end{eqnarray}$$

*usually we like to see the execution tree as a [[Google - Review - Trees|n-ary tree]] .

So for a fibonnaci recursive algorithm, this is the execution tree:
![[Pasted image 20250218151140.png|350]]

Thus, its time complexity is $\displaystyle \large O(2^n)$ since the total number of nodes has the upper bound of $\displaystyle \large 2^n -1$

