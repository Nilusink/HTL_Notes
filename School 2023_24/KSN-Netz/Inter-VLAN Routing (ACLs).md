---
title: Inter-VLAN Routing (ACLs)
updated: 2023-11-10 13:07:42Z
created: 2023-10-20 09:50:44Z
latitude: 47.26921240
longitude: 11.40410240
altitude: 0.0000
---

<style>
	body {
		font-size: 1.65vw;
		background: white;
		color: black;
	}
	date {
		color: gray;
		font-size: 1.3vw;
	}
	h1 {
		margin-top: 10vw;
		font-size: 5vw;
	}
	h2 {
		margin-top: 8vw;
		font-size: 4vw;
	}
	h3 {
		margin-top: 6.6vw;
	 	font-size: 3.3vw;
	}
	h4 {
		margin-top: 5vw;
		font-size: 2.5vw;
	}
	.merke {
		background-color: rgba(150, 0, 0, 100);
		border-radius: 2.2vw;
		border: .4vw solid red;
		padding: 2.2vw;
		margin: 1.1vw;
		color: white;
	}
	.infobox {
		background-color: rgba(20, 100, 150, 100);
		border-radius: 2.2vw;
		padding: 2.2vw;
		margin: 1.1vw;
		color: white;
		
		transition: all .3s cubic-bezier(0, 1.3, .8, 1.3);
		
		user-select: none;
	}
	.infobox:hover {
		background-color: rgba(30, 120, 180, 100);
	}
	.infobox:active {
		transform: scale(1.1, 1.1);
	}
	re {
		color: red;
	}
	or {
		color: orange;
	}
	strong {
		color: #05f01c;
	}
	.wimage {
		justify-content: center;
		background: white;
		align-items: center;
		padding: 1.1vw;

		display: flex;
	}
	.wimagetext {
		flex: 3;
		margin-left: 2.2vw;
		color: black;
	}
	.wimagetext:hover {
		flex: 5;
	}
	.wimageimage {
		flex: 2;
	}
	.wimageimage:hover {
		flex: 3;
	}
	tr {
		background: #333;
	}
</style>
#### standard
```Perl
enable
    conf t
      access-list <standard (1-99)|extended  (100-199)> <deny|permit|remark> <ip|any|host>
      access-list 1 deny 192.168.10.0 0.0.0.255
      
      interface gigabitEthernet 0/0/0.10
          ip access-group 1 in
```

### extended
```Perl
enable
    conf t
        access-list 100 <deny|permit|remark> <udp|tcp> <ip|any|host> <mask> <criteria> \
            <protocol|port> <ip|any|host>
        access-list 100 deny tcp 192.168.10.0 0.0.0.255 eq 80
        access-list 100 permit ip any any
        
        interface gigabitEthernet 0/0/0.10
            i paccess-group 1 in
```
