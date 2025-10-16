


## ACLs

### Configuring Standard IPv4 ACLs

``` bash
ip access-list standard STD-ACL
  permit host 172.16.1.10
  deny 172.16.1.0 0.0.0.255
  deny host 10.3.3.30
  permit 10.3.3.30 0.0.0.127
  int FastEthernet0/2
ip access-group STD-ACL out
```
