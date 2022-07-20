# Chapter 10: Security in Network Design

## Network Security Devices

Proxy server: intermediary between internal and external networks, scans incoming and outgoing data
Application layer, provide relatively low-grade security
Can provide some filtering, improve performance by caching files

Access Control List: list on router to determine if a packet should not be forwarded
Uses "permit" and "deny" flags; packets that match the permit statements are passed to the network, packets that match the deny statement are discarded
If a packet doesn't match either, it is moved to the next statement; if it reaches the end without a match to either, it is dropped
Implict deny rule: any traffic ACL does not explicitly permit is banned by default
access-list command can assign a statement to an ACL
Not automatically installed

Firewall: device or software that selectively filters or blocks traffic between networks