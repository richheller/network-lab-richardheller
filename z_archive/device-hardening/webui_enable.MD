

### webui enable

``` bash


config t
username admin privilege 15 secret cisco123
ip http server
ip http secure-server
ip http authentication local

```

<img src="https://github.com/richheller/network-lab-richardheller/blob/main/labs/device-hardening/webgui.png">
<i>Cisco Catalyst 2960 WebUI (http dashboard - sensitive identifiers redacted)</i>
