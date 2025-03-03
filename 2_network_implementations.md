**Routing Technologies**
1. *Static routing*
	1. Manually configured routing tables. The administrator explicitly defines next-hop addresses for each destination network.
	2. Must be manually updated when topology changes.
2. **Dynamic routing**
	1. Networks automatically share route information, propagating knowledge of topology changes. 
	2. *Border Gateway Protocol (BGP)*
		1. Port 179 (TCP) 
		2. Exterior gateway protocol (used between autonomous systems (AS))
		3. Path-vector protocol (instead of distance/link-state)
		4. Scales to handle the entire internet routing table.
	3. *Enhanced Interior Gateway Routing Protocol (EIGRP)*
		1. Cisco proprietary distance-vector protocol.
		2. Uses Diffusing Update Algorithm (DUAL) to calculate best paths.
		3. Fast convergence with minimal network traffic.
		4. Supports VLSM and CIDR.
	4. *Open Shortest Path First (OSPF)*
		1. Link-state routing protocol.
		2. Creates topology map through link-state advertisements (LSAs).
		3. Uses Djikstra's algorithm to find shortest path.
		4. Organises networks into areas for scalability.
		5. Faster convergence than distance-vector protocols.
3. **Route Selection**
	1. *Administrative distance*
		1. Indicates how trustworthy a routing source is (lower numbers are better)
		2. E.g. directly connected networks are more trustworthy than OSPF.
	2. *Prefix length*
		1. Indicates how specific a route is. More specific routes are prefered.
		2. E.g. a route to `192.168.1.0/24` is more specific than `192.168.0.0/16`
	3. *Metric*
		1. Value used by routing protocols to determine best path. Different for each protocol.
		2. Cost, bandwidth, delay, reliability, load, hop count
4. **Address translation**
	1. *Network Address Translation (NAT)*
		1. Maps one IP address to another.
		2. Static 1-1 mapping between public and private addresses or dynamic mapping from a pool of public addresses.
		3. Helps conserve public IP addresses by allowing many devices to connect to the internet through one address.
	2. *Port Address Translation (PAT)*
		1. aka. NAT overload or many-to-one NAT.
		2. Common in home or small business networks.
		3. Port numbers are used to track different connections through a single IP address.
5. **First Hop Redundancy Protocol (FHRP)**
	1. FHRPs provide high availability for default gateways through redundacy.
	2. *Virtual IP (VIP)*
		1. Shared IP address used by multiple physical routers
		2. Client devices use the VIP as their default gateway. 
		3. If the VIP fails, another takes over. 
	3. *Sub-interfaces*
		1. Allows one physical network port to act as several virtual ports.
		2. Each virtual port can connect to a different network.

**Switching Technologies**
1. **Virtual Local Area Network (VLAN)**
	1. Using a VLAN-capable switch, devices on the same logical network are separated into isolated logical virtual LANs.
	2. Its like a logical, rather than physical, subnet.
	3. Each port on the switch designates a separate VLAN.
	4. VLANs alleviate excessive broadcast traffic.
	5. VLAN1 is the default VLAN on most switches.
	6. *VLAN database*
		1. Storage area for VLAN configuration information (vlan.dat)
		2. Stores VLAN numbers, names and associated ports.
	7. *Switch Virtual Interface (SVI)*
		1. Allows a switch to have an IP address within that VLAN.
		2. Enables remote management of the switch.
		3. Acts as a gateway for inter-VLAN routing on Layer 3 switches.
2. **Interface Configuration**
	1. *Native VLAN*
		1. The default VLAN assigned to frames arriving on a trunk port without VLAN tags.
		2. Defaults to VLAN1 on most switches. 
		3. Best practice to change the native VLAN from VLAN1 immediately.
	2. *Voice VLAN*
		1. Dedicated VLAN for VoIP.
		2. Improved performance using QoS to reduce jitter and packet loss.
		3. Tagged traffic on a trunk port.
	3. *802.1Q tagging*
		1. Standard used to insert VLAN tags into Ethernet frames.
		2. The tag is a 4-byte field between the source MAC address and the EtherType/Length field
		3. A VLAN ID (VID) is a 12-bit value used to identify the target VLAN.
		4. Trunk ports carry tagged traffic from multiple VLANs, adding a tag to each frame.
		5. Access ports carry untagged traffic for a single VLAN.
	4. *Link Aggregation*
		1. The practice of combining multiple physical network links into a single logical link. 
		2. Provides failover redundancy and load balancing.
		3. Typically used with trunk ports, and Link Aggregation Control Protocol (LACP).
	5. *Speed*
		1. ???
	6. *Duplex*
		1. Refers to the mode in which data can be transmitted over a network.
		2. Half-duplex or one-way, like walkie-talkies and older 10BASE-T cables
		3. Full-duplex or two-way, like telephones and modern 100BASE-TX
		4. Collisions are more likely in half duplex.
3. *Spanning Tree Protocol (STP)*
	1. Protocol to ensure there are no loops in a switched Ethernet network, which might use loops for redundancy. 
	2. Ensures that only path exists between any two devices by dynamically blocking redundant paths.
	3. A central root bridge is used as a reference point. 
	4. When topology changes, STP opens up blocked ports to create new paths. 
	5. Rapid STP is a version with faster convergence.
	6. Multiple STP enables spanning trees across multiple VLANs.
4. **Maximum Transmission Unit (MTU)**
	1. The largest size of a packet in bytes that can be transmitted over a network without being fragmented.
	2. Larger MTU size increases throughput, but it must match the network capability otherwise fragmentation occurs. 
	3. Ethernet is typically 1500 bytes.
	4. *Jumbo frames*
		1. Can increase MTU to 9000 bytes or more.

**Wireless Technologies**
1. **Channels**
	1. Specific frequency ranges within the radio spectrum. They allow devices to transmit and receive signals without interference. 
	2. Each channel is centred around a base frequency: i.e. Channel 1 is 20Mhz either side of 2.412Ghz
	3. *Channel width*
		1. How much of a frequency range is used for communication. 
		2. Wider channels have higher bandwidth but more interference.
		3. 2.4GHz width is typically 20Mhz and its channels do not overlap.
		4. 5GHz offers different channel widths at 20, 40, 80, 120MHz. 
	4. *Non-overlapping channels*
		1. Channels that do overlap frequency and thus do not interfere. 
		2. In 2.4Ghz its channels 1, 6 and 11.
		3. In 5Ghz there are numerous which might overlap.
		4. As channel width increases, overlapping is more likely to occur.
	5. **Regulatory impacts**
		1. *802.11h*
			1. *Dynamic Frequency Selection (DSF)* 
				1. Ensures all devices automatically detect and avoid ranges used by radar systems.
			2. *Transmit Power Control (TPU)*
				1. Devices must detect and limit transmit power in regulated environments.
				2. Higher transmit power increases potential for interference.
2. **Frequency Options**
	1. *2.4GHz*
		1. Longest range. Can penetrate obstacles like walls.
		2. Lower speed due to more interference (crowded) and lower channel width (20mhz).
		3. 3 non-overlapping channels shared between many devices like microwaves, bluetooth, cordless phones.
	2. *5.6GHz*
		1. Shorter range. Less effective at penetration.
		2. Wider channels widths (20, 40, 60, 120) and less interference.
		3. Many more available channels (up to 25 non-overlapping)
	3. *6GHz*
		1. Shortest range. 
		2. Wide channels up to 160mhz.
		3. Less congested as recently opened.
	4. *Band steering*
		1. Used in dual and tri-band wifi to automatically direct devices to the appropriate frequency based on device capability, signal strength and network congestion.
3. **Service Set Identifier (SSID)**
	1. *Basic Service Set Identifier (BSSID)*
		1. The primary identifier for a wireless network. It is the name broadcast by the access point.
		2. E.g. `HomeNetwork`
	2. *Extended Service Set Identifier (ESSID)*
		1. Used when there are multiple access points broadcasting for the same network.
		2. E.g. `HomeNetwork_1`
4. **Network Types**
	1. *Mesh networks*
		1. Where each node is connected to multiple other nodes.
		2. Mesh networks are self-healing when nodes fail.
		3. Devices roam seamless within the mesh as it reconnects to closest nodes.
		4. One internet gateway router with many satellite node / access points.
		5. Nodes communicate to optimise data pathways, for example to alleviate congestion.
	2. *Ad hoc*
		1. Devices in an ad hoc network communicate without a centralised access point.
		2. Typically temporary. Each node acts as both client and server. No internet access.
	3. *Point to point*
		1. Two directly connected devices.
		2. ISP backbones are typically point-to-point networks.
	4. *Infrastructure*
		1. Networks that use a router??
5. **Encryption**
	1. *Wi-Fi Protected Access 2 (WPA2)*
		1. Uses Advanced Encryption Standard (AES) and a password (pre-shared key (PEK)).
	2. *WPA3*
		1. Uses AES-GCM and SHA-384 encryption standards.
		2. More resistant to brute force and MITM attacks using Simultaneous Authentication of Equals (SAE).
		3. Protection against offline dictionary attacks.
6. **Guest Networks**
	1. A method providing a separate, isolated network guests, so that do not have to connect to the main network.
	2. Typically only provides internet access, and have their own SSID and password.
	3. *Captive Portals*
		1. A special network that requires users to interact with a landing page before access. 
		2. They can be vulnerable to MITM attacks.
7. **Authentication**
	1. *Pre-shared Key (PSK) vs Enterprise*
		1. Pre-shared keys are basically just a password.
		2. Enterprise authentication often involves things like RADIUS servers, 802.1X authentication, Extensible Authentication Protocol (EAP).
8. **Antennas**
	1. *Omnidirectional* 
		1. Radiates signals in all directions on a horizontal plane. 
		2. Little vertical coverage. Typical in WiFi.
	2. *Directional*
		1. Focuses signals on a specific direction.
		2. Better for long range.
9. **Access Points**
	1. *Autonomous*
		1. An access point that manages its own configuration, without a central authority.
		2. Typical in SOHO networks.
	2. *Lightweight*
		1. Access point managed by a controller.
		2. Relies on a central wireless LAN controller (WLC).

**Physical Installations**
1. Important Implications
	1. Locations
		1. Intermediate Distribution Frame (IDF)
		2. Main Distribution Frame (MDF)
	2. Rack size
	3. Port-side exhaust intake
	4. Cabling
		1. Patch panel
		2. Fibre distribution panel
	5. Lockable
2. Power
	1. Uninterrupted power supply (UPS)
	2. Power distribution unit (PDU)
	3. Power load
	4. Voltage
3. Environmental Factors
	1. Humidity
	2. Fire suppression
	3. Temperature
