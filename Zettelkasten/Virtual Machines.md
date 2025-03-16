---
tags:
  - computer-science
aliases:
  - hypervisor
---
Virtual Machines (VM) are an *emulation* of a [[Physical Server]]. 

On top of a shared hardware & OS, there is the **hypervisor**, which manages virtual machines, *by virtualising the hardware and run **full** OS instances* for the VMs.


![[Pasted image 20250316164116.png|500]]

#### Pros
- Cheaper (specially when compared to [[Physical Server]])
- **Easier to maintain and scale**
- Easier to port and to provision

#### Cons
- Because they share resources, they are exposed to *noisy neighbour problem*.
- Less secure than [[Physical Server]] due to *vulnerabilities* in the *hypervisor*