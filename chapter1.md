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