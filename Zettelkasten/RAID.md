---
tags:
  - computer-science
---
*RAID* is one strategy to achieve [[Durability]] in your system.

A technology that manage multiple disks at once, making them operate as *one logical unit*. Every data that is written is copied into multiple disks.

*RAID* stands for Redundant Array of Independent Disks.

### Raid 1

RAID 1 increases [[Durability]] because it maintains an exact copy (mirror) of all data across two or more drives. If one drive fails, the data is still available on the mirrored drive.

RAID 1 increase only the *read* [[Throughput]], since reads might lay in different drives.

RAID 1 has a downside of *losing storage efficiency* because data is used for mirroring.

![[Pasted image 20250315190239.png|500]]


### RAID 0

RAID 0 operates in a different format, it *does not copy the data*, just distributes the data over multiple drives. Therefore, it **reduces** [[Durability]] (one drive fails, all data is lost)!

RAID 0 is useful to **increase** [[Throughput]] (Read & Write)

RAID 0 ends up with *100% of storage efficiency*.

![[Pasted image 20250315190608.png|500]]
