---
tags:
  - computer-science
---
*Security* is a [[non-functional requirements|non-functional requirement]]

Security system is defined as the *CIA triad*:
- *C*onfidentiality
- *I*ntegrity
- *A*vailability

**Confidentiality** : Data is protected from unauthorised viewers.
**Integrity** : data is not corrupted or lost, only authorised users can modify it.
**Availability** : authorised users have access to resources when they are needed.

This involves:
- Identity and permissions managements
		Who can access the sys? What can they do?
		How implement authentication and authorisation?
- Infrastructure protections
		How is safe from DDoS attacks?
		SQL injection? cross-site scripting?
- Data protection
		How protect data on the DB? how to protect data in transit?