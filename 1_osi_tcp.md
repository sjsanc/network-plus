**Open Systems Interconnection**
- Developed in 1977 by ISO

1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application

*Addressing* - where data should go
*Encapsulation* - how data should be packaged

Each layer adds a header to the data payload to create a complete *protocol data unit (PDU)*.

**Layer 1 - Physical**
- *Segment* - nodes that can access the same physical media. 
- **Defines**:
	- *Topology* - layout of nodes 
	- *Interfaces* - cable spec, pin-out details, connector mediums etc
	- *Modulation schemes*
- **Devices**: 
	- *Transceivers* - appliances that send/receive signals  
	- *Repeaters* - appliances that amplify electronic signals 
	- *Hubs* - multi-port repeaters
	- *Media Converters* - converts media signalling
	- *Modems* - converts between digital and analog signals
- PDU: *Bits*

**Layer 2 - Data Link**
- Transfers data between nodes on the same *logical segment*. A local segment might include multiple physical segments, making it a *logical topology.*
- *Interfaces* are described using local or hardware addresses.
- *Segment* - nodes can send traffic to each other using hardware addresses.
- **PDU**: A *frame*
	- A destination address
	- A source address
	- A payload
	- An error check
- Media Access Methods:
	- Bus-based topology + contention
	- Ring-based topology + token-passing
- **Devices**:
	- *NIC (Network Interface Cards)* - assembling/disassembling frames
	- *Bridges* - joins two network segments into one logical segment without adding more nodes.
	- *Switches* - advanced bridge with many ports
	- *WAP (Access Points)* - allows wireless nodes to connect
- IEEE 802.3 (Ethernet)
	- *MAC Sublayer* - defines how multiple interfaces share the same transmission medium. Covers topology, media access method, addressing, frame format and error checking.
- IEEE 802.2 (Logical Link Layer)
	- Provides a standard Network-layer service interface. 

**Level 3 - Network**
- Moves data around a network of networks (internet).
- Routes packets through logical networks via routers.
- Includes:
	- *WAN Router* - can communicate using various layer 2 formats + firewall
- Segment:
	- Subnets connect to the network via a layer 2 device.
	- Nodes within a subnet can communicate directly, but must go through a router to access nodes in other network segments.
- PDU: *packet* or *datagram*

**Layer 4 - Transport**
- end-to-end or host-to-host layer
- assigns port numbers to network applications
- multiplexes segments using port numbers
- ensures reliable data delivery
- Includes:
	- Multi-layer switches
	- Loadbalancers
- PDU: *segment*

**Layer 5 - Session**
- communication between client and server is called a *session* or *dialog*
- provides functions for establishing and managing this dialog:
	- *one-way simplex* - one sends, one receives
	- *two-way alternate* - host take turns in sending
	- *two-way simultaneous* - either host can send at any time

**Layer 6 - Presentation**
- transforms data from the network format into the application format

**Layer 7 - Application**

**TCP/IP**
- Transmission Control Protocol / Internet Protocol
- ARPA Model
	- Application, Transport, Internet, Link

**Link / Network Interface Layer**
- Equivalent to OSI Physical and Data Link combined. 
- Defines hosts connection to network media.
- LAN (Ethernet, Wifi), WAN (T-carrier, ISDN, DSL)

**Internet Layer**
- Provides addressing and routing functions
- Internet Protocol (IP) and Address Resolution Protocol (ARP)

**Transport Layer**
- Establishes connection between different applications that the hosts are communicating with. 
- Connection-oriented delivery with TCP
- Connectionless delivery with UDP (Universal Datagram Protocol)

**Application Layer**
- FTP, HTTP, SMTP etc.

**Packet v Circuit Switching**
- Circuit-switching in the original ARPANET required a dedicated circuit path to be designated between two computers. 
- Packet switching allowed packets to take any route between two hosts.
	- Packet switching enabled fragmentation of information, which improves robustness as packets can be resent at lower cost.

**ISOC** - Internet Society
**IAB** - Internet Architecture Board
**IETF** - Internet Engineering Task Force
**IANA** - Internet Assigned Numbers Authority
**ICANN** - Internet Corporation for Assigned Names and Numbers
