---
tags:
  - computer-science
---
*HTTP* is a [[request-response system architecture|request-response protocol]].

HTTP is:
- *request-response* protocol : Client submits *an HTTP request* and server sends back *an HTTP response*.

- **Older** HTTP uses [[TCP]] is *network protocol*
- **NEW** HTTP/3 uses [[QUIC]] is *network protocol* (an updated version of UDP)

- *New HTTP* has *persistent connection* 

- *New HTTP* support **multiplexing** : many requests are sent over the same TCP connection without waiting for responses.

- *Compression* : request is compressed on the server before sent to the client - reducing [[Latency]] and increasing [[Throughput]]


## HTTP request

*HTTP request* contains basically:
- method (GET, POST, PUT, ...)
- resource (path)
- query string (parameters)
- protocol version
- headers
- (optional) message body

![[Pasted image 20250316200907.png]]

## HTTP response

*Http response* contains:
- protocol version
- status code
- status message
- headers
- (optional) message body

![[Pasted image 20250316201008.png]]