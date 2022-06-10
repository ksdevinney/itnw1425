# Chapter 2: Network Infrastructure and Documentation

Structured cabling: uniform cabling systems created by TIA (Telecommunications Industry Associations) and EIA (Electronic Industries Alliance)
Best way to install networking media, regardless of technology and speed; assumes network is setup using a star topology

Network infrastructure components: demarc, MDFs, IDFs

Entrance facility: where an incoming network (internet) connects with the school/corporate network; equipment belongs to the service provider

Demarcation point: point where the provider's network ends and the local network begins

MDF: main distribution frame, centralized point of interconnection for an organization's LAN or WAN. May include cables running to IDFs or ethernet cables running to work spaces. Might contain the demarc or an extension, tranceiver to convert the incoming signal, other connectivity devices (switches or routers), network servers, or transmission media; only one per campus

Data room: enclosed space for holding network equipment

Racks: hold network equipment

Patch panel: central termination point for converging cables (lots of cables plugged in back here)

VOIP telephone equipment: network used to carry voice signals using TCP/IP protocols (phone calls); may include VoIP gateway device, VoIP PBX (private branch exchange). Connects to VoIP endpoints (phones)

Different data room

IDF: intermediate data frame, intermediate connection between the MDF and endpoint equipment; can be many IDFs on a campus (one per floor)

Work Areas

Work area: printers, workstations...devices

Wall jacks: can contain an outlet for voice and data, or either one

Rack systems: sides provide bracketing for attaching devices (through "rack ears"); racks usually have at least one KVM (keyboard, video, mouse switch) to connect to a single console
Organizing cables can help air flow around the rack so it doesn't overheat

**Types of cables**
* Patch cables: short, connectors on both ends
* Horiztonal cables: connects workstations to the data room, max length 100 m (90m for network device in data room to wall, 10m for wall to workstation)
* Backbone cables: connect the entrance facility and MDFs and MDFs and IDFs; thick insulation and often run through pipes

UTP (unshielded twisted pair): copper-based, wire pairs twisted inside a plastic sheath
STP (shielded twisted pair): also copper twisted wire pairs, but shielded by a metallic substance as well as insulation
Fiber optic: core of glass or plastic fibers, send light signals

**Cable Management**
Installation tips to prevent physical layer failures:

Termination: don't leave more than 1 inch of stripped cable before a twisted pair termination
Bend radius: maximum amount of bend (radius of arc) without impairing data transmission; commonly >= 4x cable diameter
Verify continuity: use a cable tester to verify each cable segment transmits data reliably
Cinching: cinch cables loosely
Protection: avoid damage from foot traffic or rolling chairs by not leaving cables on the floor (or using a cable protector); use sealed cable conduits when possible
EMI: electromagentic interference, install cables at least 3 feet away from sources (ex: fluorescent lights)
Plenum: only install cabling rated for the plenum in the plenum (area above ceiling tiles or below subflooring); these cables are coated with flame-resistant material
Grounding: follow grounding requirements
Slack: do not string cables too tightly
Cable trays: use cable management devices, but don't overfill them
Patch panels: use to organize and collect lines
Comnpany standards: use cables approved by your organization
Documentation: keep in a central location, label everything, use color-coded cables, update as needed

Monitor the environment of the data room for temperature, humidity, and airflow (among others)

Data rooms should be secure, with a locked door

## Network Documentation

Network diagrams: graphical representations of a network's devices and connections, visual overview of a network

Network mapping: discovering and identifying devices on a network, programs like Nmap and Zenmap can help

Cisco established the standard for diagram symbols in network mapping

Wiring schematic: for the network's wired infrastructure

Rack diagram: drawings to show the devices stacked in a rack system

Document relevant hardware, software, network configuration, contacts, and special instructions
Keep information in a database that can be easily updated and searched (and probably backups)

System life cycle: designing, implementing, and maintaining a network
Includes removal and disposal of outdated units, and addition of updated devices

Inventory management: monitoring and maintaining of network assets, includes hardware and software

**Labelling and Naming**

Name devices systematically, and label them

Use descriptive names (without too much information) that can help identify or find the device

Use labels on ports or tags on cables to identify the cable's purpose

**Business Documents**

RFP: request for proposal, request for vendors to submit a proposal for a service or product the business would like to purchase

MOU: memorandum of understanding, documents intentions for two or more parties to enter into an agreement

SOW: statement of work, documents in detail the work that must be completed

SLA: service-level agreement, contract (or part of a contract) that defines in measurable terms the service provided to a customer

MSA: master service agreement, contract that defines the terms of future contracts between parties

MLA: master license agreement, grants a license for a product to a third party

## Change Management

**Software and Hardware Changes**

Types of software changes:
Patch: correction or improvement to software
Upgrade: major change to software
Rollback: reverting to a previous version
Installation

Change management documentation

Includes:
Change request document
Understand and follow approval process
Change is project-managed
Provide additional documentation
Close the change