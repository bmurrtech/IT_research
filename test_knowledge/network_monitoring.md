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
