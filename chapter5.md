# Chapter 5: Network Cabling

## Transmission Basics

Bandwidth: the amount of data that could theoretically be transmitted during a given period of time (limit never happens in practice)

Throughput: measure of how much data is actually transmitted in a given period of time

Bit rate: bits transmitted per second

Actual throughput is usually lower than rated bandwidth

b: bits (data transmission)
B: bytes (data storage)

### Transmission Flaws

Noise: can degrade or distort a signal
* EMI (electromagnetic interference): caused by other electronic devices, including TV and radio (radio waves cause RFI)
* crosstalk: signal travelling on one wire interferes with signal travelling over adjacent wire
* alien crosstalk: between two cables
* NEXT: occurs between wire pairs near signal source
* FEXT: at the far end of the cable from signal source

Attenuation: loss of signal strength as it travels away from the source; signals are boosted along the way with a repeater

Latency: delay between data leaving the source and arriving at its destination; affected by length of cable and intervening connectivity device; measured by packet's Round Trip Time
Jitter (or PDV): packets arriving out of order due to a delay

Two important NIC settings: the direction signals travel over media and number of signals that can traverse media at any given time

* Duplex: signals can travel both directions simultaneously (default for modern NICs)
* Half-duplex: signals may travel both directions, but only one direction at a time (like an intercom system)
* Simplex: signals may only travel one way (like a radio)

Multiplexing: allowing multiple signals to travel simultaneously over one medium
Medium's channels are separated into subchannels
* TDM: divides a channel into multiple intervals of time, time slots are reserved for their nodes regardless of whether they have data to send
* STDM: assigns time slots to nodes, but adjusts time depending on priority and need; maximizes available bandwidth
* FDM: assigns different frequencies to each subchannels so multiple signals can transmit on the same line at the same time

Multiplexing with fiber optic cables:
* WDM: divides a light beam into different wavelengths on a single fiber
* DWDM: increases the number of channels provided by WDM
* CWDM: spaces frequency bands farther apart to allow for cheaper transceiver equipment

## Copper Cable

Coaxial cable: outdated, but still used for cable internet/TV
Made of a central metal core, insulator, braided metal shield, and outer cover
RG-59 (for relatively short connections) and RG-6 (cable internet) cables still used today
Can end in:
* F-connectors: pin in the center is the conducting core
* BNC connector: lock and turn connecting mechanism, provides its own connecting pin

Twisted pair cable: uses color-coded pairs of insulated copper wire, contains 4 pairs; one pair sends data, one pair receives, other two are not used for data transmission
More twists = more resistant to crosstalk and noise
Data category usually stamped on outside of jacket

Shielded twisted pair: twisted pair wires that are individually insulated, also surrounded by a metallic shield
Shielding prevents electromagnetic forces from affecting the signals travelling on the wire

Unshielded twisted pair: same as above, but without the additional metallic shield; cheaper than STP

* Both STP and UTP can transmit data at similar speeds
* STP is usually more expensive than UTP
* both use RJ-45 connectors (data jacks)
* STP is more protected against noise, but UTP can use filtering and balancing to reduce noise
* both support the same maximum segment length (100m for data networks from 1 Mbps to 10 Gbps)

Two different methods for inserting twisted-wire pairs into RJ-45 plugs: T568A and T568B
Use the same standard on every plug on your network
Crossover cable: reverses the transmit and receive wires to connect PC to PC or switch to swtich
Rollover cable: reverses all wires to create a mirror image; connect a computer to router