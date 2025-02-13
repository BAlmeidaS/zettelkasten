Heap can be max or min!

They are a type of [[Google - Review - Trees|binary tree]] where the top has a special property and it's always complete!
![[Pasted image 20250213153909.png|450]]



### focusing all min because python is like this
- building a max heap using a min is just inverting the values

The top of a *min heap* is always the **smallest value**

- peek : $\displaystyle \large O(1)$ 
- push : $\displaystyle \large O(\log n)$ 
- pop : $\displaystyle \large O(\log n)$ 

*heap sort is an algorithm to sort the values in an array* by **heapify** the array, and constantly remove the top. 
# Insert
Always insert in the next empty spot, top to bottom, left to right
![[compressed.gif|450]]

after inserting, it **bubbles data up** until it keeps the properties of the heap (smallest value is on top)
*In this example a 3 was added in the first space available and bubbled up*:
![[compKooha-2025-02-12-22-29-29.gif|450]]


# Remove
To take the min value we just need to remove the top, but this will leave the heap with the top empty
![[Pasted image 20250213100455.png|450]]

Then *the last element will be swapped* with the top
![[Pasted image 20250213100616.png|450]]

and we **bubble it down**, swapping with the smallest amount among the children until it is the smallest among the triplet:
![[compKooha-2025-02-13-10-06-46.gif|450]]

# implementation
since the *heap* has this property of "always been complete", which means that the nodes are added in order

So, an *array* will be the easiest implementation
![[Pasted image 20250213101323.png|600]]
![[Pasted image 20250213102532.png|400]]

# Python - heapq module
*heapify* is $\displaystyle \large O(n)$. It guarantees a valid min-heap but not a full sorted array

*heapify is **faster** than n times a heappush* - Tho the results are the same, n times heappush, takes $\displaystyle \large O(n \log n)$.

```python
import heapq

arr = [0, 3, 1, 3, 2, 10, -2, 9]

# heapify #
heapq.heapify(arr) # O(n)
arr # [-2, 2, 0, 3, 3, 10, 1, 9]

# push #
heapq.heappush(arr, 7) # push 7 - O(log n)
arr # [-2, 2, 0, 3, 3, 10, 1, 9, 7]

# pop #
min_v = heapq.heappop(arr)
min_v, arr # -2,  [0, 2, 1, 3, 3, 10, 7, 9]

# heap sort #
def heapsort(arr):
  heapq.heapify(arr)
  new_arr = [0] * len(arr)

  for i in range(len(arr)):
    _min = heapq.heapify(arr)
    new_arr[i] = _min
  
  return new_arr

# max heap #
arr = [-x for x in arr] # invert the signal and do all the the ops considering the neg input
```

### heaps with tuples

in *python*, you can push tuples inside the heap. In this case, the first value of the tuple will be used to sort!