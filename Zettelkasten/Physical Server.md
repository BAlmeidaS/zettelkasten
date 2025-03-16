---
tags:
  - computer-science
aliases:
  - bare-metal server
---
Physical Servers that run applications. Usually they are not shared, the owner uses that *machine* in isolation (*bare-metal*).

On top of the hardware and operation system, the apps are deployed

![[Pasted image 20250316163643.png|500]]

#### Pros
- complete control of its software stack
- isolation between tenants
- eliminates noisy neighbour phenomenon
- **high security**

**They are particular good for data-intensive workloads.**

Also, good for *security applications and regulatory requirements*.
#### Cons
- **Expensive**
- **Hard to manage and scale**
- hard to port
- slow to provision

