---
tags:
  - computer-languages
aliases:
  - request
  - response
  - response time
  - network delay
  - service time
---
Latency is a broad term and might be applicable into 3 different places. Let's break it down.

When a client a makes a *request* onto a server, it waits for a *response*:
![[Pasted image 20250315181455.png]]

The total time to get the response is called **Response time**.

*Response time* can be broken down into:
- **network delay** : time the request spent *"on the wire"* in both directions
- **service time** : time it took for the *server to process*
$$\displaystyle \Huge \begin{eqnarray} 
\text{response time} := 
\text{network delay} + \text{service time}  
\end{eqnarray}$$

***Latency** have **3** different **main definitions***, and people say "latency" meaning usually one of these:
- **client-side latency** : the *response time* (the most common definition)
- **network latency** : the *network delay*
- **server-side latency** : the *service time*

Usually **Latency is measured in [[Percentiles|percentiles]]**: p90 or p99


>[!hint] 
>![[Pasted image 20250315182210.png|500]]
