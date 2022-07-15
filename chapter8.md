# Chapter 8: Subnets and VLANs

## Network Segmentation

Separating traffic on one network into its own broadcast domain

* enahnces security
* improves performance
* simplifies troubleshooting

Networks are often segmented by geographic location, departmental boundaries, and device types

## Subnets

One way to segment a network is to add a router at certain points (ie one on each floor)

Subnetting: dividing pool of IP addresses into groups for each LAN

Subnet mask: used to determine what subnet a device belongs to
Always 1s and 0s, 1s mark the network portion of the IP address, 0s mark the host portion

CIDR: identifies network and host bits in an IP; uses IP address followed by / and a number representing the number of bits in the network ID

Subnetting is "classless addressing", borrowed bits from IP address represent network information

Administrator programs each interface on the router with the network ID and subnet mask for its subnet

Variable Length Subnet Masking allows subnets to be divided into smaller groups until each subnet is the same size as the necessary IP address space
Create the largest subnet first, then next largest, and so on
Not a good idea to use 100% of network space, need to allow room for growth

IPv6 subnetting: does not use classes, does not use subnet masks, one subnet is capable of supplying many IPv6 addresses

## VLANs

Can use managed switches and VLANs to segment a network (instead of using routers)

