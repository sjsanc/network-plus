**A. Install and Configure Firewalls and Proxies**
- Firewalls filter traffic according to rules, either at network boundaries or for individual hosts.
- **Packet Filtering**
	- Layer 3 (for IP + protocol) and layer 4 (for ports)
	- Stateless inspection (retains no memory)
	- Inspect headers and drop based on:
		- *IP filtering*
		- *Protocol type* - (UDP, TCP etc)
		- *Port filtering*
	- *ingress* (inbound) *egress* (outbound) filtering. Egress filtering can help prevent trojans from phoning home. 
- **Stateful Filtering**
	- Layer 5 (session)
	- Circuit-level stateful inspection firewall. Maintains state about each session in a *state table*.
	- Monitors packet sequences and TCP sessions to detect *session hijacking* and *malicious sessions*.
- **Next-Gen Firewall (NGF)**
	- Layer 7 (Application)
	- Performs analysis of packet contents to detect malicious payloads
	- Powerful but vulnerable to DoS attacks that exploit their complexity.
	- Cannot examine encrypted packets unless configured with a SSL inspector.
- **Appliance Firewall**
	- A physical device, usually at the network boundary, that uses application firmware to perform firewall services.
- **Application Based Firewall**
	- Runs as software. Personal firewall. 
- **Forward Proxy Server**
	- Connects clients (like web browsers) to internet hosts, forwarding requests on behalf of the client. 
	- It obscures the client's real IP from the web server's view.
	- It can act as a content filter by inspecting packet contents.
	- It can act as a web security gateway, controlling which web servers can be accessed.
	- It can cache web pages to improve load times for the client.
	- Multipurpose proxies serve multiple protocols, not just HTTP/S 
	- A non-transparent proxy is one that the client is configured to route through.
	- A transparent (or forced) proxy is one that intercepts traffic without the client's knowledge; and must be implemented within an inline appliance such as switch or router.
- **Content Filters**
	- Web content filtering can be implemented, like above, as a security gateway, either as an appliance or as software. 
	- Usually includes protocol filtering; url blacklists; time of day use etc.
- **Reverse Proxy Server**
	- Forwards inbound traffic coming from the web to internal network hosts.
	- Usually, application servers such as VoIP should not be in the perimeter network (directly accessible by external hosts), but instead be behind a reverse proxy that can perform content filtering on inbound traffic. 
- **Firewall / ACL Configuration**
	- *least action* - only allow the minimum of traffic through according to rules.
	- Rules are processed top to bottom, so most specific rules should be at the top.
	- Traffic that fails to match any rules is an *implicit deny*.
	- Rule parameters are called *tuples*.
	- Some basic firewall principles:
		- Block traffic on the external interface coming from internal IPs (obviously spoofed)
		- Block traffic on the external interface with internal protocols like DHCP
		- Perform pentesting to and monitor logs
- **`iptables`**
	- TODO: iptables doesn't work on my Arch install.
- **Misconfigured ACLs**
	- Can block packets that should be allowed. For example, blocking TCP/UDP.
	- To debug, check connection on either side of a firewall; temporarily disable the firewall.

**B. Explain use of IDS/IPS and UTM**
- **Network Intrusion Detection System**
	- Software like Snort sniffs packets and analyses packets for common intrusion attempts such as password guessing, port scans, worms, malformed packets etc.
- **Intrusion Prevention System**
	- Like a NIDS but provides active responses such as ending TCP session, sending a spoofed reset packet, blocking the attacker's IP (shunning), neutralising harmful packets via modification, or even just execute a custom script.
	- Positioned inline at the perimeter. 
- **Anti-Virus**
	- Observes processes and scans them for malware signatures. Tags them with *Common Malware Enumeration (CME)* codes and possible quarantines or erases them.
- **Unified Threat Management**
	- Software that centralises security controls (creating a single point of failure).
- **Host-Based IDS and IPS**
	- Captures traffic on a single host (basically locally installed antimalware).
- **Signature Management**
	- If traffic matches a pattern (signature) in the malware DB
	- Doesn't provide protection to unknown malware (addressed by behaviour-based detection)
	- Signals need to be constantly updated. 
	- Produces false-positives/negatives.
- **File Integrity Monitoring**
	- Audits files against authorised versions.