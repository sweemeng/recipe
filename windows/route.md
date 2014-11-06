# window route command
## Print routing table on window

This is to print routing tables on windows. I used powershell here, it is optional. 

Requirement
* Windows

snippet
```

PS C:\Windows\system32> route print

```

## Add routing table on windows

This is to add an entry to windows routing table, and make it permanent even if restart. 
Very useful if you want to have certain traffic go into VPN, and the rest go other the normal connection

Requirement
* Windows
* Admin access

snippet
```

PS C:\Windows\system32> route add -p 1.2.3.0 mask 255.255.255.0 1.2.3.1

```

NOTE: 1.2.3.0 the network you want to route, 1.2.3.1 is the gateway of the vpn, you can find it on using `route print`