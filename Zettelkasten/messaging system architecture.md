---
tags:
  - computer-science
---
*Messaging Systems* are, by definition, an **asynchronous** architecture. 

![[Pasted image 20250316184437.png|700]]

The main reasons is to address the problems from [[request-response system architecture]]
- The architecture can *keep messages to be processed in the server's pace*.
- *highly parallelised*, since more servers can be added to process
- *failed messages might be resent*.

But there are **drawbacks**:
- **Operational overhead** : The *message system* is another system per se, that must be [[High Availability|high available]], [[Scalability|scalable]] and [[Security|secure]].
- The whole **complexity is higher**.

## Async Messaging Patterns

We usually call the *client* as the **Producer** and the server as the **Consumer**.

There are two main patterns:
- [[messaging queuing]]
- [[publish/subscribe]]