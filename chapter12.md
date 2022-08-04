# Chapter 12: Wide Area Networks

## WAN Essentials

WAN travels a significant distance, connects LANs

WANs:
* use networking devices to connect networks over a wide geographical area
* usually owned by service providers

WAN sites: geographic endpoints connected by a WAN
DTE: customer's endpoint device on a WAN
DCE: carrier's endpoint device
DTE communicates on the LAN, DCE communicates on the WAN

Types of WAN links:
* dedicated line: continuously available communication path not available to others
* virtual circuit: appears to be a dedicated line, but can be any configuration

Switching: how connections are created between nodes on a network
* circuit switched: connection is established before nodes begin transmitting data
* packet switched: data is broken into packets, packets travel any path to destination, reassembled by node

packet-switched is more common

CPE: equipment located on customer premises

## Layer 1 WAN technologies

broadband: cables and bandwidth are shared between multiple customers, asymetrical/asynchronous (download faster than upload)

DIA: cable and portions of bandwidth are dedicated to a single customer, symmetrical and synchronous

PSTN: public switched telephone network, circuit-switching network that also provides landline telephone service
local loop: portion of PSTN that connects residences/business to nearest central office, most likely to use copper wire and carry analog signals
Formerly used dial-up and ISDN

DSL: digital subscriber line 
"always up" - does not require dialing in
* asymmetric DSL: faster download than upload, most common type
*VDSL: faster, still asymmetric
*SDSL: download and upload are equal

Cable broadband: based on coaxial cable wiring for TVs
Requires a cable modem
Many subscribers share the same local line

Metro Ethernet
??

T-Carriers: provides a dedicated logical circuit only used by the customer
T1: 
T3: 28x more throughput than T1
Required equipment: smart jack,CSU/DSU, multiplexer

SONET: synchronous optical network
fast data transfer, integrates other WAN technologies, simple link additions/removals, high degree of fault tolerance
traverses multiple ISP networks
frames sent out on a regular schedule, regardless of whether or not they contain data
expensive

## Layer 2 WAN Technologies

Frame relay: data is separated into frames and relayed from one node to another

ATM: asynchronous transfer mode
Node can transmit at any instant, destination node must accept the transmission as it comes
Message is called a "cell" and is always 48 bytes of data + 5 byte header
Can guarantee a specific QoS
Relatively expensive, being overtaken by metro ethernet

MPLS: multi-protocol label switching
Uses packet-switched technologies over circuit-switched

## Wireless WANs

Cellular: originally designed for analog phone service
* 1G: analog
* 2G: digital, allowed for texting, speed limited to 240 Kbps
* 3G: used packet switching for data, 385 Kbps
* 4G: packet switching for data and voice
* 5G: doesn't exist yet
GSM: uses TDMA (similar to TDM but comes from different sources)
CDMA: signal over a wider bandwidth

Satellite: information transmitted to an uplink transmitter to an orbiting satellite
Transponder receives the uplink, transmits to Earth-based downlink receiver
Downlink received on Earth by dish-shaped antenna
Signals can be exchanged with satellites as long as there is an unobstructed view of the sky