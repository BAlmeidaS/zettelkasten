---
tags:
  - computer-science
---
A type of [[Backup]].

Similar to [[Differential Backup]] but it increments the changes from the last change, instead of from the last full copy
![[Pasted image 20250315185600.png]]

We still, from time to time, create a new *full copy*:
![[Pasted image 20250315185635.png]]

PROS:
- small size
- short creation time

CONS:
- the longest restoration time (it needs to consume many files to do the backup)
- more complex restoration process

