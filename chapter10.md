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
Might be placed between two interconnected networks, or on the edge of a private network
Simplest: packet-filtering, only examine network address

Intrusion Detection System stand-alone device (or application or feature) running on a workstation, server, switch, router, or firewall; monitors network traffic and sends alerts about suspicious activity

Intrusion Prevention System: can prevent traffic from reaching the network or host

Security Information and Event Management: system to evaluate data generated from IDS, IPS, and firewalls

## Switch Management

Spanning Tree Protocol
* prevents traffic loops
* responds to changes in the network
* RSTP can detect a link failing in miliseconds
* SPB keeps potential paths open while managing the flow of data across those paths to prevent loops

Bridge Protocol Data units: transmits STP information between switches

Unused ports should be disabled until needed

## Authentication, Authorization, and Accounting

Controlling access to a network and its resources

Authentication: verifying a user's credentials

Local authentication: authentication processes (usernames and passwords) are stored locally
Low security
Can be more convenient for smaller networks
only option if network is down

Network authentication
* can set valid hours for activity
* can restrict total time logged on
* specify which workstations accounts can log in from
* limit how many log in attempts are allowed
* set a geographical location allowed to access

One type of DoS attack can flood the network with authentication requests that have to be responded to

Authorization: determining what the user can and cannot do
Right to install, execute, or uninstall software AND
Permission to read, modify, create, or delete files and folders

Role-based access control: privileges and permissions are assigned based on need for a user to complete certain tasks
Network admin creates user groups based on roles and assigns permissions to the group
Role separation: if user is part of more than one group, user is locked down completely

Accounting: logging access and activity

Many systems generate txt logs; files are long but can be viewed with a file viewer

Network Access Control: network policies to determine the level and type of access to each device that joins a network
An *agent* may need to be installed on a device before it can be authenticated
Nonpersistent agent: uninstalls after authentication is completed
Persistent agent: permanently installed, may provide additional security measures

## Access Control Technologies

Authentication services and protocols

Active directory: account information maintained on a server
LDAP compliant

Outdated authentication protocols: Password Authentication Protocol (sends without encryption), Challenge Handshake Authentication Protocol, MS-CHAP, MS CHAP v2

Kerberos: default authentication protocol on the active directory; uses key encryption to verify identity and securely exchange information
* Authentication service: lets clients in
* ticket granting service: issues "tickets" for authenticated clients to access services on the network

Single sign-on: client signs on one time to access multiple systems or resources
May require an additional verification for added security (ex 2FA)
MFA: requires information from two or more categories

RADIUS: remote authentication dial-in user service, authentication and authorization are the same process
only encrypts the password in transmissions

TACACS+: offers the option of separating authentication, authorization, and audtiting capabilities
relies on TCP at the transport layer
installed on a router or a switch
encrypts all information for AAA

## Wireless Network Security

WEP used OSA (no authentication key) or SKA (shared key for all clients)

802.11i = improvement

WPA incorportated TKIP
* message integrity/packet authentication
* key distribution
* encryption

WPA2
* message integrity
* encryption: uses AES, faster and more secure than TKIP

WPA has personal and enterprise versions

Personal: pre-shared key; enter a passcode for your device to enter the network
Enterprise: additional security measures, RADIUS + EAP

EAP...