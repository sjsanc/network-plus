Transmission medium is the physical channel through which signals travel.

Wireless can be describes as **unbounded media**.

**Line coding** is essentially a series of discrete pulses.

Digital transmission is less susceptible to interference and is easier to regenerate over long distances.

**Analog signals** must be sampled at intervals to create discrete binary values.

The **Nyquist Theorem** is that the sampling rate must be twice the signal bandwidth. Thus, telecomunnication channels use a 64 Kbps bandwidth because voice frequency range is 4000hz, sampled at twice the rate of 8000hz (8Khz), sample size is 1 byte (8bits), 8Khz x 8 bits = 64 kbps.

The bandwidth of transmission media refers to the available range of frequencies. Most digital signalling uses baseband transmission. Some use multiplexing schemes to divide the band.

Hertz (hz) is used to describe channel capacity (bandwidth), representing the number of cycles completed per second.

Pulses over a transmission medium are called **symbols.** Symbols per second = **baud rate**. 
The amount of bits per second is the **bit rate**. 
The **data rate** is the combination of signalling speed (baud) and encoding method, mixed with distance and noise. 

Attenuation is the loss of signal strength in decibels, determined by ratio of strength at origin and strength at destination.

Noise is anything transmitted that wasn't intended. Expressed as signal to noise ratio.

Copper:
- Twisted pair + Coaxial
- Suffers from high attenuation.

Fiber:
- Less susceptible to noise
- high bandwidth over longer links

Wireless
- High power usage.
- Limited range due to high interference.
- Use of radio waves is governed by the ITU (International Telecommunications Union).
- Use of certain bands require a license.

**Media Access Control**
In a multiple-access area network, nodes use a MAC method to determine when to communicate.
- Deterministic media access such as **token ring**, where a permission token is passed between devices, ensures that a single node cannot saturate the media.
- Contented-based MAC allow nodes to compete with each other for use of the media. Because collision (message sent simultaneously) are discarded, nodes are divided into collision zones to reduce waste, with traffic passed between them by bridges (the broadcast domain).

**CSMA**
Carrier Sense Multiple Access. Ethernet protocols that govern contention. 
- **Carrier Sense** - detect activity on the media.
- **Multiple Access** - multiple nodes use the same media.
- **Half Duplex** - nodes can transmit or receive, but not both at the same time.
- **CA** - Collision Detection
	- When a signal is present on the interfaces transmit and receive lines simultaneously, the node broadcasts a jam signal. Each node then waits for a random period (backoff) before attempting to send again.
- **CD** - Collision Avoidance
	- Nodes listen and wait until there is space to transmit (adds signal control overhead).

**Switched Networks**
Contention-based networks do not scale to large numbers of nodes within the same collision domain. Switches can resolve this by connecting two nodes together using a temporary circuit, reducing their collision domain to just the two, allowing for full-duplex transmission (skipping the CSMA/CD entirely).

**Broadcast Domains**
- In a broadcast domain, each node receives all traffic. Nodes that share the same broadcast address.
- Unicast - nodes only process traffic addressed to it.
- Broadcast - traffic addressed to all nodes at once.

All devices attached to a hub are part of the same collision domain.
Devices on either side of a bridge are in different collision domains.
Switches eliminate the concept of collision domains entirely.

VLAN (virtual LANs) allow networks to create separate broadcast domains within the same physical topology.

**Ethernet - IEEE 802.3**
- Uses baseband signalling.
- Uses CSMA/CD for MAC.
- Frame: 
	- Preamble > SFD > Dest. MAC > Source MAC > Ether Type > Payload > FCS
	- Preamble
		- clock sync to identify collision (CSMA/CD)
		- 8 bytes of alternating 1s and 0s, followed by SFD (11)
	- Addressing
		- a MAC address is a unique identifier for each network adaptor interface. 
		- 48 bits (6 bytes)
	- MTU - Maximum Transmission Unit
		- Usually between 46 and 1500 bytes.
	- If the MTU is greater than 1536, then it is interpreted as Ethertype, either IPv4 or IPv6 instead.
- Error Checking
	- Cyclic Redundancy Check
	- Frame Checking Sequence

**Ethernet Deployment Standards**
- xBASE-y = bit rate, signal mode, media type
- 10BASE-T = 10Mbps, Baseband, Twised Pair

: You should only need to know the distance limitations for 10GBASE-T for the
certification exam
... 
UNFINISHED NOTES

"If the central device were a switch, only the server would receive the unicast packet.
The switch tracks which MAC addresses are associated with each of its ports and only
forwards unicast traffic over the correct port."