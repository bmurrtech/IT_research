__Question 1
What does tcpdump do? Select all that apply.__
- [ ] Generates packets 
- [ ] Encrypts your packets
- [x] Analyzes packets and provides a textual analysis 
- [x] Captures packets 
- [ ] 
Correct! Tcpdump is a popular, lightweight command line tool for capturing packets and analyzing network traffic.

__Question 2
What does wireshark do differently from tcpdump? Check all that apply.__
- [ ] It can write packet captures to a file.
This should not be selected because both wireshark and tcpdump are capable of writing packet captures to files.
- [x] It understands more application-level protocols. 
- [ ] It can capture packets and analyze them. 
- [x] It has a graphical interface. 
Awesome job! tcpdump is a command line utility, while wireshark has a powerful graphical interface. While tcpdump understands some application-layer protocols, wireshark expands on this with a much larger complement of protocols understood.

__Question 3
What factors should you consider when designing an IDS installation? Check all that apply.__
- [x] Traffic bandwidth 
- [x] Storage capacity 
- [ ] Internet connection speed
- [ ] OS types in use 
Wohoo! It's important to understand the amount of traffic the IDS would be analyzing. This ensures that the IDS system is capable of keeping up with the volume of traffic. Storage capacity is important to consider for logs and packet capture retention reasons.

__Question 4
What is the difference between an Intrusion Detection System and an Intrusion Prevention System?__
- [ ] They are the same thing.
- [ ] An IDS can actively block attack traffic, while an IPS can only alert on detected attack traffic.
- [x] An IDS can alert on detected attack traffic, but an IPS can actively block attack traffic.
- [ ] An IDS can detect malware activity on a network, but an IPS can't
That's exactly right! An IDS only detects intrusions or attacks, while an IPS can make changes to firewall rules to actively drop or block detected attack traffic.

__Question 5
What factors would limit your ability to capture packets? Check all that apply.__
- [x] Network interface not being in promiscuous or monitor mode
- [ ] Anti-malware software
- [ ] Encryption
- [x] Access to the traffic in question
You got it! If your NIC isn't in monitor or promiscuous mode, it'll only capture packets sent by and sent to your host. In order to capture traffic, you need to be able to access the packets. So, being connected to a switch wouldn't allow you to capture other clients' traffic.

__What does tcpdump do?__
- [ ] Generates DDoS attack traffic 
- [x] Performs packet capture and analysis
- [ ] Handles packet injection
- [ ] Brute forces password databases
tcpdump captures and analyzes packets for you, interpreting the binary information contained in the packets and converting it into a human-readable format.

__What can protect your network from DoS attacks?__
- [ ] DHCP Snooping 
- [ ] IP Source Guard 
- [ ] Dynamic ARP Inspection 
- [x] Flood Guard
Flood guards provide protection from DoS attacks by blocking common flood attack traffic when it's detected.

__What occurs after a Network Intrusion Detection System (NIDS) first detects an attack?__
- [x] Triggers alerts 
- [ ] Shuts down
- [ ] Disables network access
- [ ] Blocks traffic
A NIDS only alerts when it detects a potential attack.

__What does a Network Intrusion Prevention System (NIPS) do when it detects an attack?__
- [x] It blocks the traffic.
- [ ] It triggers an alert. 
- [ ] It does nothing. 
- [ ] It attacks back.
An NIPS would make adjustments to firewall rules on the fly, and drop any malicious traffic detected.

__How do you protect against rogue DHCP server attacks?__
- [ ] IP Source Guard 
- [ ] Flood Guard
- [x] DHCP Snooping 
- [ ] Dynamic ARP Inspection 
DHCP snooping prevents rogue DHCP server attacks. It does this by creating a mapping of IP addresses to switch ports and keeping track of authoritative DHCP servers.

__What underlying symmetric encryption cipher does WEP use?__
- [ ] RSA 
- [ ] AES
- [ ] DES 
- [x] RC4 
WEP uses the RC4 stream cipher.

__What traffic would an implicit deny firewall rule block?__
- [x] Everything that is not explicitly permitted or allowed 
- [ ] Nothing unless blocked
- [ ] Outbound traffic only 
- [ ] Inbound traffic only
Implicit deny means that everything is blocked, unless it's explicitly allowed.

__What allows you to take all packets from a specified port, port range, or an entire VLAN and mirror the packets to a specified switch port?__
- [ ] Network hub 
- [ ] Promiscuous Mode
- [x] Port Mirroring 
- [ ] DHCP Snooping 
Port mirroring allows you to capture traffic on a switch port transparently, by sending a copy of traffic on the port to another port of your choosing.

__What kind of attack does IP Source Guard (IPSG) protect against?__
- [ ] Rogue DHCP Server attacks
- [ ] DoS attacks
- [ ] ARP Man-in-the-middle attacks
- [x] IP Spoofing attacks 
IP Source Guard protects against IP spoofing. It does this by dynamically generating ACLs for each switch port, only permitting traffic for the mapped IP address for that port.

__What can be configured to allow secure remote connections to web applications without requiring a VPN?__
- [ ] RC4
- [ ] Web browser 
- [ ] NIDS
- [x] Reverse proxy
A reverse proxy can be used to allow remote access into a network.
