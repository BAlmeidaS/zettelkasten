---
tags:
  - Negnevistky-chap-4
---
In this step, we aggregate all the [[Fuzzy Sets|fuzzy set]] outputs of all rules fired, to create on unified set, with a unique [[Membership Function]].

![[Pasted image 20231027182729.png]]

It is important that the aggregation happens following the *original membership function* of C. We call *Consequence Correlation* and usually we do **correlation minimisation** / **clipping** the functions on the values found it. Another strategy could be *correlation product* / *scaling*.

![[Pasted image 20231101160840.png|600]]