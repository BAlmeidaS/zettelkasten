---
tags:
  - computer-science
---
*Linearizability* is a strong [[Consistency|consistency model]].

**After the update completes, all clients get back the updated value when read data**.

*Linearizability* ensuring that all operations appear to execute atomically in a single, global order that respects real-time.

If one operation completes before another starts, the system must reflect that order. It's practical for small-scale systems but challenging in distributed environments due to latency and synchronization constraints.

>[!note]
> *Linearizability is slow*. Usually it involves a trade-off between *linearizability* and [[High Availability|availability]].
> 
> Typical usage: Banking, e-commerce, distributed locks
