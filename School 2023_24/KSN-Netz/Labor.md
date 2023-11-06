---
title: Labor
updated: 2023-09-27 09:36:45Z
created: 2023-09-19 09:27:38Z
latitude: 47.26921240
longitude: 11.40410240
altitude: 0.0000
---

```Perl
enable
	conf t
		hostname Seppl
		enable password P@ssw0r1
		service password-encryption
		banner motd "You are now on switch Seppl"  # set login-message (Message Of The Day)

		# telnet configuration
		line vty 0 15
			password P@ssw0r1
			login
			exit

		# VLAN configuration
		interface range GigabitEthernet 0/1-9
			switchport mode access
			switchport access vlan 10
			exit

		interface vlan 20
			ip address 192.168.1.254 255.255.255.0
			no shut
			exit

		interface range GigabitEhternet 0/10-19
			switchport mode access
			switchport access vlan 20
			exit


```

