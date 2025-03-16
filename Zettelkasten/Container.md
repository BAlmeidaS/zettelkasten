---
tags:
  - computer-science
aliases:
  - container engine
---
*Container* is a **lightweight, standalone, executable package of software** that includes **everything** needed to run an app:
- code
- runtime
- system tools
- system libraries
- settings

Instead of virtualise the hardware as with a [[Virtual Machines|hypervisor]], container rely on **container engine** that *virtualise the operating system*, they run on top of the *OS kernel directly* but they *isolate the applications*, not the hardware.

![[Pasted image 20250316164918.png|500]]
#### Pros
- Lightweight
- **Scalable and Portable**
- *Easy to maintain and deploy*.
- Faster to start

#### Cons
- less secure than [[Virtual Machines]]
- less flexible when dealing with multiple Operating Systems (you need the same OS that a container was created for to run it)
