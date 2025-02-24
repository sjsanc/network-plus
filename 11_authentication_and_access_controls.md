**A.**
**Explain Authentication Controls and Attacks**
- Access controls are the rules that govern how subjects (users) interact with objects (resources).
- *ACLs* lists the privileges granted to a subject for an object.
- **Identity and Access Management (IAM)**
	- *Identify* - creating an account or ID
	- *Authenticate* - proving that a subject is who they say they are
	- *Authorise* - determine what rights the subject has
	- *Account* - tracking the subject's usage of rights
- Users can be trusted or untrusted (such as guests, which or may not be authenticated).
- *Role separation* prevent single points of failure, and ensures subjects only have as much power (rights) as needed for their roles (least privilege).
- *Insider Threat* - angry employees.
- *Logic Bombs* - like fork-bombs. Scripts that cannot be treated as malware. 
- *Social Engineering* - human hacking. Impersonation. 
- *Spear Phising* - targeted phising attack
- *Whaling* - targeting CEOs
- *Pharming* - malicious DNS spoofing
- *Ransomware* - give me money or i'll encrypt ur machine
- *Multifactor and 2FA*
- *SSO*
- *Something you know* - logon, PIN, password etc
- *Brute Force* - dictionary attacks, hash collisions
- *Cleartext Password reading*
- *Something you have* -  digital tokens, security keys, one-time-passwords
- *Something you are/do* - biometrics
- *Somewhere you are* - geolocation

**B.**
**Explain the use of Authentication Protocols and Directory Services**
- Local Authentication
	- *LAN Manager* (LM / LANMAN / NTLM / NTLMv2)
		- NOS developed by Microsoft and 3Com.
		- Challenge/response authentication protocol.
	- *Linux Local Authentication*
		- `/etc/passwd` and `/etc/group` and `/etc/shadow` (for pw hashes)
- Kerberos
	- Network auth protocol from MIT 1980s.
	- Provides single sign-on (SSO).
	- Used in Windows 2000 and later.
	- Clients request from a server and are verified by a Key Distribution Center (KDC) (TCP/UDP port 88), consisting of:
		- Authentication Service
		- Ticket Granting Service
	- Users are provided a Ticket Granting Ticket. To access a resource, they request a Service Ticket by supplying the TGT to receive a Ticket Granting Service (TGS).
- Digital Certificates
	- Depends on public key cryptography (asymmetric encryption).
		- Using a key pair, you distribute a public key which can encrypt messages that only the private key and decrypt. 
		- To authenticate yourself, you encrypt a signature with your private key that can only be decrypted with your public key. 
	- PGP is supported by certificate authorities (chains of issuers and guarantors).
		- Defined by the X.509 standard.
- Authentication, Authorisation and Accounting Servers
	- Dedicated servers that handle AAA so that edge clients don't have to.
	- RADIUS (remote authentication dial-in user service) is an example
		- Microsoft's Network Policy Server
		- Unix FreeRADIUS
		- UDP 1812 and 1813 (or UDP 1645 and 1646) 
	- TACACS+ (terminal access controller access control system)
- Directory Services and Access Control Lists
	- Resources are part of an access control list (ACL). Users permissions are baked into their access key. 
- LDAP (Lightweight Directory Access Protocol)
	- Directory (database), Object (record), Attribute (fields)
	- Used to query and update a ITU X.500 Directory.
	- TCP/UDP port 389
	- Distinguished Name is a unique identifier for any resource in a X.500 directory. Consists of attribute=value pairs, which become progressively broader. The first pair is the Relative Distinguished Name as its the most specific.
		- `CN=Administrator,CN=Users,DC=classroom,DC=local`
	- CN - Common Name
	- OU - Organisational Unit
	- O - Organisation
	- L - Locality
- LDAP Secure
	- Basic LDAP is in plaintext by default. 
	- Authentication is referred to as binding.
	- SASL (simple authentication and security layer) - negotiation between client and server to use a security mechanism such as TLS or Kerberos.
	- LDAPS - Port 636/TCP - uses TLS/SSL
	- LDAP Ports 389/TCP&UDP should be blocked by a firewall.
- Auditing and Logging
	- AAA servers log things. 
	- Non-repudiation - users cannot deny that they've accessed something.
	- Log failure-type events to detect intrusion
	- Deciding what to log can be hard

**C.**
**Explain the use of Port Security and NAC**
- Endpoint security provides defense-in-depth. 
- Port Security
	- Mac Filtering
		- Defining which MAC addresses can connect to a port.
	- Flood Guard
		- Defining how many addresses can connect to a port.
		- Flood attacks can be used to perform eavesdropping. By overloading the mapping table or Content Addressable Memory, a switch will start flooding traffic out of all ports, allowing an attacker to sniff all unicast traffic. 
	- ARP Inspection
		- Prevents MAC spoofing and ARP cache poisoning
	- DHCP Snooping
		- Prevents MAC spoofing and rogue DHCP servers
- Port Based Access Control (IEEE 802.1X PNAC)
	- The switch authenticates devices for activating ports.
	- Device requesting access is the **supplicant**.
	- Uses the EAPoL (Extensible Authentication Protocol over LAN) and an AAA server like RADIUS.
	- A health policy defines minimum-security network access control (NAC)
- Admission Control
	- The point at which client devices are granted or denied access
	- Pre-admission - the device must meet the policy
	- Post-admission - the device is polled for continual compliance
	- NAC Policy Enforcer server
- Host Health Checks
	- Posture assessment - health checks
	- NAC solutions use client software called "agents" which can be persistent or non-persistent (dissolvable)
- Remediation
	- Guest Network - VLAN of firewalled subnet (DMZ)
	- Quarantine Network - using a captive portal

**D.**
**Implement Network Device Hardening**
- Defense in depth
- Changing default credentials
- Avoiding common passwords
- Backdoor/default control (disable defaults)
- Disabling unnecessary services (reduce attack surface)
- Disable unused IP ports
- Close unused device ports
- Don't use unsecure protocols like raw HTTP, Telnet, FTP or SNMP
- Change compromised keys
- File hashing using MD5 or SHA to verify file integrity

**E.**
**Explain Patch Management and Vulnerability Scanning Processes**
- Patch management - ensuring software is up to date
- Have a rollback/backup plan
- Hotfixes
- Firmware flashing
- Downgrading / Rollback
- Vulnerability scanning
- Penetration testing
- Honeypots & honeynets (decoy network)