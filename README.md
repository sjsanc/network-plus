# 🖥️ CompTIA Network+

Study notes for the CompTIA Network+ exam.

1. [Networking Concepts](https://github.com/sjsanc/network-plus/blob/master/1_networking_concepts.md)
	1. OSI Model
		1. Physical
		2. Data Link
		3. Network
		4. Transport
		5. Sessions
		6. Presentation
		7. Application
	2. Appliances
		8. Physical & Virtual
			1. Router
			2. Switch
			3. Firewall
			4. Intrusion Detection System (IDS)
			5. Load Balancer
			6. Proxy
			7. Network-Attached Storage (NAS)
			8. Storage Area Network (SAN)
			9. Wireless Access Point (WAP)
			10. Wireless Controller
		9. Applications
			1. Content Delivery Network (CDN)
		10. Functions
			2. Virtual Private Network (VPN)
			3. Quality of Service (QoS)
			4. Time-to-Live (TTL)
	3. Cloud Concepts
		1. Network Functions Virtualisation (NFV)
		2. Virtual Private Cloud (VPC)
		3. Network Security Groups
		4. Network Security Lists
		5. Cloud Gateways
			1. Internet Gateway
			2. Network Address Translation (NAT) Gateway
		6. Cloud Connectivity Options
			1. VPN
			2. Direct Connect
		7. Deployment Models
			1. Public
			2. Private
			3. Hybrid
		8. Service Models
			4. Software as a Service (SaaS)
			5. Infrastructure as a Service (IaaS)
			6. Platform as a Service (PaaS)
		9. Scalability
		10. Elasticity
		11. Multi-tenancy
	4. Common Ports, Protocols, Services and Traffic
		12. Protocols
			1. File Transfer Protocl (FTP)
			2. Secure File Transfer Protocol (SFTP)
			3. Secure Shell (SSH)
			4. Telnet
			5. Simple Mail Transfer Protocol (SMTP)
			6. Domain Name System (DNS)
			7. Dynamic Host Configuration Protocol (DHCP)
			8. Trivial File Transfer Protocol (TFTP)
			9. Hypertext Transfer Protocol (HTTP)
			10. Network Time Protocol (NTP)
			11. Simple Network Management Protocol (SNMP)
			12. Lightweight Directory Access Protocol (LDAP)
			13. Hypertext Transfer Protocol Secure (HTTPS)
			14. Server Message Block (SMB)
			15. Syslog
			16. Simple Mail Transfer Protocol Secure (SMTPS)
			17. Lightweight Directory Access Protocol Secure (LDAPS)
			18. Structure Query Language (SQL) Server
			19. Remote Desktop Protocol (RDP)
			20. Sessions Initiation Protocol (SIP)
		13. Internet Protocol (IP) Type
			1. Internet Control Message Protocol (ICMP)
			2. Transmission Control Protocol (TCP)
			3. User Datagram Protocol (UDP)
			4. Generic Routing Encapsulation (GRE)
			5. Internet Protocol Security (IPSec)
				1. Authentication Header (AH)
				2. Encapsulating Security Payload (ESP)
				3. Internet Key Exchange (IKE)
		14. Traffic Types
			6. Unicast
			7. Multicast
			8. Anycast
			9. Broadcast
	5. Transmission Media and Transceivers
		1. Wireless
			1. 802.11 
			2. Cellular
			3. Satellite
		2. Wired
			4. 802.3
			5. Single-mode vs Multi-mode fibre
			6. Direct Attach copper (DAC)
			7. Twinaxial cable
			8. Coaxial cable
			9. Cable speeds
			10. Plenum vs non-plenum cable
		3. Transceivers
			1. Ethernet
			2. Fibre Channel (FC)
		4. Form Factors
			1. Small form-factor pluggable (SFP)
			2. Quad small form-factor pluggable (QSFP)
		5. Connector types
			1. Subscriber connector (SC)
			2. Local connector (LC)
			3. Straight tip (ST)
			4. Multi-fibre push on (MPO)
			5. Registered jack (RJ)11
			6. RJ45
			7. F-type
		6. Network Topologies, Architectures and Types
			8. Mesh
			9. Hybrid
			10. Star/hub and spoke
			11. Spine and leaf
			12. Point to point
			13. Three-tier hierarchical model
				1. Core
				2. Distribution
				3. Access
			14. Collapsed Core
			15. Traffic Flows
				4. North-south
				5. East-west
		7. IPv4 Network Addresses
			1. Public vs Private
				1. Automatic Private IP Addressing (APIPA)
				2. RFC1918
				3. Loopback/localhost
			2. Subnetting
				4. Variable Length Subnet Mask (VLSM)
				5. Classless Inter-domain Routing (CIDR)
			3. IPv4 Address Classes
				1. Class A
				2. Class B
				3. Class C
				4. Class D
				5. Class E
		8. Modern Network Environments
			4. Software-defined network (SND) and Software-defined wide area network (SD-WAN)
				6. Application aware
				7. Zero-touch provisioning
				8. Transport agnostic
				9. Central policy management
			5. Virtual Extensible Local Area Network (VXLAN)
				10. Data centre interconnect (DCI)
				11. Layer 2 encapsulation
			6. Zero trust architecture (ZTA)
				12. Policy-based authentication
				13. Authorisation
				14. Least Privilege Access
			7. Secure Access Secure Edge (SASE) / Security Service Edge (SSE)
			8. Infrastructure as Code (IaC)
				15. Automation
					1. Playbooks/templates/reusable tasks
					2. Configuration drift/compliance
					3. Upgrades
					4. Dynamic Inventories
				16. Source Control
					1. Version Control
					2. Central Repository
					3. Conflict Identification
					4. Branching
			9. IPv6 Addressing
				17. Mitigating address exhaustion
				18. Compatibility requirements
					1. Tunnelling 
					2. Dual stack
					3. NAT64
2. Network Implementation
	6. Routing Technologies
		1. Static routing
		2. Dynamic Routing
			1. Border Gateway Protocol (BGP)
			2. Enhanced Interior Gateway Routing Protocol (EIGRP)
			3. Open Shortest Path First (OSPF)
		3. Route Selection
			1. Administrative distance
			2. Prefix length
			3. Metric
		4. Address translation
			4. NAT
			5. Port address translation (PAT)
		5. First Hop Redundancy Protocol (FHRP)
			1. Virtual IP (VIP)
			2. Subinterfaces
	7. Switching Technologies
		6. Virtual Local Area Network (VLAN)
			1. VLAN database
			2. Switch Virtual Interface (SVI)
		7. Interface configuration
			1. Native VLAN
			2. Voice VLAN
			3. 802.1Q tagging
			4. Link aggregation
			5. Speed
			6. Duplex
		8. Spanning Tree
		9. Maximum Transmission Unit (MTU)
			1. Jumbo frames
	8. Wireless Technologies
		10. Channels
			2. Channel width
			3. Non-overlapping channels
			4. Regulatory impacts
				1. 802.11h
		11. Frequency options
			5. 2.4GHz
			6. 5Ghz
			7. 6Ghz
			8. Band steering
		12. Service set identifier (SSID)
			9. Basic service set identifier (BSSID)
			10. Extended service set identifier (ESSID)
		13. Network Types
			11. Mesh networks
			12. Ad hoc
			13. Point to point
			14. Infrastructure
		14. Encryption
			15. Wi-Fi Protected Access 2 (WPA2)
			16. WPA3
		15. Guest Networks
			17. Captive portals
		16. Authentication
			18. Pre-shared Key (PSK) vs Enterprise
		17. Antennas
			19. Omnidirectional vs Directional
		18. Autonomous vs Lightweight access point
	9. Physical Installations
		19. Important implications
			20. Locations
				2. Intermediate distribution frame (IDF)
				3. Main distribution frame (MDF)
			21. Rack size
			22. Port-side exhaust intake
			23. Cabling
				4. Patch panel
				5. Fibre distribution panel
			24. Lockable
		20. Power
			25. Uninterrupted power supply (UPS)
			26. Power distribution unit (PDU)
			27. Power load
			28. Voltage
		21. Environmental factors
			29. Humidity
			30. Fire suppression
			31. Temperature
3. Network Operations
	1. Organisational Processes
		1. Documentation
			1. Physical vs logical diagrams
			2. Rack diagrams
			3. Cable maps and diagrams
			4. Network diagrams
				1. Layer 1
				2. Layer 2
				3. Layer 3
			5. Asset inventory
				1. Hardware
				2. Software
				3. Licensing
				4. Warranty support
			6. IP address management (IPAM)
			7. Service-level agreement (SLA)
			8. Wireless survey/heat map
		2. Life-cycle management
			1. End-of-life (EOL)
			2. End-of-support (EOS)
			3. Software management 
				1. Patches and bug fixes
				2. Operating system (OS)
				3. Firmware
			4. Decommissioning
		3. Change management
			1. Request process tracking/service request
		4. Configuration management
			2. Production configuration
			3. Backup configuration
			4. Baseline/golden configuration
	2. Network Monitoring Technologies
		1. Methods
			1. SNMP
				1. Traps
				2. Management information base (MIB)
				3. Versions
					1. v2c
					2. v3
				4. Community strings
				5. Authentication
			2. Flow data
			3. Packet capture
			4. Baseline metrics
				1. Anomaly alerting notifications
			5. Log aggregation
				1. Syslog collector
				2. Security information and event management (SIEM)
			6. Application programming interface (API) integration
			7. Port mirroring
		2. Solutions
			8. Network discovery
				1. Ad-hoc
				2. Scheduled
			9. Traffic analysis
			10. Performance monitoring
			11. Availability monitoring
			12. Configuration monitoring
	3. Disaster Recovery
		1. DR metrics
			1. Recovery point objective (RPO)
			2. Recovery time obejctive (RTO)
			3. Mean time to repair (MTTR)
			4. Mean time between failures (MTBF)
		2. DR sites
			1. Cold site
			2. Warm site
			3. Hot site
		3. High-availability appraoches
			1. Active-active
			2. Active-passive
		4. Testing
			1. Tabletop exercises
			2. Validation tests
	4. IPv5 and IPv6 Network Services
		1. Dynamic Addressing
			1. DHCP
				1. Reservations
				2. Scope
				3. Lease time
				4. Options
				5. Relay/IP helper
				6. Exclusions
			2. Stateless Address Autoconfiguration (SLAAC)
		2. Name Resolution
			1. DNS
				1. Domain Name Security Extensions (DNSSEC)
				2. DNS over HTTPS (DoH) and DNS over TLS (DoT)
				3. Record types
					1. Address (A)
					2. AAAA
					3. Canonical (CNAME)
					4. Mail exchange (MX)
					5. Text (TXT)
					6. Nameserver (NS)
					7. Pointer (PTR)
				4. Zone types
					8. Forward 
					9. Reverse
				5. Authoritative vs non-Authoritative
				6. Primary vs Secondary
				7. Recursive
			2. Hosts file
		3. Time protocols
			1. NTP
			2. Precision time protocol (PTP)
			3. Network time security (NTS)
	5. Network Access and Management Methods
		1. Site-to-site VPN
		2. Client-to-site VPN
			1. Clientless
			2. Split tunnel vs full tunnel
		3. Connection methods
			1. SSH
			2. Graphical User Interface (GUI)
			3. API
			4. Console
		4. Jump box/host
		5. In-band vs out-of-band management
4. Network Security
	6. Basic Network Security
		6. Logical Security
			1. Encryption
				1. Data in transit
				2. Data at rest
			2. Certificates
				1. Public key infrastructure (PKI)
				2. Self-signed
			3. Identity and access management (IAM)
				1. Authentication
					1. Multifactor authentication (MFA)
					2. Single sign-on (SSO)
					3. Remote Authentication Dial-in User Service (RADIUS)
					4. LDAP
					5. Security Assertion Markup Language (SAML)
					6. Terminal Access Controller Access Control System Plus (TACACS+)
					7. Time-based authentication
				2. Authorisation
					8. Least privilege
					9. Role-based access control
			4. Geofencing
		7. Physical Security
			1. Camera
			2. Locks
		8. Deception technologies
			1. Honeypot
			2. Honeynet
		9. Common Security Terminology
			1. Risk
			2. Vulnerability
			3. Exploit
			4. Threat
			5. Confidentiality, Integrity and Availability (CIA) triad
		10. Audits and Regulatory Compliance
			6. Data locality
			7. Payment Card Industry Data Security Standards (PCI DSS)
			8. General Data Protection Regulation (GDPR)
		11. Network Segmentation enforcement
			9. Internet of Things (IoT) and Industrial Internet of Things (IIoT)
			10. Supervisory Control and Data Acquisition (SCADA), 
			11. Industrial Control System (ICS)
			12. Operational Technology (OT)
			13. Guest
			14. Bring your own device (BYOD)
	7. Types of Network Attacks and Impact
		12. (Distributed) Denial of Service ((D)DoS)
		13. VLAN hopping
		14. MAC flooding
		15. ARP poisoning + spoofing
		16. DNS poisoning + poisoning
		17. Rogue devices and services
			15. DHCP
			16. AP
		18. Evil twin
		19. On-path attack
		20. Social Engineering
			17. Phishing
			18. Dumpster-diving
			19. Shoulder-surfing
			20. Tailgating
		21. Malware
	8. Network Security and Defense Techniques
		22. Device hardening
			21. Disable unused ports and services
			22. Change default passwords
		23. Network Access Control (NAC)
			23. Port security
			24. 802.1X
			25. MAC filtering
		24. Key management
		25. Security rules
			26. Access control list (ACL)
			27. Uniform Resource Locator (URL) filtering
			28. Content filtering
		26. Zones
			29. Trusted vs untrusted
			30. Screened subnet
5. Network Troubleshooting
	1. Troubleshooting Methodology
		1. Identify the problem
			1. Gather information
			2. Question users
			3. Identify symptoms
			4. Determine is anything has changed
			5. Duplicate the problem, if possible
			6. Approach multiple problems individually
		2. Establish a theory of probable cause
			1. Question the obvious
			2. Consider multiple approaches
				1. Top-to-bottom/bottom-to-top OSI model
				2. Divide and conquer
		3. Test the theory to determine the cause
			1. If confirmed, determine next steps
			2. If not confirmed, establish new theory or escalate
		4. Establish a plan of action to resolve problem and identify potential effects
		5. Implement the solution or escalate as necessary
		6. Verify full system functionality and implement preventative measures if applicable
		7. Document findings, actions, outcomes and lessons learned throughout the process
	2. Troubleshooting Common Cabling and Physical Interface Issues
		8. Cable issues
			1. Incorrect cable
				1. Single mode vs multimode
				2. Category 5/6/7/8
				3. Shielded twisted pair (STP) vs unshielded twisted pair (UTP)
			2. Signal degradation
				4. Crosstalk
				5. Interference
				6. Attenuation
			3. Improper termination
			4. Transmitter (TX) / Receiver (RX) transposed
		9. Interface issues
			1. Increasing interface counters
				1. Cyclic redundancy check (CRC)
				2. Runts
				3. Giants
				4. Drops
			2. Port status
				1. Error disabled
				2. Administratively down
				3. Suspended
		10. Hardware issues
			1. Power over Ethernet (PoE)
				1. Power budget exceeded
				2. Incorrect standard
			2. Transceivers
				1. Mismatch
				2. Signal strength
	3. Common issues with network services
		1. Switching issues
			1. STP
				1. Network loops
				2. Root bridge selection
				3. Port roles
				4. Port states
			2. Incorrect VLAN assignment
			3. ACLS
		2. Route selection
			4. Routing table
			5. Default routes
		3. Address pool exhaustion
		4. Incorrect default gateway
		5. Incorrect IP address
			1. Duplicate IP address
		6. Incorrect subnet mask
	4. Common performance issues
		1. Congestion/contention
		2. Bottlenecking
		3. Bandwidth
			1. Throughput capacity
		4. Latency
		5. Packet loss
		6. Jitter
		7. Wireless
			1. Interference
				1. Channel overlap
			2. Signal degradation or loss
			3. Insufficient wireless coverage
			4. Client disassociation issues
			5. Roaming misconfiguration
	5. Tools & Protocols
		1. Software Tools
			1. Protocol Analyzer
			2. Command Line
				1. ping
				2. traceroute/tracert
				3. nslookup
				4. tcpdump
				5. dig
				6. netstat
				7. ip/ifconfig/ipconfig
				8. arp
				9. nmap
				10. Link Layer Discovery Protocol (LLDP)
				11. Speed tester
			3. Hardware tools
				1. Toner
				2. Cable tester
				3. Taps
				4. Wi-Fi analyzer
				5. Visual fault locator
			4. Basic networking device commands
				6. show mac-address-table
				7. show route
				8. show interface
				9. show config
				10. show arp
				11. show vlan
				12. show power