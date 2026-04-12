

<h1>EIGRP - Unequal Cost Load Balancing</h1>

Overview

EIGRP is an advanced distance vector routing protocol, originally Cisco proprietary. For this lab I created in scratch in CML on a dedicated server I host.



This lab demonstrates EIGRP unequal-cost load balancing using the variance command. Interface delay was manipulated to influence path metrics and create multiple feasible successors.
<img width="1904" height="628" alt="image" src="https://github.com/user-attachments/assets/fece605a-3c1a-4db3-b851-1f727388f8fd" />


<img width="1040" height="671" alt="image" src="https://github.com/user-attachments/assets/63af0928-7803-4511-9e6b-c3f13014a608" />


My path to R1 network at 10.0.12.0/30 has <b>1 successor and 2 feasible successors</b> as both alternative paths satisfy the feasibility condition <b>RD < FD</b>.

<img width="478" height="89" alt="image" src="https://github.com/user-attachments/assets/56dcabce-51f5-4398-929f-99850fd5865a" />


The highest metric path (28416) requires a minimum variance of approximately 6.16 (28416 / 4608). Since variance must be an integer, a value of 7 is required to include the third path.


