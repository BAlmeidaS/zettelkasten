---
tags:
  - computer-science
aliases:
  - DP
---
*Dynamic Programming* (DP) is a paradigma that can *systematically and efficiently explore **all possible solutions** of a problem*.

Such problems have usually two characteristics:
1. the problem can be *broken down into **overlapping subproblems*** :
	smaller versions of the original problem that are re-used multiple times
2. the problem has an *optimal structure* :
	An optimal solution can be formed from optimal solutions to the overlapping subproblems



Important to notice that:
- [[greedy algorithm]] have optimal substracture, *but **not** overlapping subproblems*.
- [[Divide and Conquer algorithms]]  break a problem into subproblems, *but these subproblems are **not overlapping***.

# Bottom-up or Tabulation

*Bottom-up* is implemented with [[iteration]] and starts at the base cases.

>[!example]

to calculate the Fibonacci, we start by the Bases cases:
$$\displaystyle \Huge \begin{eqnarray} 
F(0) = 0
\\
F(1) = 1
\end{eqnarray}$$
and we go until the value we want

```python
def fib(n: int) -> int:
	if n < 2: return n

	f_0, f_1, f_n = 0, 1, None
	for _ in range(n-1):
		f_n = f_0 + f_1
		f_0, f_1 = f_1, f_n

	return f_n
```


# Top-down / Memoisation

*Top-down* is implemented with [[Recursion]] and made efficient with [[Memoisation]].

>[!note]
>**memoizing** a result means to store the result of a function call, usually in a hashmap or an array, so that when the same function call is made again, we can simply return the **memoized** result instead of recalculating the result.

Usually the **Bottom-up** approach is preferable, due to the overhead that the **call stack** brings with recursion.

# How to identify a DP problem

**The first characteristic** that is common in DP problems is that the problem will ask for the optimum value (maximum or minimum) of something, or the number of ways there are to do something.

- Only with the first characteristic a problem might be solved using [[greedy algorithm]].

**The second characteristic** that is common in DP problems is that future "decisions" depend on earlier decisions. Deciding to do something at one step may affect the ability to do something in a later step.

- This characteristic is what makes a [[greedy algorithm]] invalid for a DP problem - we need to factor in results from previous decisions.

>[!hint]
>When you're solving a problem on your own and trying to decide if the second characteristic is applicable, assume it isn't, then try to think of a counterexample that proves a greedy algorithm won't work. If you can think of an example where earlier decisions affect future decisions, then DP is applicable.

# The framework

*state* :  In a DP problem, a **state** is a set of variables that can sufficiently describe a scenario. These variables are called **state variables**, and we only care about relevant ones.

To solve a DP problem, we need:

1. **A function or data structure that will compute/contain the answer to the problem for every given state**.
	Typically, top-down is implemented with a recursive function and hash map, whereas bottom-up is implemented with nested for loops and an array.

2. **A recurrence relation to transition between states.**
	A recurrence relation is an equation that relates different states with each other.

3. **Base cases, so that our recurrence relation doesn't go on infinitely.**
	Finding the base cases is often the easiest part of solving a DP problem, and just involves a little bit of logical thinking.