- linear data structures
- flexible size

# Stack
*LIFO* : Last In First Out
![[Pasted image 20250212204535.png]]

*in python **use a list*** :
```python
stack = []

stack.append(1) # push on the stack

last_item = stack.pop() # pop from the top

stack[-1] # peek the top
```

# Queue
*FIFO* : First In First Out
![[Pasted image 20250212204553.png|500]]

*in python **use a deque*** 
```python
from collection import deque

queue = deque()

queue.append(1) # push in the front

queue.popleft() # remove from the back O(1)

queue.is_empty() # check empty

queue[0] # peek the front
```


# Python - queue module

Python has a module called *queue* and it is specially good for multithread, becasue *it is **thread-safe***.

##### Stack - queue module
```python
from queue import LifoQueue

stack = LifoQueue()

stack.empty() # check if empty

stack.put(1) # stack value

if not stack.empty(): # must check before get
	last_item = stack.get() # pop() and get the value

# DOES NOT HAVE A PEEK!!!! super bad =/
# have to pop() and put again
```

##### Queue - queue module
```python
from queue import Queue

queue = Queue()

queue.empty() # check if empty

queue.put(1) # stack value

if not queue.empty(): # must check before get
	first_item = queue.get() # pop() and get the value

# DOES NOT HAVE A PEEK!!!! super bad =/
# q.queue[0] is a workaround BUT is not threadsafe 
```