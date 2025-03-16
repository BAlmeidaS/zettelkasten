---
tags:
  - computer-science
---
*Eventual Consistency* is a weak [[Consistency|consistency model]].

**If there are no additional updates, eventually all reads will return the latest written value**.

*Eventual Consistency* says that, given enough time without new updates, all replicas will converge to the same state. 

It does not guarantee immediate consistency after a write, allowing **temporary divergence**. This trade-off improves [[High Availability|availability]] and [[Performance]].

>[!note]
>Inconsistency windows is typically small (sub-second). But might cause impression of *missing data*, *out-of-order*, *not all data*
>
> Much faster than [[linearizability]].
>
> DNS is a popular example

