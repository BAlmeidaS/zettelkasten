---
tags:
  - computer-science
---
A technique used for processing large datasets in a distributed and parallel manner to increase [[Throughput]]

*MapReduce* operates in two main stages: **Map** and **Reduce**.

1. **Map Phase**:
    - The input data is divided into smaller chunks.
    - Each chunk is processed in parallel by "mapper" functions.
    - The mapper transforms the data into key-value pairs.
	
2. **Shuffle & Sort** (Intermediate Step):
    - The key-value pairs from the mappers are grouped by key.
    - They are then sorted and passed to the reducers.
	
3. **Reduce Phase**:
    - The "reducer" function processes the grouped key-value pairs.
    - It aggregates or summarizes the data (e.g., summing values, counting occurrences).
    - The final output is stored.

![[Pasted image 20250315183146.png]]