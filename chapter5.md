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

Power over Ethernet- twisted pair ethernet connections can supply power (this is how landlines work), useful for nodes far from power recepticles or that need a steady source of power
Provides relatively small amounts of power, but enough to power certain devices (like a wireless access point)

Cable's category determines the fastest network speed it can support

## Fiber Optic Cable

Data is transmitted through glass or plastic core of the cable, sent via laser (long distances) or LED (short distances), core is surrounded by glass or plastic cadding which reflects light back to the core (allows cables to bend without sacrificing signal)

Fiber optic cables can contain hundreds of fibers, or just a few, depending on their purpose

Each strand of fiber transmits in only one direction, two strands are needed for duplex communication

compared to copper, fiber optic cable allows:
* higher throughput
* high noise resistance
* excellent security
* can carry signals for longer without requiring a repeater

More expensive than twisted pair, requires special equipment for splicing

Single mode fiber: narrow core, uses laser light and reflects very little, can accomodate high bandwidths and long distances; mostly used for longer connections

Multimode fiber: larger core, many pulses of LED or laser travel at various angles; more prone to attenuation so not suited to longer distances (more than a few km); less expensive than SMF

Ferrule: extended tip of a connector that makes contact with receptacle in jack
UPC: extensively polished to created a rounded tip, allows two fibers to meet and increases efficiency
APC: also polished, end faces are placed at an angle to each other

Media conversion must occur if both copper and fiber media are used
Media converters complete the physical connection, convert electrical signals to light (and vice versa)

Hot swappable: hardware that can be updated without disrupting operations
Transceivers: modular interfaces

GBIC: standard Ethernet interface from the 90s, replaced by:
* SFP (more compact)
* XFP (supports up to 10Gbps)
* SPF+ (supports up to 16Gbps)
* QSFP (supports 4 channels in a receiver and up to 40Gbps)
* QSFP+ (up to 112Gbps)
* CFP (for 100 Gbps networks)

Transceivers include 2 ports for full-duplex communication, **bidirectional** fiber carries data in both directions

### Common Fiber Cable Problems

* Fiber type mismatch: connecting cables with different core widths or types
* wavelength mismatch: different cords use different wavelengths, transmissions are optimized for certain types of cables
* dirty connectors: dirt and dust block light

## Troubleshooting Tools

Lights on device network ports:
Steady light: connectivity
Blinking light: activity
Red or amber: problems

Tone generator: issues a signal on a wire
Tone locator (probe): emits a tone when it detects electrical activity on a wire

Multimeter: can measure circuit's resistance, voltage, and impedance

Cable continuity tester: measures whether or not cable is carrying a signal to its destination; base unit connects to one end of cable and emits a voltage, remote unit at other end detects a voltage

Cable performance tester: can measure the distance to a connectivity device, attenuation along a cable, crosstalk, termination resistance and impedance; issue pass/fail ratings for connectivity standards, store or print testing results, graphically represent crosstalk and attenuation 

Optical power meter: measures the amount of light power transmitted on a fiber optic line

### Quiz

Patch cables for a government office: green/white wire goes in first pin

Gigabit ethernet: supported by category 5e, 6a, 7