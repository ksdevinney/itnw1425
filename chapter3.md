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

Port: number assigned to a process that can receive data; used to find a process running on a computer

Socket: host's IP:process's port

Socket opens when the host receives a request to communicate; socket closes when session is complete

Well-known ports: 0 through 1023 (for well-known utlities such as HTTP)
Registered ports: 1024 through 49151 (nonstandard assignments with increased security)
Dynamic and private ports: 49152 through 65535, dynamic: assigned as a need arises; private: assigned by a network administrator

TFTP: trivial file transfer protocol, used automatically by computers during boot up to request configuration files from another computer on the local network

NTP: network time protocol, synchronize clocks of computers on the same network

LDAP: lighweight directory access protocol, accessing network-based dictionaries

SMB: server message block, for sharing files on a network

SIP: session initiaon protocol, makes an initial connection between hosts but doesn't participate in data transfer

H.323: same as above, replaced by SIP

## Domain Names and DNS

Domain names: because it's easier than looking up a website by IP address

Common domains: com, edu, gov, net, org, mil, biz, info

FQDNs must be translated to an IP address to find the referenced computer

Name resolution: discovering the IP address using the FQDN

DNS: domain name system, associates computer names with IP addresses
Made up of namespaces (entire collection of computer names and associates IP addresses), name servers (computers that hold namespace databases), and resolvers (client that requests information from DNS servers)

DNS namespace databases are stored on servers around the world. DNS will not experience catastrophic failures if a few servers experience errors

DNS zone: domains an organization is responsible for managing

Authoritative server: authority on computer names and IP addresses

Name Servers
Primary DNS server: authoritative name server
Secondary DNS server: backup authoritative name server
Caching DNS server: accesses public DNS data and caches the DNS information it collects
Forwarding DNS server: receives DNS queries; provides the information if it already has it, forwards it to another server to resolve if not

Server types can conexist on the same machine

Recursive query: query that requires resolution (either the answer or "not found")
Iterative query: does not demand resolution, information only passed from servers if they have it

Information on DNS servers is kept in resource records:
Address: name-to-address mapping for IPv4
AAAAddress: name-to-address mapping for IPv6
CNAME: alternate names for a host
PTR: pointer, for reverse lookups (provides a host name from IP address)
NS: indicates the authoritative server for a domain
MX: for email servers and traffic
SRV: hostname and port of a computer that hosts a specific network (besides email)
TXT: holds text, SPF (identifies email servers allowed to send mail) and DKIM (verifies the domain of a email's sender) 

BIND (Berkeley Internet Name Domain) is the most popular DNS server software

Firewall: dedicated device or software that selectively filters or blocks traffic between networks
Area between two firewalls is a DMZ

## Troubleshooting

Start with Event Viewer

Command-line tools: 
ping verifies TCP/IP is installed, bound to the NIC, configured correctly, and communicating with the network
ipconfig: shows current TCP/IP addressing and domain name (ifconfig on Linux)
nslookup: query the DNS database and find the host name of a device using its IP address (dig for Linux and MacOS)

Common network issues:
Incorrect time: TNP time source is not reliable
DHCP issues: DHCP scope should be large enough to account for clients the network must support
Network Connection Configuration Issues: incorrect netmask, incorrect gateway, duplicate IP address, names not resolving