---
tags:
  - computer-science
---
*Request-response systems* might be either **synchronous** or **asynchronous**. 

![[Pasted image 20250316184146.png|500]]

The main reason and the main advantage is:
- **easy and fast to implement**

Though some problems with this architecture:
- *what should the client do when server is not available?*
- *what should the client do with failed requests?*
- *what should the client do when server gets slower?*

>[!example] an async example 
>An *asynchronous* example not necessarily involves a callback, rather is *more common* to see a *client that fires a bunch of async calls* and builds the needed object when all of them return.
>
>![[Pasted image 20250316185053.png|600]]
