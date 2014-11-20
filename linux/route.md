# route command
## Route to another network. 
I use this when I have to route from my office network to a network of VM that I setup as a test environment. 

Assuming that I am on network 2.3.4.x but I need to connect into network 1.2.3.0/24. In the network is a gateway to interface 2.3.4.5. So I just do the following
```

sudo route add 1.2.3.0 netmask 255.255.255.0 gw 2.3.4.5

```