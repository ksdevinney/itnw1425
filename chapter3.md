# Addressing on Networks

Data Link Layer: MAC address- 48 bits, 6 hex numbers separated by colons; unique to the NIC

Network Layer: IP address, assigned to every interface (network connection made by a node), can be used to find a computer
IPv4: 32 bits, 4 decimal numbers (octets- in binary consists of 8 bits)
IPv6: 128 bits, 8 blocks of hex numbers separated by colons

Transport layer: port number is used to find an application

Application layer: FQDNs (fully qualified domain names), computer names, host names; every host on a network is assigned a unique name
ftp.company.com.
ftp: host name
company.com: domain name

## MAC Addresses

Communication inside a network

MAC addresses are stamped or labeled on the NIC 

First 24 bits (6 hex characters) are the manufacturer's OUI (organizationally unique identifier)- can identify the NIC's maker based on the MAC address

Remaining 24 bits identify the device (device ID), based on model and manufacture dates; no two devices should have the same MAC address

## IP Addresses

required to communicate outside a local network (through a router)

Can be static or dynamic

### IPv4

4 groups of 8 bits each, separated by decimal; can be any number from 0 to 255

Classful addressing: manages network vs. host portions determined by numerical range of the IP

Class A: 1.x.y.z to 126.x.y.z
Class B: 128.0.x.y to 191.255.x.y
Class C: 192.0.0.x to 223.255.255.x

Class A, B, and C are public IP addresses

Private IP addresses can be used on networks that don't connect directly to the internet
10.0.0.0 through 10.255.255.255
172.16.0.0 through 172.31.255.255
192.168.0.0 through 192.168.255.255

Class D and E are not available for public use
Class D begins with octets 224 through 239, used for multicast transmissions

Reserved:
255.255.255.255
0.0.0.0
127.0.0.1 through 127.255.255.254 research or loopback address
169.254.0.1 through 169.254.255.254 used to create APIPA

Static IP addresses are assigned by a network adminstrator, dynamic IP addresses automatically assigned by DHCP server each time the device connects to the network

Address translation: gateway device will substitute a device's IP address for its own; requires only one public IP address for many devices and provides more security

Port Address Translation assigns a separate port to each session between a local host and internet host

SNAT: static network address translation, assigns the same public IP to a host each time it makes a request to access the internet, for small home networks with only one public IP; changes the IP address of the source of outgoing messages

DNAT: destination NAT, hosts outside the network address a computer inside the network using a single IP address; changes the destination IP address of incoming messages

### IPv6

Established to allow more public IP addresses on the internet and improve routing capabilities and transmission speeds

128 bits over 8 blocks, each block is 16 bits; leading zeroes (0064) don't need to be written; blocks of all zeroes (0000) can be eliminated and replaced with double colons, but only one set of double colons can be used per address

link: LAN bounded by routers
Interface: node's attachment to link
dual stacked: network configured to IPv4 and IPv6
tunneling: transporting IPv6 packets through or over IPv4
Interface ID: Last 64 bits/4 blocks of IPv6
Neighbors: nodes on the same link

Unicast address: single node on the network
Global address: can be routed on the internet
Link Local address: can be used for communicating with nodes in the same link

Multicast address: delivers packets to all nodes in the multicast group

Anycast address: identifies multiple destinations, packets delivered to the closest destination

Unlike IPv4, IPv6 eliminates broadcasting

With IPv6, computer can autoconfigure its own link local IP address without a DHCPv6 server

## Ports and Sockets