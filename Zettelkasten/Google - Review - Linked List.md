---
tags:
---
list of nodes where each one is connected to the next
![[Pasted image 20250212135241.png|500]]

- *first node* is called **head**
- *last item* points to a **null** object
#### Singly-linked list

Each node has:
- data : info
- next : next node
![[Pasted image 20250212135125.png|300]]

#### doubly-linked list
Each node has:
- data : info
- next : next node
- prev : prev
![[Pasted image 20250212135338.png|300]]
#### Circular linked list
- last node is connected to the first

---
#### overall
- takes more memory than array, since it stores the data + 1 (or 2) pointers

lookup : $\displaystyle \large O(n)$
add: O(1) (last) or O(n) (position)