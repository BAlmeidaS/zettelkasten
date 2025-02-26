---
tags:
  - computer-science
---
*Kadane's algorithm* is a [[greedy algorithm]] to calculate the max sum of a [[subarray]] of an array. 

The idea is to find the *subarray* that has the *max sum*. 

To do this, is creates two variables, `cur_sum` and `max_sum`. It runs in *linear time*.

it iterate over every element of the array:
1. `cur_sum` is updated by the **max** of the number, and the sum of that number with the cumulative value so far
		The rationale here is, either we should consider *all that pass before* or we should *get rid of all that has passed and consider only the actual element that we are*
2. update `max_sum` with the *max* between `max_sum` and `cur_sum`


```python
def max_subarray(numbers):
    best_sum = float('-inf')
    current_sum = 0
	
    for x in numbers:
        current_sum = max(x, current_sum + x)
        best_sum = max(best_sum, current_sum)
    return best_sum
```

It is *greedy because every step considers only what is more valuable between **get the past of cur_sum** or **consider only from this point***.

>[!note]
>The same algorithm can be used to find the **min sum**, by just replacing the `max` with a `min`
