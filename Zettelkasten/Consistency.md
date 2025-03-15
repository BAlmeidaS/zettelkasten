---
tags:
  - computer-science
aliases:
  - consistency model
---
*Consistency* is a [[non-functional requirements|non-functional requirement]]

*Consistency* might change the meaning but, all in all, it refers to one of the two meanings:
- refers to **database transactions** : database constraints are not violated when transaction is executed
- refers to **data replication** : value is the same on all [[Replication|replicas]] and, if not, when they will be. (most common usage)

*Data [[Replication]]* is important not only because of [[Durability]] but because of [[Scalability|read scalability]].

*Consistency* have a model to define *"degrees" of consistency*  and these are called **The consistency models**.

The *consistency models* vary between **weak consistency** to **strong consistency**
![[Pasted image 20250315232526.png]]

Most common **Consistency models**:
- (strong consistency)
- [[strict consistency]]
- [[linearizability]]
- [[monotonic reads]] | [[read-your-writes]] | [[consistent prefix reads]]
- [[eventual consistency]]
- (weak consistency)