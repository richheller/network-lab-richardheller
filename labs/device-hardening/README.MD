# Device Hardening

## Securing Unused Ports
``` bash
int range GigabitEthernet0/1-2
  shutdown
  exit

##moving unused ports to dedicated vlan
int range GigabitEthernet0/1-2
  switchport mode access 
  switchport access vlan 999
  shutdown
  exit
vlan 999
  name Parking_vlan
  shutdown
  exit

```

## Infrastructure ACL - iACLs
``` bash

```

## Disabling Unused Services
``` bash

```

## Port Security
``` bash

```

## Implementing DHCP snooping
``` bash

```

