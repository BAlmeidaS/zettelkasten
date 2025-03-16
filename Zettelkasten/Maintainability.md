---
tags:
  - computer-science
---
*Maintainability* is a [[non-functional requirements|non-functional requirement]].

After a product is launch, everything that goes after is related to *Maintainability*.

- Failure modes
		if a component fails, what happens to the rest of the system?
- Mitigations
		How the system handles network partitions
- Monitoring
		how we monitor health of the sys?
		In case of a [[Difference between error, fault and failure|failure]], how do we know what exactly is broken?
- Testing
		How to test individual components?
		How to test flows end-to-end
- Deployment
		How to deploy safely?
		How to rollback?