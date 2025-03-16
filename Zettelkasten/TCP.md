---
tags:
  - computer-science
---
*TCP* is a [[request-response system architecture|network protocol]].

**TCP prioritises *Reliability over Time***.

TCP is:
- **connection-oriented** : connection is established *before* data is sent

- *handshake* : multi-step connection establishment process (3-step)
		Client-server (hi), server-client (hello), client-server (I will start), ... 
		
- [[Reliability|reliable]] : lost packets are resent
	- by using *sequence numbers* that identify packages.
			consume them on the *right order*, and discard duplicates
	- by using *acknowledgements*
			sender knows when a package needs to be resent
	- by using [[checksum]]
			ensure data correctness

- flow control : limit the rate a sender transfers
