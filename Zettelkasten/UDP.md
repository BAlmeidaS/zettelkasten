---
tags:
  - computer-science
---
*UDP* is a [[request-response system architecture|network protocol]].

*UDP prioritises **Time over Reliability***.

UDP is:
- **no connection** : sender transmits the messages without verifying the readiness of the receiver 

- **no reliability** : data may get lost

- **no** *acknowledgements, retransmission or order guarantee*

- **no** flow control

* it uses [[checksum]] : to ensure data correctness

- *broadcast* : a single message can be transferred to all recipients

- *multicast* : a single message is routed *only to intended* recipients

- **simpler and faster** than [[TCP]]