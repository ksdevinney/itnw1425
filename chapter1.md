# Introduction to Networking

Network: group of devices connected by some type of transmission media

## 1.1 Network Models

Topology- how parts work together; physical (hardware) vs logical (software)

Network operating systems: control access to the entire network

**Peer-to-peer**: OS of each device on the network is responsible for controlling access to its resources without centralized control. Computers (nodes) control their own administration, resources, and security
* simpler
* Less expensive to set up and maintain
* not scalable
* not as secure
* not practical for more than a few computers

**Client-server**: resources managed by the NOS through a central directory database
Domain: server controls network access to a group of computers
Client: computer making a request
The NOS:
* Manages data for clients
* Ensures only authorized users access the network
* Controls which files a user can open and read
* Restricting where/when users can access the network
* Dictating rules computers use to communicate
* Supplying applications and files to clients

Servers using a NOS require more memory, processing power, and storage capacity

Advantages over peer-to-peer:
* User accounts are assigned in one place
* Access to shared resources can be centrally granted
* Network problems can be diagnosed from one location
* More scalable

## 1.2 Client-Server Applications

Network services: resources a network makes available to its users, applications and data

Protocols: methods and rules for communication used by networked devices
TCP (transmission control protocol) and IP (internet protocol)

Web service: serves web pages to clients, primarily uses HTTP (hypertext transfer protocol). HTTP + SSL (Secure sockets layer) or HTTP + TLS (transport layer security) = HTTPS (HTTP secure)

Email services: client uses SMTP (simple mail transfer protocol) to send a mail message to the first server; first server send the message on to the recipient's email server; recipient's mail server delivers using POP3 (post office protocol 3 - email downloaded to the client's computer) or IMAP4 (internet message access protocol 4- client application manages the email while it's stored on the server)

FTP services: transers files between two computers (file transer protocol), not secure. Web browsers can be FTP clients

Telnet service: allows an administrator to control another computer remotely; not secure

Remote application: installed and executed on a server and presented to a user on a client computer. Remote Desktop Services manage remote applications. Client computers require less computing power and less support as a result

Remote Desktop: RDP (Remote Desktop Protocol) allows a technician to remote in, encrypted and secure 

## 1.3 Network Hardware

### LANs

LAN (local area network) each node on a network can communicate with others directly through the network

Connected by a switch (receives data through one port and redirects data out through another port), previously hubs were used

Star topology: all devices connect to one central device (the switch)

Devices have network ports for network cables, can be embedded in the motherboard or provided by a NIC (network interface card) and installed in an expansion slot

LAN can have several switches connected to each other to form a backbone (central conduit that connects pieces of a network)

Bus topology: when switches are daisy-chained together in a single line; if each switch is connected to computers it is still a star topology

Hybrid topology: combines topologies, such as a star-bus

Ring topology (outdated): nodes are connected in a ring, one node is only connected to its two neighboring nodes. Slower.

Router allows LANs to communicate with other networks, manages traffic between two or more networks
Home networks may use a combo device (both a router and a switch and possibly a Wifi hot spot)

Switch belongs only to a local network, routers belong to two or more networks; host on one LAN cannot communicate with a host of another without a router 

Host: computer on a network that hosts a resource (application or data); node: any device on a network that can be addressed by the local network

### MANs and WANs

WANs: Wide Area Network, LANs spread out over a wide geographical area
MANs: Metropolitan Area Network, connected LANs in the same geographical area 

The internet is the largest WAN; PAN (personal are network) is the smallest network, personal devices connected together

## 1.4 Seven-layer OSI model

OSI: open systems interconnection

Physical layer, data link layer, network layer, transport layer, session layer, presentation layer, application layer

- 7 **Application layer** is the interface between two applications on separate computers
* Application programs that provide services to a user (like a web browser)
* Utility programs that provide services to the system (SNMP- simple network management protocol), programs that monitor network traffic

*payload* is data passed between applications

- 6 **Presentation layer** reformats, compresses, and encrypts data for the receiving application

- 5 **Session layer** describes how data is synced and recovered between sessions

Each of these layers can be performed by the application or the OS

*** 

- 4**Transport layer** transports application layer payloads from one application to another
TCP: transmission control protocol; makes a conncection with the end host, checks if data is received, resends if not; connection-oriented protocol
UDP: user datagram protocol; does not guarantee delivery of data; used for streaming where speed is important
Both of these add an information control *header* to the message

- 3 **Network layer** moves messages from one node to another until they reach the destination
Uses IP, which adds its own header to the segment to create a **packet**

- 2 **Data link layer** is the type of hardware or technology used on a network (ethernet or WiFi)
This layer puts its own control information in a header and also includes a trailer to the end of a packet; the entire message is called a *frame*
Frame header includes MAC (media access control) address or physical address

- 1 **Physical layer** responsible only for sending bits along a wired or wireless transmission

Names of a message change as it moves from one layer to another:
Bit, L1PDU (1); Frame, L2PDU (2); Packet, L3PDU (3); Segment (TCP) or Datagram (UDP), L4DPU (4); payload or data, L7DPU (5-7)

## 1.5 Safety Procedures and Policies

Fail open: access allowed during failure (building's doors unlocking automatically during a fire)
Fail close: access denied during failure (data locked until software comes back online)

Sensitive electronic devices can be harmed by static electricity (ESD)

Catastrophic failure: damaged beyond use
Upset failure: shortens life of component, causes errors

## 1.6 Troubleshooting Network Problems

- 1: Identify the problem and its symptoms

- 2: Establish a theory of probable cause (start with the bottom of the OSI model)

- 3: Test your theory to determine the cause (try least invasive/least expensive methods first)

- 4: Establish a plan for solving the problem (make your changes when the least number of users are on the network)

- 5: Implement the solution or escalate the problem

- 6: Verify functionality and implement preventative measures

- 7: Document findings, actions, and outcomes