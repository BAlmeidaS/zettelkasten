---
aliases:
  - Tail Call Optimisation
  - TCO
---

**Python is *NOT* optimised for tail recursion**. The argument is that it optimises readability and prioritises *iteration over recursion*

Still, the definition is:

**Tail recursion** is a recursion where the recursive call is the final instruction in the recursion function. And there should be only **one** recursive call in the function.

```python
def factorial(n):
	if n == 0:
		return 1
	return factorial(n-1) * n

def tail_factorial(n, accumulator = 1):
	if n == 0:
		return accumulator
	return tail_factorial(n-1, accumulator * n)
 ```
 