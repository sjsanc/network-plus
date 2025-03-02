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
	2. Each port on the switch designates a separate VLAN.
	3. VLANs alleviate excessive broadcast traffic.
	4. VLAN1 is the default VLAN on most switches.
	5. *VLAN database*
		1. Storage area for VLAN configuration information (vlan.dat)
		2. Stores VLAN numbers, names and associated ports.
	6. *Switch Virtual Interface (SVI)*
		1. Allows a switch to have an IP address within that VLAN.
		2. Enables remote management of the switch.
		3. Acts as a gateway for inter-VLAN routing on Layer 3 switches.
2. **Interface Configuration**
	1. Native VLAN
	2. Voice VLAN
	3. 802.1Q tagging
	4. Link Aggregation
	5. Speed
	6. Duplex
3. Spanning Tree
4. Maximum Transmission Unit (MTU)
	1. Jumbo frames

**Wireless Technologies**
1. Channels
	1. Channel width
	2. Non-overlapping channels
	3. Regulatory impacts
		1. 802.11h
2. Frequency Options
	1. 2.4GHz
	2. 5.6GHz
	3. 6GHz
	4. Band steering
3. Service Set Identifier (SSID)
	1. Basic Service Set Identifier (BSSID)
	2. Extended Service Set Identifier (ESSID)
4. Network Types
	1. Mesh networks
	2. Ad hoc
	3. Point to point
	4. Infrastructure
5. Encryption
	1. Wi-Fi Protected Access 2 (WPA2)
	2. WPA3
6. Guest Networks
	1. Captive Portals
7. Authentication
	1. Pre-shared Key (PSK) vs Enterprise
8. Antennas
	1. Omnidirectional vs Directional
9. Autonomous vs Lightweight Access Point

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
