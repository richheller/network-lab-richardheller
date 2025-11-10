
### NTP configuration

``` bash
###on router

config t
int loopback 10
ip add 10.10.4.1 255.255.255.0
exit
ntp master 3
ntp source loopback 10

###on switch

config t
ntp server 10.10.4.1



###to check

sh ntp associations

sh ntp status

```
