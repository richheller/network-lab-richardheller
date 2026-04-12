

<h1>EIGRP - Unequal Cost Load Balancing</h1>

Overview

EIGRP is an advanced distance vector routing protocol, originally Cisco proprietary. For this lab I created in scratch in CML on a dedicated server I host.



This lab demonstrates EIGRP unequal-cost load balancing using the variance command. Interface delay was manipulated to influence path metrics and create multiple feasible successors.

<img width="1535" height="550" alt="image" src="https://github.com/user-attachments/assets/2570533e-71a6-4b02-973a-29b0787011ee" />


<img width="1040" height="671" alt="image" src="https://github.com/user-attachments/assets/63af0928-7803-4511-9e6b-c3f13014a608" />

My path to R1 network at 10.0.12.0/30 has three feasible successors since the RD < FD.

![Uploading image.png…]()

<img width="478" height="89" alt="image" src="https://github.com/user-attachments/assets/56dcabce-51f5-4398-929f-99850fd5865a" />
