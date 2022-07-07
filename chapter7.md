# Chapter 7: Virtualization and Cloud Computing

## Virtualization

Virtual (or logical) version of something, rather than the actual (physical) version- virtual machine installed on a computer, like for lab

Hypervisor: creates and manages a VM, manages resource allocation between host and VMs

Type 1 hypervisor: installed on computer before OS, creates partitions for multiple VMs
Type 2 hypervisor: installed on a host OS as an application (this type is used for labs)

VMs have vNICs that connect the VM to other machines
vNICs are customizable and each VM can have multiple vNICs

Hypervisor automatically creates a vSwitch (or bridge) between the VM and the host

Bridged mode: vNIC accesses a physical network using the host's NIC; still obtains its own IP address, default gateway, and subnet mask; appears as a regular node on the network

NAT mode: host machine acts as a NAT device; other devices communicate with the host's IP address, VM is invisible to the network

Host-only mode: VM can exchange data with host and other VMs on the host, but not with any nodes beyond the host

Virtualization advantages:
* uses resources efficiently; one computer can run multiple 
* cost savings: fewer physical machines are needed
* isolation: issues with one instance of a virtual machine does not affect the others
* simple to backup, backup images can be used to easily recreate that machine

Disadvantages:
* may rob resources from other VMs or the host
* more complex: must understand the software, addressing and switching
* each VM using commerical software requires its own license
* VMs fail if host fails

Network devices can also be virtualized, such as firewall and router
Virtual firewall emulates a hardware firewall

NFV: Network Functions Virtualization, merging physical and virtual network pieces

SDN: Software Defined Networking, uses an SDN controller to handle decision-making responsibility
SDN can temporarily assign more bandwidth to an app that needs it

## Cloud Computing

Different types of cloud computing models, determined by how much of its network an organization is responsible for

* Traditional: everything is managed at your location (using MS Office on your own computer)
* Infrastructure as a Service: hardware services are provided virtually, infrastructure is managed by vendor but apps, data management, and backups are managed by user (AWS)
* Platform as a Service: provides platform services (OS), users are responsible for software installation and data management (Google Cloud)
* Software as a Service: applications provided through a user interface, compatible with many devices and OSes (Google drive, online mail)
* Anything as a Service: cloud provides functions depending on the user's needs

Cloud services use different deployment models:
* Public cloud: provided over public transmission lines (internet)
* Private cloud: service on an organization's own servers, or established for a single organization's private use over a WAN
* Community cloud: shared between multiple organizations, not available publicly 
* Hybrid cloud: combination of other service models

Cloud usage depends on network connection, connection to the ISP and other third parties
Using internet connections can also mean security concerns

## Encryption Protocols

States of data:
* at rest (most secure, on a device protected by multiple types of security)
* in use (able to be accessed)
* in motion (possibly leaving secured network, vulnerable to security gaps)

Encryption: using a cipher to keep data unreadable

Key encryption: most popular, uses a key (random string) to scramble the data

Private key: key used is only known by the sender and receiver of data, key must be shared between the two (symmetric because the same key is used on both ends)
Public key: data encrypted with a private key known only to the user, decrypted with with a related public key (available through third party, asymmetric)

IPsec: protocol that defines rules for encryption, authentication, and key management

1. IPsec initiation
2. key managment
3. security negotiations
4. data transfer
5. termination

SSL and TLS are methods of encrypting TCP/IP transmissions
Supported by all modern browsers for HTTP security

TSL: transport layer, updated version of SSL

HTTP uses port 80, HTTPS uses encryption and port 443

## Remote Access

Allows user to connect with a server, LAN, or WAN in a different geographical area

Require a Remote Access Server 

Point-to-Point Protocol directly connects two WAN endlpoints

Terminal Emulation: allows one user (client) to control another (host or server) across a network
Host may allow privileges from viewing the screen, to receiving keystrokes

Telnet: allows a user to control a host remotely, little security
SSH: protocols that do authentication and encryption, allows you to log on to a host and execute commands; SSH needs to be running on both computers
RDP and VNC: 
...
Out-of-Band Management: relies on dedicated connection 
Remote File Access (FTP): allows file transfer between client and host

VPN: network encrypted from end-to-end that creates a private connection to a remote network
Can be used instead of leasing PPP connections 
Tunnel