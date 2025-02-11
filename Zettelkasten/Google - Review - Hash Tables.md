
### Hash map
https://www.youtube.com/watch?v=h2d9b_nEzoA
- 2 components: Key + Value
- hash function: get key as input as create a hash code
	- hash code: position where to store the value
![[Pasted image 20250211165452.png|400]]

lookup : $\displaystyle \large O(1)$ 
insert : $\displaystyle \large O(1)$ 
delete : $\displaystyle \large O(1)$ 

Hash function might lead to *collision* (2 keys, same bucket)
#### What makes good hash functions?
- makes use of all info from the key
- uniformly distributes values across table
- maps similar keys to very different hash values
- use fast operations!

#### how to deal with collision?
##### 1. Linear probing
*Linear Probing* puts the collision input in the *next index available*:

![[Pasted image 20250211170041.png|400]]

*linear probing **have an issue called clustering**

**clustering** : collisions in an area increase the chance of more collisions happen on the same area

*linear probing changes the [[Big-O]] of $\displaystyle \large lookup / insert / deletion$ to $\displaystyle \large O(n)$

##### 2. Separate Chaining

Use *linked lists* to solve collision
![[Pasted image 20250211170455.png|400]]

insert : $\displaystyle \large O(1)$
lookup : $\displaystyle \large O(n/k)$
delete : $\displaystyle \large O(n/k)$

$\displaystyle \large k$ : k is the size of the hash table