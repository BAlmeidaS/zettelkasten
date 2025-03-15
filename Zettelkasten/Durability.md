---
tags:
  - computer-science
---
*Durabilit* is a [[non-functional requirements|non-functional requirement]].

The definition is, *once data is successfully submitted to the system, it is not lost*.

>[!ssummary] 
>*Storing data without losing it*

Generally, system achieve *durability* by *creating and maintaining **multiple copies** of data*. The main strategies are:
- [[Backup]]
- [[RAID]]
- [[Replication]]
- versioning, safeguards against deletion, etc...

Those mechanisms are not mutually exclusive, they might be used together.

*durability* is not about just copying the data, but *also validating that the data integrity*, usually by calculating [[checksum]] of the data, and comparing across its copies.



