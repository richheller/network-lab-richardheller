
### NTP configuration

``` bash

config t
int loopback 10
ip add 10.10.4.1 255.255.255.0
exit
ntp master 3
ntp source loopback 10
```
