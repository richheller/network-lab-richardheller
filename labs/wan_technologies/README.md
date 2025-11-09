


## static NAT

``` bash
config t
int e0/1
ip nat inside

int e0/3
ip nat outside

ip nat inside source static 10.10.2.20 198.51.100.2


show ip nat translations

```
<img width="813" height="84" alt="image" src="https://github.com/user-attachments/assets/2133214b-d02e-41c5-b5f2-2a78c95aafa2" />

## dynamic NAT


``` bash
show ip nat statistics

config t
int e0/0
ip nat inside
exit
access-list 10 permit 10.0.0.0 0.0.255.255
ip nat pool NAT_POOL 198.51.100.100 198.51.100.149 netmask 255.255.255.0
ip nat inside source list 10 NAT_POOL

show ip nat translations

clear ip nat translation *


```

<img width="1294" height="220" alt="image" src="https://github.com/user-attachments/assets/32087489-abee-4355-8dd4-9f637b11245e" />

<img width="1340" height="346" alt="image" src="https://github.com/user-attachments/assets/3419aaf8-02ba-412a-8b0d-49b41dc176ff" />

<img width="1184" height="722" alt="image" src="https://github.com/user-attachments/assets/89f997ec-664e-458e-81cf-b38d6a2f8e43" />


## NAT overload


``` bash
config t
ip nat inside source list 10 interface e0/3 overload

```
