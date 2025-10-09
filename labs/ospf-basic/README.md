
# OSPF Basic Lab

## Objective
Specify OSPF interface cost parameter to 1

## Configuration

```text
config t
int e0/0
ip ospf cost 1
```

```
router ospf 1
router-id 1.1.1.1
network 10.0.1.0 0.0.0.255
do sh ip ospf
do sh ip ospf int brief

sh ip route
sh ip route ospf
```
