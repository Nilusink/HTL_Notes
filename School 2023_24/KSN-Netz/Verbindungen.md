---
title: Verbindungen
updated: 2023-10-10 08:00:11Z
created: 2023-10-10 07:13:42Z
latitude: 47.26921240
longitude: 11.40410240
altitude: 0.0000
---

## Verbindungen
|Netz|Port|Router-IP|
|-|-|-|
|10.x|GE 0/0|10.10.10.254|
|11.x|GE 0/1|10.10.11.253|
|12.x|FE 0/0|10.10.12.253|
|2.x|FE 0/1|10.10.2.254|

Konfiguration GE
```Perl
enable
    conf t
        interface ge 0/x
            ip address 10.10.n.x
            no shut
```

Konfiguration FE
```Perl
enable
    conf t
        interface fa 0/0/x
            switchport mode access
            switchport access vlan n

        interface vlan n
            ip address 10.10.n.x
```

Router-RIP
```Perl
enable
    conf t
        router rip
            version 2
            no auto-summary
            
            network 10.10.n.0
            ...
            
            passive-interface fa 0/1
```

DHCP für 10.10.2.0:
```Perl
enable
    conf t
        ip dhcp pool "2"
            network 10.10.2.0 255.255.255.0
            default-router 10.10.2.254
            dns-server 1.1.1.1
```
