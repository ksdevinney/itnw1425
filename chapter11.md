# Chapter 11: Network Performance and Recovery

Network Management: assessment, monitoring, maintenance of all aspects of a network

## Monitoring tools

Network monitor: continually monitors network traffic
Protocol analyzer: monitors traffic at a specific interface between a server or client and the network

Wireless monitoring: run monitoring software on a computer connected wirelessly to a network; must support "promiscuous mode" for computer to see all traffic

Port mirroring: traffic sent to a port is also sent to a mirrored port, running monitoring software

In-line monitoring: test access point

All network monitoring tools can:
* set NIC to run in promiscuous mode
* monitor network traffic on a segment
* capture network data
* capture frames sent to or from a specific node
* reproduce network conditions
* generate statistics about network activity

Traffic analysis: examines the flow of nextwork traffic for patterns and exceptions

Packet analysis: identifies protocols, errors, and misconfigurations
**list of complications: runts, giants, jabber, ghosts, packet loss, discarded packets, interface resets**

Conditions recognzed by an OS can be recorded; records are kept in a log; network admin can define conditions for new entries

NMS server- collects data from multiple managed devices (polling)
Managed device: network node monitored by the NMS (may contain managed objects, assigned an OID)
Network management agent: runs on each managed device
MIB: list of objects managed by the NMS

Most agents use SNMP, 3 versions exist (v3 is the most secure, v2 still common)
Messages should be configured to give *useful* data; too much data can be unhelpful

Baseline: report of the network's normal state of operation
Obtained by analyzing network traffic information
Allows you to compare future performance increases or decreases caused by network changes
Baseline performance metrics: utilization, error rate, packet drops, jitter

## Managing Network Traffic

Traffic shaping: manipulating certain characteristics of packets, data, or connections to manage the type and amount of traffic on a network
* delaying less important traffic
* prioritizing more important traffic
* limitng volume of traffic
* limiting throughput rate for an interface

Traffic policing: last two from the list
Many ISPs use traffic throttling to slow down high-bandwidth users


Delay sensitive vs loss tolerant ? 

Quality of service: adjusting priority to various types of transmissions
DiffServ: prioritizes layer 3 traffic
CoS: layer 2

## Network Availability

availability: how consistently a connection can be accessed; expressed as a percentage
High Availability- functions reliably nearly all the time
Can be measured by uptime (duration of time between failures)

Fault tolerance: capacity to continue performing despite hardware or software problems
Best to provide multiple paths that data can travel

Failure: deviation from a specified level of system performance for a given period of time
Fault: malfunction of one component of a system; can result in a failure

Redundancy: networks designed with two or more of the same item, service, or connection filling the same role on the network; intended to eliminate single points of failure
Automatic failover: one component can automatically resume the duties of an identical component

Redundant links: redundant connections between devices
Link aggregation: seamless combination of network interfaces to act as one logical interface

LACP
CARP: allows a pool of computers to share IP addresses

Backup: copy of data or files created for archiving or safekeeping
Full: backs up everything every time
Incremental: backs up only changed data since last backup
Differential: dad that has changed since last full backup

Snapshot: frequently saved incremental backup

NAS: specialized storage that provides fault-tolerant data storage for a network
RAID

SAN: network of storage devices that communicate with each other and other networks
multiple storage devices are connected to multiple servers; fault tolerant and fast

Power flaws:
* surge (momentary voltage increase)
* noise (fluctuation in voltage caused by other devices)
* brownout (momentary voltage decrease)
* blackout (complete power loss)

Uninterruptable Power Supply: battery operated power source directly attached to devices, prevents undesired fluctuations

Generator: backup power source

## Response and Recovery

incident: any event that has adverse effects on a network's resources
disaster: extreme incident

Incident response policy: defines characteristics of an event that qualifies as an incident and steps that should be followed

Disaster recovery: process of restoring critical functionality and data
Purpose is to ensure business continuity

cold site: tools necessary to rebuild a network, but not ready for immediate use
Warm site: tools necessary to rebuild a network, some pieces are ready to use
hot site: tools are all correctly configured, updated, and connected to match the network's current state