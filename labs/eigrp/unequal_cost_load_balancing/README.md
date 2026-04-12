### Lab Files
- topology.yaml - Cisco Modeling Labs file for recreating this topology
To use this lab, import the topology.yaml file into Cisco Modeling Labs

<h1>EIGRP - Unequal Cost Load Balancing</h1>

# Overview

EIGRP is an advanced distance vector routing protocol, originally Cisco proprietary. For this lab I created in scratch in CML on a dedicated server I host.



This lab demonstrates EIGRP unequal-cost load balancing using the variance command. Interface delay was manipulated to influence path metrics and create multiple feasible successors.
<img width="1904" height="628" alt="image" src="https://github.com/user-attachments/assets/fece605a-3c1a-4db3-b851-1f727388f8fd" />


<img width="1040" height="671" alt="image" src="https://github.com/user-attachments/assets/63af0928-7803-4511-9e6b-c3f13014a608" />


R5 has <b>1 successor and 2 feasible successors for the 10.0.12.0/30 network</b> as both alternative paths satisfy the feasibility condition <b>RD < FD</b>. Only paths that satisfy the feasibility condition (RD < FD) are eligible to be added to the routing table when variance is applied.

<img width="478" height="89" alt="image" src="https://github.com/user-attachments/assets/56dcabce-51f5-4398-929f-99850fd5865a" />


The highest metric path (28416) requires a minimum variance of approximately 6.16 (28416 / 4608). Since variance must be an integer, a value of 7 is required to include the third feasible path into the routing table.


Before applying the variance command, R5 reaches the 10.0.12.0/30 network via a single best path (10.0.35.1).

<img width="650" height="21" alt="image" src="https://github.com/user-attachments/assets/cf5b2b2c-72b4-4d16-ade8-5391916195da" />


<img width="739" height="569" alt="image" src="https://github.com/user-attachments/assets/ce31d245-f222-4be1-806c-1ae244dac71a" />

The variance command allows EIGRP to install additional paths into the routing table as long as their metric is within the configured multiple of the best path

This lab shows how you can actually control path selection in EIGRP and allow multiple routes to be installed even when they aren't equal cost.

<img width="534" height="128" alt="image" src="https://github.com/user-attachments/assets/b0f81ca7-837f-449a-8ba3-60640ee6d389" />

Traffic is distributed proportionally across paths based on the metric.



<img width="1104" height="607" alt="image" src="https://github.com/user-attachments/assets/75c107ca-34c8-41cb-99b8-51251f38e0af" />



