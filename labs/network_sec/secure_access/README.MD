


## Priv Exec mode
```bash
config t
enable secret Secret123
```
## Console Line
```bash
config t
  line console 0
  login
  password Console123

```
## virtual terminal lines using both Telnet and SSH
```bash
config t
  ip domain-name loonslocal.lab
  crypto key generate rsa
  ip ssh ver 2
  transport input all
```

## configuring login banners
```bash

```

## ACLs to limit who can connect
```bash

```



vty - virtual terminal
