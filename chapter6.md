# Chapter 6: Wireless Networking

## Characteristics of Wireless Transmissions

Wireless signals are carried through the air by electromagnetic waves

Wireless spectrum: airwaves, frequency range of electromagnetic waves used for data and voice, spans frequency bands between 9 kHz and 300 GHz

Band used by a wireless device is defined by its frequency range; bands are subdivided into channels and channels are subdivided into narrowband channels so devices can share the same band

FHSS: short bursts of data are transmitted on a single frequency, next burst goes to next frequency in the sequence; cheaper and performs better in crowded, indoor environments
DSSS: data streams are divided into "chips" and spread over all available frequencies at the same time, uses bandwidth more efficiently and has a higher throughput

DSSS users: Wi-Fi, ZigBee
FHSS users: Bluetooth

Different technologies have ways of handling collisions

Antennas are used for both transmission and reception of wireless signals
Electrical signal travels from a transmitter to an antenna, antenna emits the signal as a series of electromagnetic waves, waves move through the air until they reach their destination

Unidirectional antenna: issues signals along a single directiom; used when the source needs to communicate with one destination (satellite downlink for TV signals)
Omnidirectional antenna: issues and receives wireless signals with equal strength in all directions; many different receivers must be able to pick up the signal (cell towers, TV and radio stations)

Propogation: how wave travels from one point to another
LOS propogation: signal travels directly in a straight line from transmitter to receiver; ideal but not practical due to atmosphere

Fading: energy from a signal loses strength as it passes through obstacles
Attenuation: signal loses strength the farther it travels from its transmitter
Interference: wireless signals are vulnerable to EMI because they travel without protection (like cable shielding)
Refraction: waves are altered by travelling through different mediums
Reflection: waves bounce back as they encounter certain obstacles
Scattering: waves are diffused when they hit certain surfaces
Diffraction: split into secondary (smaller) waves when they hit an obstruction

## Wireless Standards

Internet of Things: anything that can connect to the internet

Connected devices within a home create a Home Area Network

ZigBee: low powered, battery conserving wireless technology; simple and reliable, secure

Z-Wave: smart home protocol that provides signaling and control; devices on the network have a node ID and the entire network uses a network ID

Bluetooth: unites various types of separate devices; usually requires close proximity, devices must be paired; subject to security risks

ANT+: gathers and tracks information, can wirelessly sync to other devices (used by smart watches)

RFID: uses electromagnetic fields to store data on a small chip that can transmit and receive data; contactless payment
* active reader passive tag: tag pulls power from reader, only works up to a few cm
* passive reader active tag: battery-powered tag actively transmits data at regular intervals, can work up to 200m away
* active reader active tag: reader interacts with battery-powered tag

NFC: form of RFID, transfers data over short distances; do not require power of their own

Wireless USB: operates on a relatively uncrowded band, requires little power and has ~10m range

IR: collects data through sensors, uses wavelength just longer than red (invisible); requires unobstructed line of sight between transmitter and receiver, dust can obstruct

## WLAN Standards

On layers 1 and 2

WiFi- most popular WLAN standard

### Access Method

802.11 networks can be combined with other 802 networks, but 802.11 devices cannot prevent collisions

CSMA/CA reduces the chance of collisions, but cannot detect or recover from collisions; uses ACK packets to verify transmission
802.11 require more overhead than 802.3 networks (ethernet)

Nodes too far apart cannot collaborate in preventing collisions; RTS/CTS prototcol can reserve the medium for one node's use

### Association

Node with wireless protocols running constantly surveys the area for evidence of an access point

Active scanning: client takes initivative
Passive scanning: access point takes initiative

BSS: group of nodes that share an access point
ESS: group of access points connected to the same LAN

...

## Implementing a Wireless Network

### Topologies

ad hoc: small number of nodes positioned close together

infrastructure: intervening connectivity device accepts wireless signals and retransmits them to the rest of the network

mesh: several access points as peer devices on the network

...

## Wifi Network Security

Authentication: comparing and matching a client's credentials with the credentials in a client database
Encryption: scrambling data into a format that can only be read by a certain algorithm

### WPA/WPA2

Assigns every transmission its own key

---

Quiz

A hacker takes advantage of an open Bluetooth connection to send a virus to a user's smartphone. What type of security breach has occurred?
* Bluejacking