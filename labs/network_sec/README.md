


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

### Configuring Extended IPv4 ACLs

``` bash
access-list 101 deny tcp 172.16.3.0 0.0.0.255 any eq 22


ip access-list extended EXT-ACL
  10 permit 172.16.7.0 0.0.0.255 any
  20 permit 172.16.20.0 0.0.0.255 host 172.16.16.133

  int FastEthernet 0/1
  ip access-group EXT-ACL in

```
