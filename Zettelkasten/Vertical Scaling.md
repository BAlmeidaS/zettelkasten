---
tags:
  - computer-science
---
**Vertical scaling** (Scaling up) is a type of [[Scalability]]
 - Making a bigger server
 ![[Pasted image 20250315161802.png|400]]

It's biggest downside is that price usually grows exponentially for bigger machines, and there is a level of load that no unique machine can handle.

Thus, at some point we must use [[Horizontal Scaling]], though is common starting a solution with *vertical scaling* and migrating afterwards.

>[!example]
>A good example is a relational database, that we usually scale up its machine up to a point that we have to split it in multiple servers.