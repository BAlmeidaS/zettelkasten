---
tags:
  - computer-science
---
A type of [[Backup]].

The idea here is to save *only the differences* from the *last full backup*.
![[Pasted image 20250315185144.png]]

From time to time, you create a new base reference (another *full backup*):
![[Pasted image 20250315185336.png]]

PROS:
- smaller than [[Full Backup]]
- shorter creation time

CONS:
- longer restoration time (than [[Full Backup]])