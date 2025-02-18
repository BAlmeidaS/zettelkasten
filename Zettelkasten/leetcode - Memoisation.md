*Memorisation* is an optimisation technique used primarily to **speed up** [[Google - Review - Recursion|recursion]] by **storing** the results of expensive function calls and returning the cached result when the same inputs occur again.

Fibonnaci with memoisation

### Pythonic way
```python
from functools import cache

@cache
def factorial(n):
	return n * factor(n-1) if n else 1
```

Another options is using `lru_cache(maxsize=)` by setting a `max_size`  one can have a better control of how much memory will be used [python doc](https://docs.python.org/3/library/functools.html#functools.lru_cache)

[`cache` returns the same as `lru_cache(maxsize=None)`](https://docs.python.org/3/library/functools.html#functools.cache)


#### Explicit way
```python
cache = {}
def recur_fib(N):
	if N < 2:
		return N
		
	if N in cache:
		return cache[N]
	else:
		result = recur_fib(N-1) + recur_fib(N-2)

	cache[N] = result
	return result

return recur_fib(N)
```


### Time Complexity
Since the goal of memoisation if *caching* calls *usually its time will be reduced to **linear***. Though, further evaluation must be done.

>[!example] Example : Fibonacci
>In the Fibonacci example, since each node will be calculated only once, we reduce from $\displaystyle \large O(2^n)$ to $\displaystyle \large O(n)$
>
>![[Pasted image 20250218152757.png]]

