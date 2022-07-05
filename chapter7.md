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