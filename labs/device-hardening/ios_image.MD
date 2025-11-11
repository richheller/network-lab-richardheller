
###  Cisco ios Image

``` bash
sh running-config

sh startup-config

```

### validating Cisco ios Image

``` bash

verify /md5 flash:/ image_name .bin


```


#### merge configuration from RAM with a saved config file on TFTP server 

``` bash
copy tftp running-config
```
