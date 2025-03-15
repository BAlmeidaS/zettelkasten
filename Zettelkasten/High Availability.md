---
tags:
  - computer-science
aliases:
  - service-level objective
  - slo
  - sla
  - availability
---
*High availability* is a [[non-functional requirements|non-functional requirement]].

>[!summary]
> ***Small downtime***.
>
> System knows how to handle **expected failures** (server crash, network problems, power outage) 

It is usually *measure in percentage* and has two main meanings:
- system **uptime**, the percentage the sys has been available. 99% means unavailable about 3.65 days a year
- **success ratio** of requests. 99% means 1 request out of 100.

*The percentage number that shows availability is called **Service-level Objective (SLO)***. 
While the commitment between the provider and client is called *Service Level Agreement (SLA)*.

High availability is a conscious decision about being available, thus it lies on some *architecture decisions*:
1. **build redundancy** to eliminate single points of failure
		(regions, fallback, data replication)
2. *switch from one server to another **without losing data***.
		(DNS, load balancing, reverse proxy, API gateway)
3. system must **protect** itself from **atypical client behaviour**.
		(load shedding, rate limiting, shuffle sharding)
4. system must **protect** itself from **failures and performance degradation**.
		(timeouts, circuit breaker, retries)
5. **detect failuers as they occur**.
		(monitoring)


Some process help a system to have high availability:
- Code review and code approved
- QA
- deployment quick and safe
- automated rollbacks
- monitor sys utilisation and add resources on demand
- disaster recovery
- root cause analysis
- team culture