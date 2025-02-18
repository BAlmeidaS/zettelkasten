A *recursive function* have the following properties:
1. *base case* : A terminating scenario
2. *recurrence relation* : reduces all cases towards the base case - the relationship between the result of a problem and the result of its subproblem

Optimisation of Recursion:
[[Memoisation]]
[[Tail Recursion]]

### Time Complexity

$\displaystyle \large O(T)$ is typically the product of **the number of recursion** **_invocations_** (denoted as $\displaystyle \large R$) and **the time complexity of calculation** (denoted as $\displaystyle \large O(s)$) that incurs along with each recursion call:
$$\displaystyle \Huge \begin{eqnarray} 
O(T) = R*O(s)
\end{eqnarray}$$

*usually we like to see the execution tree as a [[Google - Review - Trees|n-ary tree]] .

So for a fibonnaci recursive algorithm, this is the execution tree:
![[Pasted image 20250218151140.png|350]]

Thus, its time complexity is $\displaystyle \large O(2^n)$ since the total number of nodes has the upper bound of $\displaystyle \large 2^n -1$


### Space Complexity
$$\displaystyle \Huge \begin{eqnarray} 
\text{Total Space Complexity} = \text{Max Depth of Recursion} \times \text{Space per call}
\end{eqnarray}$$

- Max Depth of Recursion : is the maximum number of times that the function *will be stacked in the **call stack***.
- Space per call : space used each time that the function is executed

>[!example] Example - merge sort with slicing
>The following code is a lazy implementation of merge sort using recursion. It is lazy because uses slices which end-up creating a copy of the array in memory:
>
>```python
>def merge_sort(arr):
>	if len(arr) <= 1:
>		return arr
>		
>	mid = len(arr) // 2
>	left = merge_sort(arr[:mid])
>	right = merge_sort(arr[mid:])
>	
>	return merge(left, right)
>```
>
>In this case, the:
>- Space per call = $\displaystyle \large O(n)$ : because the array is copied via slicing
>- Max Depth of Recursion : $\displaystyle \large O(\log n)$ : because the array is being divided in half
>
>So, for this lazy implementation of merge sort,
>$$\displaystyle \Huge \begin{eqnarray} 
>\text{Space Complexity} = O(n*\log n)
>\end{eqnarray}$$
>If done right, merge sort uses space O(n), it needs to create an auxiliary array.