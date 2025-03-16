---
tags:
  - computer-languages
aliases:
  - Competing Consumers
  - Request/Response messaging
---
*Message queuing* is a pattern of [[messaging system architecture]].

![[Pasted image 20250316190317.png]]

The main goal here is *a single consumer gets the message*!

## Competing consumers

If there are more than one consumer, **they will compete by the messages**. This pattern of competing by message is called **competing consumers**.

![[Pasted image 20250316190818.png|400]]

This pattern improves:
- [[Scalability]] : add more instances *as messages increases over time*.
- [[High Availability|Availability]] : When a *consumer fails* others continue processing.
- [[Performance]] : Add more instances to improve [[Throughput]]

## Request/Response messaging

This pattern is used when the *producer* **needs to get a response back**. Usually is implemented by adding a new callback queue, where the *consumer* returns the answer (very similar to a hook).

The *message* sent by the producer usually *specifies the callback queue that the **producer will be listening**.

![[Pasted image 20250316191228.png]]

## Priority Queue

The messages queued on the queue have a *priority* attached, so it is not [[FIFO]], it follows this priority. Every time that a new message arrives, the *queue system resort the messages to be consumed*.

If a *priority queue **is not support** by the message sys* then a solution is having **multiple queues, one for each priority**, and the **polls of consumers are different based on the priorities**.

![[Pasted image 20250316191853.png]]

## Claim check

Useful when the message to be passed is **large**, so the message is a "claim" to be collected in another place (*I like to call this "message-by-reference"*). The *consumer gets a message that points out to where is the large data*.

![[Pasted image 20250316192126.png]]

