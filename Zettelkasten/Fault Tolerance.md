---
tags:
  - computer-science
---
*Fault tolerance* is a type of [[non-functional requirements|non-functional requirement]].

>[!summary]
> ***close to zero downtime***.
>
> System knows how to handle **unexpected failures** (load spikes, dependency failures) 

>[!summary] Wikipedia
>*Fault tolerance* is the property that enables a system *to continue operating properly* in the event of *one or more faults within some of its components*.

A *Fault tolerant* system isolates [[Difference between error, fault and failure|faults]] to avoid them to cause [[Difference between error, fault and failure|failures]].

One can understand *fault tolerance* as a stronger version of [[High Availability]].

>[!info] 
> *fault tolerant* systems are often defined as [[High Availability]]. Nonetheless, high available means usually *minimise the downtime*, whereas, fault tolerance has a goal of *zero downtime*.
>
> A car is a high available system, if a tire failures we have another one, with a short downtime we can replace it.
> An airplane is a fault tolerance system, it cannot stop to change the systems if one fails. It must rely on other engines taking over the place of the failed one.



