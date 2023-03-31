# Table of Contents
- [Introdution to Cybersecurity](#intro-to-it-security)
- [Types of Malware](#malware)
- [About Network Attacks](#network-attacks)
- [Symetric Encryption](#symmetric-encryption)
- [Asymmetric Cryptography](#asymmetric-cryptography)
- [Cryptography Real-world Usecases](#cryptography-applications)
- [Encryption Generation Linux Lab](#encryption-lab)
- [Generating Hash and Verifying Linux Lab](#hashing-and-hash-verification-lab)
- [Securing Network Architecture](#securing-network-architecture)

# Intro to IT Security

#### The CIA Triad

- **C**onfidentiality
- **I**ntegrity
- **A**vailablity

**Confidentiality** means keeping things hidden, in IT it means keeping the data that you have hidden safely from unwanted eyes.

**Integrity** means keeping our data accurate and untampered with the data that we send or receive should remain the same throughout its entire journey (i.e. SHA256 checksum hash and cryptography secuirty methods).

**Availability** means that the information we have is readily accessible to those people that should have it. This could be many things like being prepared if your data is lost or if your system is down.

#### Terms
- **Risk**: the possibility of suffering a loss and the event of an attack on the system.
- **Vulnerability** flaw in the system that could be exploited to compromise the system. Vulnerabilities can be holes that you may or may not be aware of.
    -  Example: When you're writing a web app and enable a debug account for testing during development, but forget to disable the debug account before launching the app.
    - There's a special type of vulnerability called a **zero-day vulnerability**, or zero-day for short, which is a vulnerability that has _already been exploited before by a hacker_ but the vulnerability is totaly unknown to the developer or vendor.
- **Exploit**: An exploit takes advantage of a vulnerability to run arbitrary code or gain access. It is used to take advantage of a security bug or vulnerability in the software. Attackers will write up exploits for vulnerabilities they find in software to cause harm to the system. 
-  **Threat**: The possibility of danger that could exploit a vulnerability. Threats are just possible attackers sort of like burglars. Not all burglars will attempt to break into your home to steal your most prized possessions, but they could and so they're considered threats.
-  **Hacker**: in the security world, a hacker is someone who attempts to break into or exploit a system. Most of us associate hackers with malicious figures, but there are actually two common types of hackers:
    - *Black Hat Hackers*: who try to get into systems to do something malicious.  
    - *White Hat Hackers* who attempt to find weaknesses in the system, but also alert the owners of those systems so that they can fix it before someone else does something malicious.
- **Attack**: An actual attempt at causing harm to a system.

# Malware 
- **Malware**: Malware is a type of malicious software that can be used to obtain your sensitive information or delete or modify files.
    -  **Virus** the virus attaches itself to some executable code like a program. When the program is running, it touches many files, each of which is now susceptible to being infected with the virus. The virus replicates itself on these files, does the malicious work it's intended to do and repeats this over and over until it spreads as far as it can.
    - **Worms** are similar to viruses, except that instead of having to attach themselves onto something to spread, worms can live on their own and spread through channels like the network. One case of a famous computer worm was the ILoveYou or Love Bug, which spread to millions of Windows machines. This is just one of the many reasons why _you should never open email attachments that you do not recognize_. 
    - **Adware** is one of the most visible forms of malware that you'll encounter. Most of us see it every day. Adware is just software that displays advertisements and collects data. Sometimes we legitimately download adware. That happens when you agree to the terms of service that allows you to use free software in exchange for showing you advertisements. 
    - **Trojan Horse** A Trojan is malware that disguises itself as one thing, but does something else. 
    - __Spyware__ is a type of malware that's meant to spy on you, which could mean monitoring your computer screens, key presses, webcams, and then reporting or streaming all of this information to another party. 
   - A __key logger__ is a common type of spyware that's used to record every keystroke you make. It can capture all of the messages you type, your confidential information, your passwords, and even more.
   - __Ransomware__ is a type of attack that holds your data or system hostage until you pay some ransom. Our case of ransomware was the WannaCry ransomware attack in May, of 2017. The malware took advantage of _a vulnerability in older Windows systems_, infecting hundreds of thousands of machines across the world. Most notably, the attacks shutdown the systems for the National Health Services in England, causing a health-related crisis.
   - __Botnets__ are designed to utilize the power of the internet connected machines to perform some distributed function. Take mining Bitcoin, for example.
    - __A backdoor__ is a way to get into a system if the other methods to get in a system aren't allowed. It's a secret entryway for attackers. Backdoors are most commonly installed after an attacker has gained access to your system and wants to maintain that access, even if you discovered your system has been compromised, you may not realize that a backdoor to your system exists.
    -  A __rootkit__, by its name, is a kit for root, meaning a collection of software or tools that an admin would use. It allows admin level modification to an operating system. A rootkit can be hard to detect because they can hide itself from the system using the system itself--those processes wouldn't show up in Task Manager because it can hide its own presence.
    - A __logic bomb__ is a type of Malware that's intentionally installed after a certain event or time has triggered, it will run the malicious program.
        - There's a popular logic bomb case that happened in 2006, where [an unhappy systems administrator at a bank set off a logic bomb](https://www.independent.co.uk/news/business/news/disgruntled-worker-tried-to-cripple-ubs-in-protest-over-32-000-bonus-481515.html) and brought down accompanies services in an attempt to drop their stock prices. 

#### Antimalware Protection, Malware Removal 
Malware can disrupt, damage, or even destroy a computer. IT teams are often responsible for evaluating and repairing computers that are not running well. If a computer is performing poorly or acting strangely, it might be infected with malware. IT professionals need to know how to isolate, remove, and repair infected devices. This reading covers the steps to take to detect and remove malware.

##### Gather and verify
If you suspect that the computer is infected, you should gather information from the user. It is helpful to note when the symptoms started and if the user has downloaded any unusual files. If the computer has one or more of the following symptoms it may be infected with malware:
- Running slower than normal 
- Restarts on its own multiple times 
- Uses all or a higher than normal amount of memory

After you’ve gathered information, verify that the issues are still occurring by monitoring the computer for a period of time. One way to monitor and verify is to review the activity on the computer’s resource manager where you can see open processes running on a system.

When looking at the resource manager, you might see a program with a name you do not recognize, a program that is using a lot of memory, or both. If you see a suspicious program, you should investigate this application by asking the user if it is familiar to them.  

##### Quarantine malware
Some malware communicates with bad actors or sends out sensitive information. Other malware is designed to take part in a distributed botnet. A botnet is a number of Internet-connected devices, each of which runs one or more bots. Because of malware’s potential ability to communicate with other bad actors, you should quarantine the infected device. 

To quarantine, or separate, the infected device from the rest of the network, you should disconnect from the internet by turning off WiFi and unplugging the ethernet cable. Once the computer is disconnected, the malware can no longer spread to other computers on the network. 

You should also disable any automatic system backup. Some malware can reinfect a computer by using automatic backup, because you can restore the system with files infected by the malware. 

##### Remove malware
Once you have confirmed and isolated the malware on a device, you should attempt to remove the malware from the device. First, run an offline malware scan. This scan helps find and remove the malware while the computer is still disconnected from the local network and internet.

All anti-virus/anti-malware programs rely on threat definition files to identify a virus or malware. These files are often updated automatically, but in the case of an infected computer they may be incomplete or unable to update. In this case, you may need to briefly connect to the internet to confirm that your malware program is fully updated.

The scan should successfully identify, quarantine, and remove the malware on the computer. Once the process is complete, monitor the computer again to confirm that there are no further issues.

To help ensure that a malware infection doesn’t happen again threat definitions should be set to update automatically, and to automatically scan for and quarantine suspected malware. 

After the malware has been removed from the computer, you should turn back on the automatic backup tool and manually create a safe restore point. If the computer needs attention in the future, this new restore point is confirmed safe and clean. 

##### Malware education
One of the most important things an IT professional can do to protect a company and its employees is to educate users about malware. The goal of education is to stop malware from ever gaining access to company systems. Here are a few ways users and IT professionals can protect their computer and the company from malware: 

- Keep the computer and software updated
- Use a non-administrator account whenever possible
- Think twice before clicking links or downloading anything
- Be careful about opening email attachments or images
- Don't trust pop-up windows that ask to download software
- Limit your file-sharing
- Use antivirus software

When all employees are on the lookout for suspicious files, it’s much easier to prevent malware and viruses from taking hold. 

As malware gets more sophisticated, the chance of malware eventually infecting the computers you manage becomes more likely. These steps will help you when and if that time comes. 

##### Key takeaways

Malware can be devastating for a company’s computer network. As an IT support professional, you should be familiar with how to detect, isolate, and remove malware from the computers you manage. 

- An infected device should be isolated from the local network and internet as soon as possible. 
- Antivirus and Anti-Malware software is a key tool for detecting and removing malware.
- Keeping threat protection software updated makes malware removal faster and easier.
- Education is the first and best line of defense against malware.

# Network Attacks
- A __DNS cache poisoning attack__ works by tricking a DNS server into accepting a fake DNS record that will point you to a compromised DNS server. It then feeds you fake DNS addresses when you try to access legitimate websites. Not only that, DNS cache poisoning can spread to other networks too.
  -  Several years ago, there was [a large scale DNS cache poisoning attack in Brazil](https://threatpost.com/major-dns-cache-poisoning-attack-hits-brazilian-isps-110711/75859/). It appeared that attackers managed to poison the DNS cache of some local ISPs by inserting fake DNS records for various popular websites like Google, Gmail or Hotmail. When someone attempted to visit one of those sites, they were served a fake DNS record an were sent to a server that the attacker controlled which hosted a small Java applet. The user would then be tricked into installing the applet which was actually a malicious banking trojan designed to steal banking credentials. This is an example of the real world damage DNS cache poisoning attacks can pose.
- __A man in the middle attack__ is an attack that places the attacker in the middle of two hosts that think they're communicating directly with each other.
    - A common man in the middle attack is a __session hijacking or cookie hijacking__, let's say you log into a website and forget to log out. Now you've already authenticated yourself to the website and generated a session token that grants you access to that website. If someone was performing a session hijacking, they could steal that token and impersonate you on the website (combat using SSL certificate).
    - Another way, a man in the middle attack can be established is a rogue access point attack. A __rogue AP__ _is an access point that is installed on the network without the network administrators knowledge_. Sometimes in corporate environments, someone may plug a router into their corporate network to create a simple wireless network. Innocent enough, right wrong. This can actually be pretty dangerous and could grant unauthorized access to an authorized secure network. Instead of an attacker having to gain access to a network by plugging directly into a network code. They can just stand outside the building and hop onto this wireless network.
    -  An __Evil Twin__. It's similar to the rogue AP example but has a small but important difference. _The premise of an Evil twin attack is for you to connect to a network that is identical to yours._ This identical network is our networks Evil twin and is controlled by our attacker. Once we connect to it, they will be able to monitor our traffic.
- A __denial-of-service or DoS attack__ is an attack that tries to prevent access to a service for legitimate users by overwhelming the network or server. Think about how you normally get on a website. Most major websites are capable of serving millions of users, but for this example, imagine you have a website that could only serve ten users. If someone was performing a denial of service attack, _they would just take up all ten of those spots and legitimate users would have been denied the service because there's no more room for them_.
    - The __ping of death or POD__ is a pretty simple example of a DoS attack. It works by sending a malformed ping to a computer. The ping would be larger in size than what the internet protocol was made to handle. So it results in a buffer overflow. This can cause the system to crash and potentially allow the execution of malicious code.
    - Another example is a __ping flood__ which sends tons of ping packets to a system. More specifically, it sends ICMP echo requests since a ping expects an equal number of ICMP echo replies. If a computer can't keep up with this, then it's prone to being overwhelmed and taken down.
    - Similar to a ping flood is a __SNC flood__ or __half-open attacks__ Remember that to make a TCP connection, a client sends a SYN packet to a server, it wants to connect to next, the server sends back a SYN-ACK message. Then the client sends an ACK message. In a SYN flood, the server is being bombarded with these sim packets. The server is sending back SYN-ACK packets, but the attacker is not sending ACK messages. _This means that the connection stays open and is taking up the server's resources. Other users will be unable to connect to the server_, which is a big problem, since the TCP connection is half open _we also refer to SYN floods as_ __half-open attacks__.

    [syn_flood](https://i.imgur.com/yvyz6Ny.png)

    - What if Attackers could utilize multiple machines? A _DoS attack using multiple systems_ is called a __distributed denial of service attack or DDoS__. It would require a large volume of systems to carry out an attack. And they're usually helped by botnet attackers, in that scenario, they can gain access to large volumes of machines to perform an attack.
       - In October of 2016 a DDoS attack occurred when the DNS service provider DYN was the target of a DDoS, fake DNS look up requests along with SYN floods that botnets were performing overloaded their system. DYN handled the DNS for major websites like Reddit, Git hub, Twitter, etc. So once it went down, it also took down its customers, making those services inaccessible.

For more information about DDoS attacks how to protect against them, see:

- [How to Stop DDoS Attacks: Prevention & Response](https://www.esecurityplanet.com/networks/how-to-stop-ddos-attacks-tips-for-fighting-ddos-attacks/) - Article from eSecurity Planet about types of DDoS attacks, motivations for launching DDoS attacks, and how to prevent them.
- [What is a DDOS Attack & How to Protect Your Site Against One](https://aws.amazon.com/shield/ddos-attack-protection/) - AWS article about DDoS attacks and protection techniques.
- [DDoS Protection, Mitigation, and Defense: 8 Essential Tips](https://www.indusface.com/blog/ddos-protection-mitigation-and-defense-8-essential-tips/) - A list of eight best practice tips to prevent DDoS attacks.

# Other Attacks

#### Client-side Attacks
- An __injection attack__: A common security exploit that can occur in software development and runs rampant on the web is the possibility for an attacker to inject malicious code. We refer to these types of attacks as injection attacks.
    - Example: You keep your car running by putting gas in it. Now consider someone who wants to do something malicious to that car. That person could _inject your gas tank with some bad mojo that will mess up the engine_. So how do you fight against that? A hypothetical method to prevent this is _adding a mechanism to your car that only accepts gasoline and no other liquids_. Injection attacks and websites work the exact same way. _Injection attacks can be mitigated with good software development principles like validating input and sanitizing data._
    - __Cross-site scripting or XSS attacks__ are a type of injection attack where the attacker can insert malicious code and target the user of the service. XSS attacks are a common method to achieve a __session hijacking__. _It would be as simple as embedding a malicious script in a website and the user unknowingly executes the scripts in their browser._
    - __SQL injection attack__ targets a website, not users, by checking if the website is using a SQL database. Attackers can potentially run SQL commands that allow them to delete website data, copy it and run other malicious commands.

#### Password Attacks
- A common password attack is __a brute force attack__ which just continuously tries different combinations of characters and letters until it gets access. Since this attack requires testing a lot of combinations of passwords, it usually it takes a while to do this.
    - A __CAPTCHA__ prevents the brute force password attempts of a computer running an automated system to brute force guess passwords and gain access to your online accounts.
- A __dictionary attack__ doesn't test out brute-force combinations like abc1 or ABC1. Instead, it tries out words that are commonly used and passwords like password, monkey football.
    - The best way to prevent a password attack is to utilize strong passwords. Don't include real words you would find in a dictionary and make sure to _use a mix of capitals, letters, and symbols._ For example, it would take a typical password cracker application about one minute to crack a password like a "sandwich."

#### Social Engineering (Deceptive Acttacks)
- Social engineering is a con game where attackers use deceptive techniques to gain access to personal information. They then try to have a user execute something and basically scam a victim into doing that thing. A popular type of social engineering attack is a phishing attack. Phishing usually occurs when a malicious email is sent to a victim disguised as something legitimate.
    - One common __phishing attack__ is an email saying your bank account has been compromised. It then gives you a link to click on to reset your password. When you go to the link, it looks like your bank's website, but it's actually a fake website so your tricked into entering your current password and credentials in order to reset your current password.
    -  __Spear phishing__ specifically targets individual or group. The fake emails may contain some personal information like your name or the names of friends or family, so they seem more trustworthy. 
    - __Email spooffing__ Spoofing is when a source is masquerading around as something else. This is what happens when you receive an email with a misleading sender address. Imagine if you open the email you thought was from your friend Brian. He sent you a link to a funny video to watch, you click it, and now you suddenly have malware on you computer.
    - __Baiting__ is used to entice the victim to do something. For example, an attacker could just leave a USB drive somewhere in hopes that someone out there will plug it into their machine to see what's on it. But they've just installed malware on their machine without even knowing it.
    - __Tailgating__ which is essentially gaining access into a restricted area or building following a real employee in. In most corporate environments, building access is restricted through the use of a key card or some other entry method. A tailgate or could use social engineering tactics to trick an employee into thinking that they're there for a legitimate reason, like doing maintenance on the building or delivering packages. Once the tailgater is in, they have physical access to your corporate assets.

#### Types of Email Attacks

__Phishing__: A cybercriminal may use email and text messaging to “fish” or phish for victims that will take the cybercriminal’s bait. One basic type of phishing bait may include a convincing story to trick the victim into replying to the email with personal or sensitive information. Another common phishing scam includes using “clickbait” links. These phishing messages entice victims to click on a link by using bait such as popular pet videos, gossip, news scandals, opportunities to win money or prizes, lewd images or videos, etc. If the recipient clicks on the link, they become victim to the next phase of the malicious attack, which could be some type of forced download of malware, ransomware, viruses, keyloggers, trackers, and more.

__Spoofing__: Cybercriminals use this technique to alter the header on phishing emails in order to appear to originate  from a legitimate business or reputable person. For example, a spoofed email might use a fake header that appears to be from a bank. The body of the email might ask the victim to click a given link to log into their bank account to fix a “problem”. The link leads to the cybercriminal’s fake website that looks identical to the bank website and exists only to collect the bank login credentials from victims. The fake website might even give the victim an error message and forward them to the real bank to try to login again. This technique keeps the victim from immediately recognizing they have been scammed because the second login attempt on the real website is usually successful. 

__Spear phishing__: A cybercriminal might use details about a victim’s life to win the victim’s trust. For example, the criminal might first purchase data from a social media platform that provides personal information about the platform’s users. The cybercriminal then uses this data to target or “spear” specific individuals. The cybercriminal could select a name from a user’s friends list and create a spoofed email that appears to be from that friend. The spoofed email may say something as simple as, “look at this photo I found of you online!” The email may also include an attachment or a clickbait link that leads to the next stage of the attack.   

__Whaling__: When a cybercriminal wants to spear phish a big target or “whale,” they will spend more time and effort deceiving the victim. A whale target is typically someone in a position of power, such as a wealthy and/or famous person, an executive of a company, or a high-level government employee. The whale is targeted because of the likelihood that they have the ability to pay high ransomware fees, trade valuable information or confidential data, or may be vulnerable to blackmail. 

__Vishing__: Cybercriminals use Voice over IP (VoIP) to make phone calls or leave voice messages pretending to be from reputable companies in order to trick victims into revealing personal information, such as banking details and credit card numbers. Although telephone scams have been running for decades, vishing with VoIP makes it easier for cybercriminals to hide their true identity. VoIP calls are significantly more difficult to trace than landline calls.

#### Targeted and in-person Deceptive Attacks 

__Shoulder surfing__: This malicious attack might have a specific victim or organization as their target. Shoulder surfing happens _when a person looks over a victim’s shoulder to watch them enter login credentials, credit card numbers, or other sensitive information_. For example, a temporary contractor for an organization may look over the shoulder of an employee to watch the employee enter their login info. The temporary employee’s goal might be to steal credentials in order to illegally obtain confidential company data or plant ransomware. 

__Tailgating__: This in-person attack is a form of social engineering in which an unauthorized party gains physical access to a restricted area by simply following a person or group of persons who have authorized access. For example, a criminal wanting to gain physical access to an organization’s computer network might dress in business clothing and follow a group of coworkers coming back from lunch. One member of the group may use their key card to open the door, then hold the door open for the rest of the group, as well as the criminal who is dressed and behaving as though they belong in the building. The criminal may even have a fake ID card to show anyone who questions them.   

__Impersonation__: This attack might happen over email, text messaging, or a phone call. The attacker impersonates someone who should have access to an organization’s computer network. For example, the attacker might call the IT Support team to request help with a password reset. Alternatively, the attacker might pretend to be a member of an organization’s IT Support team. They may call an employee to ask them to change some settings on their computer to fix a fake problem. These changes are intended to open a door for the cybercriminal to gain access to the organization’s network. 

__Dumpster Diving__: This in-person attack involves the attacker literally digging through the trash of an individual or organization to hunt for confidential information, like financial or customer information. Shredding all confidential documents is an easy way to prevent this type of attack. 

__Evil twin__: This type of attack involves the cybercriminal installing Wi-Fi routers that appear to belong to an organization's network. These Wi-Fi access points may not require a password and might appear to offer a stronger signal than the real Wi-Fi router. When victims connect to the fake Wi-Fi access point, the cybercriminal gains access to the victim’s wireless transmissions, which can include login credentials and other sensitive information.

### Security Terms Glossary

- Adware: Software that displays advertisements and collects data
- Attack: An actual attempt at causing harm to a system
- Availability: Means that the information we have is readily accessible to those people that should have it
- Backdoor: A way to get into a system if the other methods to get in a system aren't allowed, it's a secret entryway for attackers
- Baiting: An attack that happens through actual physical contact, enticing a victim to do something
- Botnet: A collection of one or more Bots
- Bots: Machines compromised by malware that are utilized to perform tasks centrally controlled by an attacker
- Brute force attacks: A common password attack which consists of just continuously trying different combinations of characters and letters until one gets access
- CIA Triad: Confidentiality, integrity, and availability. Three key principles of a guiding model for designing information security policies
- Confidentiality: Keeping things hidden
- Cross-site scripting (XSS): A type of injection attack where the attacker can insert malicious code and target the user of the service
- Denial-of-Service (DoS) attack: An attack that tries to prevent access to a service for legitimate users by overwhelming the network or server
- Dictionary attack: A type of password attack that tries out words that are commonly used in passwords, like password, monkey, football
- Distributed Denial-of-Service (DDoS) attack: A DoS attack using multiple systems
- DNS Cache Poisoning Attack: It works by tricking a DNS server into accepting a fake DNS record that will point you to a compromised DNS server
- Evil twin: The premise of an evil twin attack is for you to connect to a network that is identical to yours but that is controlled by an attacker. Once connected to it, they will be able to monitor your traffic
- Exploit: Software that is used to take advantage of a security bug or vulnerability
- Hacker: Someone who attempts to break into or exploit a system
- Half-open attacks: A way to refer to SYN floods
- Injection attacks: A common security exploit that can occur in software development and runs rampant on the web, where an attacker injects malicious code
- Integrity: Means keeping our data accurate and untampered with
- Keylogger: A common type of spyware that's used to record every keystroke you make
- Logic bomb: A type of Malware that's intentionally installed
- Malware: A type of malicious software that can be used to obtain your sensitive information or delete or modify files
- Meddler in the middle (formerly known as Man in the Middle): An attack that places the attacker in the middle of two hosts that think they're communicating directly with each other
- Password attacks: Utilize software like password crackers that try and guess your password
- Phishing attack: It usually occurs when a malicious email is sent to a victim disguised as something legitimate
- Ping flood: It sends tons of ping packets to a system. If a computer can't keep up with this, then it's prone to being overwhelmed and taken down
- Ransomware: A type of attack that holds your data or system hostage until you pay some sort of ransom
- Risk: The possibility of suffering a loss in the event of an attack on the system
- Rogue Access Point (AP) Attack: An access point that is installed on the network without the network administrator's knowledge
- Rootkit: A collection of software or tools that an admin would use
- Screen lock: A security feature that helps prevent unwanted access by creating an action you have to do to gain entry
- Session hijacking (cookie hijacking): A common meddler in the middle attack
- Social engineering: An attack method that relies heavily on interactions with humans instead of computers
- Spear phishing: Phishing that targets individual or group - the fake emails may contain some personal information like your name, or the names of friends or family
- Spoofing: When a source is masquerading around as something else
- Spyware: The type of malware that's meant to spy on you
- SQL Injection Attack: An attack that targets the entire website if the website is using a SQL database
- SYN flood: The server is bombarded with SYN packets
- Tailgating: Gaining access into a restricted area or building by following a real employee in
- Threat: The possibility of danger that could exploit a vulnerability
- Trojan: Malware that disguises itself as one thing but does something else
- Viruses: The best known type of malware
- Vulnerability: A flaw in the system that could be exploited to compromise the system
- Worms: They are similar to viruses except that instead of having to attach themselves onto something to spread, worms can live on their own and spread through channels like the network
- 0-Day Vulnerability (Zero Day): A vulnerability that is not known to the software developer or vendor, but is known to an attacker

# Symmetric Encryption
Encryption is the act of taking a message called plaintext and applying an operation to it called a cipher so that you receive a garbled, unreadable message as the output called ciphertext. The reverse process, taking the garbled output and transforming it back into the readable plaintext, is called decryption.

History of Cryptology

One of the first practical asymmetric cryptography systems to be developed is RSA. Named for the initials of the three co-inventors Ron Rivest, Adi Shamir, and Leonard Alderman. This crypto system was patented in 1983 and was released to the public domain by RSA security in the year 2000. The RSA system specifies mechanisms for generation and distribution of keys, along with encryption and decryption operation using these keys.

DES key as an example, 64 bits long minus the eight parity bits gives us a key length of 56 bits. This means that there are a maximum of 2^56 power or 72 quadrillion possible keys. That seems like a ton of keys and back in the 1970s, it was. But as technology advanced and computers got faster and more efficient, 64 bit keys quickly proved to be too small. What were once only theoretical attacks on the key size became reality in 1998 when the EFF, _Electronic Frontier Foundation decrypted a DES encrypted message_ __in only 56 hours.__

RC4 supports key sizes from 40 bits to 2048 bits, so the weakness isn't due to brute force attacks, but there are lots of examples showing RC4 being broken. A recent example of RC4 being broken is the RC4 normal more attack. This attack was able to recover an authentication cookie from a TLS encrypted connection __in just 52 hours__. It was also supported in SSL and TLS until 2015 when RC4 was dropped in all versions of TLS because of inherent weaknesses. For this reason, [most major web browsers have dropped support for RC4 entirely in 2015](https://www.rc4nomore.com/). The preferred secure configuration is __TLS 1.2 with AES GCM__, a specific mode of operation for the AES block cipher that essentially turns it into a stream cipher.

In 2001, adopted AES, Advanced Encryption Standard after an international competition. AES is also the first and only public cipher that's approved for use with top secret information by the United States National Security Agency. Because of the large key size, brute-force attacks on AES are only theoretical right now because the computing power required or time required using modern technology exceeds anything feasible today; however, __quantum computing__ may change the encryption game entirely. For example: _the NSA has expressed concern about EC encryption being potentially vulnerable to quantum computing attacks, as quantum computing technology continues to evolve and mature_.

__It's important to call out that the security of the system__ is dependent on choosing a random seed value that's incorporated into the signing process. _If this value is leaked_ or if it can be inferred, if the prime number isn't truly random, then it's possible for _an attacker to recover the private key_.

#### The Sony Playstation 3 Cispher Hack
[This actually happened in 2010 to Sony with their PlayStation 3 Game Console](https://nakedsecurity.sophos.com/2012/10/25/sony-ps3-hacked-for-good-master-keys-revealed/). It turns out they weren't ensuring this randomized value was changed for every signature. This resulted in a hacker group called Fail0verflow being able to recover the private key that Sony used to sign software for their platform. This allowed matters to write and sign custom software that was allowed to run on the otherwise very lockdown Console platform. This resulted in [game piracy becoming a problem for Sony](https://www.theguardian.com/technology/gamesblog/2011/jan/07/playstation-3-hack-ps3) as this facilitated the illicit copying and distribution of games which caused significant losses in sales. 

__Cryptography__ is a method of protecting information and communications using codes so that only the intended person can read and process them. Cryptography has mainly stemmed from the manual encoding of messages and information using a formula to convert any given letter or number to a new value. Encryption is the process that encodes the data making it harder to decode. The goal of encrypting data is to keep internal information secure. 

__Cryptanalysis__ uses technology to improve the process of encrypting data and innovates new ways to defend companies from attacks that can access and decode their data.  

### Types of Cryptanalysis Attack
There are several types of attacks that hackers or security professionals employ to get data from a network using cryptanalysis. The attacks all use a different way into the network to gain encoded information and translate it from the encoded form into information that can be easily read. 

The following are the most common cryptanalytic attacks:

__Known-Plaintext Analysis (KPA)__ requires access to some or all of the plaintext of the encrypted information. The plaintext is not computationally tagged, specially formatted, or written in code. The analyst's goal is to examine the known plaintext to determine the key used to encrypt the message. Then they use the  key to decrypt the encoded information. 

__Chosen-Plaintext Analysis (CPA)__ requires that the attacker knows the encryption algorithm or has access to the device used to do the encryption. The analyst can encrypt one block of chosen plaintext with the targeted algorithm to get information about the key. Once the analyst obtains the key, they can decrypt and use sensitive information. 

__Ciphertext-Only Analysis (COA)__ requires access to one or more encrypted messages. No information is needed about the plaintext data, the algorithm, or data about the cryptographic key. Intelligence agencies face this challenge when intercepting encrypted communications with no key.

__Adaptive Chosen-Plaintext Attack (ACPA)__ is similar to a chosen-plaintext attack. Unlike a CPA, it can use smaller lines of plaintext to receive its encrypted ciphertext and then crack the encryption code using the ciphertext.  

__Meddler-in-the-Middle (MITM)__ uses cryptanalysts to insert a meddler between two communication devices or applications to exchange their keys for secure communication. The meddler replies as the user and then performs a key exchange with each party. The users or systems think they communicate with each other, not the meddler. These attacks allow the meddler to obtain login credentials and other sensitive information.

### Results from a Cryptanalysis Attack
There are various results of a cryptanalysis attack. Some attacks result in a total break in the encryption and some result in more information that can help the attacker cause other damage or get closer to the goal of a total break.    

Common results from a cryptanalysis attack include:

- __Instance deduction__ where the attacker discovers additional plain or cipher text. While the key isn’t found to break the code, the additional plaintext or ciphertext can be used to cause problems or continue attacks. 
- __Information deduction__ where the attacker obtains some information about plain or cipher text not previously known. The additional information can lead to more information about the encryption key. 
- __Distinguishing algorithm__ where the attacker can distinguish the encryption algorithm from a random alteration. This information reveals clues about the encryption algorithm and can lead to more significant breaks.
- __Global deduction__ where the attacker finds an algorithm that is functionally equivalent to the one used in the key. This algorithm is then used to decrypt all information and messages. 
- __Total break__ where the attacker can gain the entire key. With the entire key, the attacker can decrypt all messages and information.

# Asymmetric Cryptography

- __Asymmetric Encryption__ generates _different_ keys are used to encrypt and decrypt. In asymmetric encryption, algorithm is chosen as a key exchange mechanism or cipher. What this means is that, the symmetric encryption key or shared secret, is transmitted securely to the other party using asymmetric encryption to keep the shared secret secure in transit. Once the shared secret is received, data can be sent quickly and efficiently and securely using an asymmetric encryption cipher.
- __MACs or Message Authentication Codes__ Not to be confused with Media Access Control or MAC addresses. A MAC is a bit of information that allows authentication of a received message, ensuring that the message came from the alleged sender and not a third party masquerading as them. It also ensures that the message wasn't modified in some way in order to provide data integrity.
- __HMAC or a keyed hash message authentication code__ uses a cryptographic hash function along with a secret key to generate a MAC. Any cryptographic hash functions can be used like SHA-1 or MD5.
- __CBC-MACs or Cipher-Based Message Authentication Codes__ CBC-MAC is a mechanism for building MACs using block ciphers. This works by taking a message and encrypting it using a block cipher operating in CBC mode. It is similar to HMAC, but instead of using a hashing function to produce a digest, a _symmetric_ cipher with a shared key is used to encrypt the message and the resulting output is used as the MAC.

### Hashing

Hashing or a hash function is a type of function or operation that takes in an arbitrary data input and maps it to an output of a fixed size called a hash or a digest. What this means exactly is that you feed in any amount of data into a hash function and the resulting output will always be the same size, but the output should be unique to the input, such that two different inputs should never yield the same output.

Hashing can also be used to identify duplicate datasets and databases or archives to speed up searching of tables or to remove duplicate data to save space.

Cryptographic hashing is distinctly different from encryption because cryptographic hash functions should be one-directional. The ideal cryptographic hash function should be deterministic, meaning that the same input value should always return the same hash value. The function should be quick to compute and be efficient, it should be infeasible to reverse the function and recover the plain text from the hash digest. A small change in the input should result in a change in the output so that there is no correlation between the change in the input and the resulting change in the output. Finally, the function should not allow for __hash collisions__, _meaning two different inputs mapping to the same output._

```
"Hello World" | [hash function] | E49AOOFF
INPUT: "hello world" | [hash function] | FF1832AE
```
Real Example:

```bash
$ echo 'Hello World' | md5sum | e59ff97941044f85df5297e1c302d260
$ echo 'hello worldl | md5sum | 6f5902ac237024bddOc176cb93063dc4
```
Note that the hash is different for each example which indicates a divergence.

__MD5__ is a popular and widely used hash function designed in the early 1990s as a cryptographic hashing function.
- It operates on a 512 bit blocks and generates 128 bit hash digest. While MD5 was published in 1992, _a design flaw was discovered in 1996__, and in 2004, it was discovered that MD5 is susceptible to __hash collisions__, _allowing for a bad actor to craft a malicious file that can generate the same MD5 digest as another different legitimate file_.
- Shortly after this flaw was discovered, _security researchers were able to generate two different files that have __matching__ MD5 hash digest_. In 2008, security researchers took this a step further and demonstrated the ability to create a fake SSL certificate that validated due to an MD5 hash collision.
- In 2012, this hash collision was used for nefarious purposes in the Flame malware, which used the forage Microsoft digital certificate to sign their malware, which resulted in the malware appearing to be from legitimate software that came from Microsoft.
- When design flaws were discovered in MD5, it was recommended to use SHA1 as a replacement.

__SHA1__ is part of the Secure Hash Algorithm suite of functions designed by the NSA and published in 1995. SHA1 is another widely used cryptographic hashing functions _used in popular protocols like TLS/SSL, PGP/SSH, and IPSec_. SHA1 is also used in version control systems like Git, which uses hashes to identify revisions and _ensure data integrity by detecting corruption or tampering_. However, _significant computational could theoreticaly cause a hash collision_.
- For example: A full collisions using these methods requires significant computing power. One such attack was _estimated to require $2.77 million in Cloud computing CPU resources_.
- However, due to increasing computational power of modern CPUs and GPUs,(especially in the space of GPU accelerated computations and Cloud resources), a full collision with _this attack method was estimated to be feasible using CPU and GPU Cloud computing for approximately $75K to $120,000_, much cheaper than previous attacks.
- [In early 2017, using significant CPU and GPU resources, two unique PDF files were created that result in the same SHA1 hash](https://shattered.io/). The estimated processing power required to do this was described as equivalent of 6,500 years of a single CPU and 110 years of a single GPU computing non-stop.
A __MIC (Message Integrity Check)__ is essentially a hash digest of the message in question.
- You can think of it as a checksum for the message, ensuring that the contents of the message weren't modified in transit.
- But this is distinctly different from a MAC that we talked about earlier. It doesn't use secret keys, which means the message isn't authenticated.
- Therefore, _there's nothing stopping an attacker from altering the message_, recomputing the checksum, and modifying the MIC attached to the message.
- You can think of MICs as protecting against accidental corruption or loss, but not protecting against tampering or malicious actions.

### Hashing Rainbow Tables and How to Defend Against It
[rainbow_table](https://i.imgur.com/uvn7F29.png)

A __rainbow table__ is just _a pre computed table of all possible password values, and their corresponding hashes_. These tables are used by bad actors to help speed up the process of recovering passwords from stolen password hashes. 
 - The idea behind rainbow table attacks is to trade computational power for disk space, by pre computing the hashes and storing them in a table.
 - An attacker can determine what the corresponding password is for a given hash, by just looking up the hash in their rainbow table. This is unlike a brute force attack, where the hash is computed for each guess attempt. It's possible to download rainbow tables from the internet for popular password lists and hashing functions. This further reduces the need for computational resources, requiring large amounts of storage space to keep all the password and hash data.

 A __password salt__ _is additional randomized data that's added into the hashing function to generate a hash that's unique to the password and salt combination_. Here's how it works: 
 - A randomly chosen large salt is concatenated or attacked onto the end of the password. The combination of salt and password is then run through the hashing function to generate the hash, which is then stored alongside the salt.
 - What this means now for an attacker, is _that they'd have to compute a rainbow table for each possible salt value_. If a large salt is used, the computational and storage requirements to generate useful rainbow tables becomes almost infeasible. Early UNIX systems used a 12 bit salt, which amounts to a total of 4096 possible salts.
 - An attacker would have to generate hashes for every password in their database 4096 times over. _Modern systems like Linux, BSD and Solaris use a 128 bit salt. That means, there are 2 to the 128th power possible salt values, which is over 340 undecillion, that's 340 with 36 zeros following._
 - Clearly, 128 bit salt raises the bar high enough that a rainbow table attack wouldn't be possible in any realistic timeframe. 

### How to Check Hashes

[VirusTotal](https://www.virustotal.com/gui/home/upload) is a free online tool that can check the file hash. However, you can use your computer's CLI to check the hash, too.

#### [PowerShell](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/get-filehash?view=powershell-7.3 ):

```powershell
Get-FileHash -Path [C:\path\to\file.iso] -Algorithm [hash_type] | Format-List
```
> Note: You can specify which Hash to use by adding a -Algorithm [hash_name]. Hash names available are:
> - MD5
> - SHA1
> - SHA256
> - SHA384
> - MACTripleDES
> - RIPMD160

For example:

```ps
Get-FileHash -path C:\users\user_name\downloads\proxmox-ve_7.3-1.iso -algorithm sha256 | format-list
```

Output Example:
```
Algorithm : SHA256
Hash      : 539A2ACD3A921F76F08C759058A12C7FA97E1E1E4956AD6389F25FD4F3C3085B
Path      : C:\users\bmurray\downloads\proxmox-ve_7.3-1.iso
```

#### MacOS (Terminal):

```
[hash_name] /path/to/file.iso
```
Hashnames include:
- md5
- shasum
- shasum -1
- shasum -256

#### Linux Examples

```
md5sum /path/to/file.iso
sha1sum /path/to/file.iso
sha256sum /path/to/file.iso
```

# Cryptography Applications

A __PKI (Public Key Infrastructure)__ is a system that defines the creation, storage, and distribution of digital certificates. A digital certificate is a file that proves that an entity owns a certain public key. A certificate contains information about the public key, the entity it belongs to, and a digital signature from another party that has verified this information.

The entity that is responsible for storing, issuing, and signing certificates is referred to as __CA, or Certificate Authority__. It's a crucial component of a PKI system. There's also an __RA or Registration Authority__ that's _responsible for verifying the identities of any entities requesting certificates to be signed and stored with the CA_. This role is usually lumped together with the CA.

_A central repository is needed to securely store and index keys, and a certificate management system of some sort, makes managing access to storage certificates and issuance of certificates easier_. There were a few different types of certificates that have different applications or uses. The one you're probably most familiar with is SSL or TLS server certificate. This is a certificate that a web server presents to a client as part of the initial secure setup of an SSL/TLS connection.
In some cases, a __wildcard certificate__ can be issued where _the host name is replaced with an asterix denoting validity for all host names within a domain_. It's also possible for a server to use what's called a __self-signed certificate__. You may have guessed from the name, this certificate _has been signed by the same entity that issued the certificate_.

Another certificate type is an __SSL/TLS client certificate__. This is an optional component of SSL/TLS connections and is less commonly seen than server certificates. As the name implies, these are certificates that are bound to clients and are used to authenticate the client to the server, allowing access control to an SSL/TLS service.
- These are different from server certificates, in that the client certificates aren't issued by a public CA. Usually, the service operator would have their own internal CA which issues and manages client certificates for their service.

There are also __code signing certificates__ which are used for signing executable programs. This allows users of the signed applications to verify the signatures and ensure that the application was not tampered with. It also lets them verify that the application came from the software author and is not a malicious twin.

_A certificate that has no authority as a CA_ is referred to as an __end-entity or leaf certificate__. Similar to a leaf on a tree, it's the end of the tree structure and can be considered the opposite of the roots.
 - In order to bootstrap this chain of trust, you have to trust a root CA certificate, otherwise, the whole chain is untrusted. This is done by distributing root CA certificates via alternative channels. Each major OS vendor ships a large number of trusted root CA certificates with their OS. They typically have their own programs to facilitate distribution of root CA certificates.

 ### Certificates

#### X.509 Standard
The [__X.509 standard__](https://www.ietf.org/rfc/rfc5280.txt) is _what defines the format of digital certificates_. It also defines a certificate revocation list, or CRL, which is a means to distribute a list of certificates that are no longer valid. The fields defined in an X.509 certificate are:
 - __The Version__ what version of the X.509 standard the certificate adheres to
 - The __Serial Number__  a unique identifier for the certificate assigned by the CA, which allows the CA to manage and identify individual certificates. 
 - __Certificates signature algorithm__ indicates what public key algorithm is used for the public key and what hashing algorithm is used to sign the certificate.
 - __Issuer name__ contains information about the authority that sign the certificate.
 - __Validity__ contains two subfields, Not Before and Not After, which define the dates when the certificate is valid for.
 - __Subject__ contains identifying information about the entity the certificate was issued to.
 - __Subject public key info__. These two subfields define the algorithm of the public key along with the public key itself.
 - __Certificates signature algorithm__ same as the subject public key and field, these two fields must match.
 - __Certificate signature value__, the digital signature data itself.

#### Web of Trust
Alternative to the centralized PKI model of establishing trust and binding identities is what's called the __web of trust__.

- A __web of trust__ is where individuals, instead of certificate authorities, sign other individuals public keys.

[web_trust](https://i.imgur.com/ppxAYgc.png)

- Before an individual signs a key, they should first verify the person's identity through an agreed upon mechanism, usually by checking some form of identification, driver's license, passport, etc.
- Once they've determined the person is who they claim to be, signing their public key is basically vouching for this person. You're saying that you trust that this public key belongs to this individual.
- In the future when one of these participants in the initial key signing party establishes trust with a new member. The web of trust extends to include this new member and other individuals they also trust. This allows separate webs of trust to be bridged by individuals and allows the network of trust to grow.

### HTTP vs HTTPS
#### Port 80 - HTTP (Hypertext Transfer Protocol)
...is the way data is sent and received over a network
Example: i.e. http://website.com is a client computer browser request to the server hosting the website to respond by providing the information/data from the server to the client machine via HTTP.
HTTP requests/responses are sent across the internet as plaintext; therefore, any data exchanged is viewable to anyone monitoring the connection.

HTTP is a security risk because:
- Essentially, a malicious actor can just read the text in the request or the response and know exactly what information someone is asking for, sending, or receiving, and even manipulate the communication.
- For example: An attacker could gain control of a Linux distribution’s website and modify the hashes that appear on it, or an attacker could perform a man-in-the-middle attack and modify the web page in transit if you were accessing the website via HTTP instead of encrypted HTTPS.
- For example: Linux Mint’s website was hacked, and a modified ISO was put up for download that included a backdoor. While the problem was fixed quickly, it demonstrates the importance of checking Linux ISO files you download.

#### Port 443 - HTTPS (Hypertext Transfer Protocol Secure)
- a.k.a. HTTP over TLS or SSL (Security Socket Layer)
- HTTPS prevents Man-in-the-middle attacks, DNS hijacking, and domain spoofing through cryptographic keys.
- What makes HTTPS secure is the cryptographic encryption (public key/hash and a private key/hash) of a CA (Certificate Authority) which cryptographically signs the exchange of data.
- When a client machine wants to connect to the HTTPS web server through a browser, each machine must verify identity. This is accomplished by the two devices using the public and private key to agree on new keys, called session keys.
- Think of the private keys as an ID card.
- In addition, any communication between client and server is encrypted (i.e. credit card/payment information cannot be stolen by anyone monitoring the connection because it is encrypted).

### TCB vs UDP Protocol
| TCP vs | UDP Protocol |
| ----------- | ----------- |
| Secure  | Unsecure  |
| Slow  | Fast  |
| Guaranteed Transmission  | No Guaranteed Transmission  |
| Critical Application Use  | Real-team Application Use  |
| Flow Control  | None  |
| Advance Error Checks  | Basic Error Checks (Checksum)  |
| DNS, HTTPS, FTP. SMTP, ect.  | DNS, DHCP, SNMP, TFTP, etc.  |
| Connection-oriented (must have a connection between client &] server before data transfer)  | Connectionless (data transfer happens w/o connection between client and server)  |

### Securing Network traffic

What if our application doesn't utilize encryption or what if we want to provide remote access to internal resources too sensitive to expose directly to the internet? We use a VPN or virtual private network solution.

A __VPN (Vitrual Private Network)__ is a mechanism that allows you to remotely connect a host or network to an internal private network, passing the data over a public channel like the internet.
- You can think of this as a sort of encrypted tunnel where all of our remote systems network traffic would flow, transparently channeling our packets via the tunnel through the remote private network.
- A VPN can also be point to point where two gateways are connected via a VPN, essentially bridging two private networks through an encrypted tunnel.
- SSL, TLS is also used in some VPN implementations to secure network traffic as opposed to individual sessions or connections. An example of this is [__OpenVPN__](https://openvpn.net/index.php/open-source.html) which uses the open SSL library to handle key exchange and encryption of data along with control channels. This also enables OpenVPN to make use of all the ciphers implemented by the open SSL library.
- It should be called out that OpenVPN doesn't implement user name password authentication directly, it uses modules to plug into authentication systems. OpenVPN can operate over either TCP or UDP, typically over ports 1194.
- It supports pushing network configuration options from the server to a client and it supports two interfaces for networking. It can either rely on a layer 3 IP tunnel or a layer 2 ethernet tap. The ethernet tap is more flexible, allowing it to carry a wider range of traffic. From the security perspective, OpenVPN supports up to 256 bit encryption through the OpenSSL library. 

[ipsec](https://i.imgur.com/c1MJJx9.png)

__IPsec__ works by encrypting an IP packet and encapsulating the encrypted packet inside an IPsec packet. This encrypted packet then gets routed to the VPN end-point where the packet is de-encapsulated and decrypted then sent to the final destination. IPsec supports two modes of operations, transport mode and tunnel mode.
- While not a VPN solution itself, [__L2TP or layer two tunneling protocol__](https://tools.ietf.org/html/rfc3193) is typically used to support VPNs. A common implementation of L2TP is in conjunction with IPsec when data confidentiality is needed. Since L2TP doesn't provide encryption itself, it's a simple tunneling protocol that allows encapsulation of different protocols or traffic over a network that may not support the type of traffic being sent. L2TP can also just segregate and manage the traffic. ISPs will use L2TP to deliver network access to a customer's end point.
- For example, the combination of L2TP and IPsec is referred to as L2TP IPsec and was officially standardized in IETF RFC 3193.
- An important distinction to make in this setup is the difference between the tunnel and the secure channel. The tunnel is provided by L2TP which permits the passing of unmodified packets from one network to another. The secure channel, on the other hand, is provided by IPsec which provides confidentiality, integrity and authentication of data being passed.

### Cryptographic Hardware
[tmp](https://i.imgur.com/ISGmyih.png)

__TPM (trusted platform module)__ This is a hardware device that's typically integrated into the hardware of a computer that's a dedicated crypto processor.
-    TPMs offer:
  - secure generation of keys,
  - random number generation, remote attestation,
  - and data binding and seiling.
- A TPM has unique secret RSA key burned into the hardware at the time of manufacturer, which allows the TPM to perform things like hardware authentication.
- This can detect unauthorized hardware changes to a system.
- [TPMs have received criticism](https://arstechnica.com/gadgets/2021/08/how-to-go-from-stolen-pc-to-network-intrusion-in-30-minutes/) around trusting the manufacturer. Since the secret key is burned into the hardware at the time of manufacturer, the manufacturer would have access to this key at the time. It is possible for the manufacturer to store the keys that could then be used to duplicate a TPM that could break the security the module is supposed to provide.
- But this attack required the use of an electron microscope and micron precision equipment for manipulating the TPM circuitry.

__TEE (trusted execution environment)__ which takes the concept a bit further. It provides a full-blown isolated execution environment that runs alongside the main OS.

__Full disk encryption or FTE__ as you might have guessed from the name is the practice of encrypting the entire drive of the system, not just sensitive files in the system. This allows us to protect the entire contents of the disc from data theft or tampering.

Like the commercial product, PGP, Bitlocker from Microsoft, which integrates very well with TPM. Filevault 2 from Apple and the open source software, dm-crypt, which provides encryption for Linux systems.

Because the volume is encrypted, the BIOS can't access data on this volume for boot purposes. This is why FTE configurations will have a small unencrypted boot partition that contains elements like the kernel, bootloader and a NRD. At boot time, these elements are loaded which then prompts the user to enter a pass phrase to unlock the disk and continue the boot process.

[file_encrypt](https://i.imgur.com/0NRUxho.png)

### Cryptographic Terms Glossary

- Advanced Encryption Standard (AES): The first and only public cipher that's approved for use with top secret information by the United States National Security Agency
- Asymmetric encryption: Systems where different keys are used to encrypt and decrypt
- Authentication: A crucial application for cryptographic hash functions
- Block ciphers: The cipher takes data in, places that into a bucket or block of data that's a fixed size, then encodes that entire block as one unit
- CA (Certificate authority): It's the entity that's responsible for storing, issuing, and signing certificates. It's a crucial component of the PKI system
- Caesar cipher: A substitution alphabet, where you replace characters in the alphabet with others usually by shifting or rotating the alphabet, a set of numbers or characters
- CBC-MAC (Cipher block chaining message authentication codes): A mechanism for building MACs using block ciphers
- Central repository: It is needed to securely store and index keys and a certificate management system of some sort makes managing access to storage certificates and issuance of certificates easier
- Certificate fingerprints: These are just hash digests of the whole certificate, and aren't actually fields in the certificate itself, but are computed by clients when validating or inspecting certificates
- Certificate Revocation List (CRL): A means to distribute a list of certificates that are no longer valid
- Certificate Signature Algorithm: This field indicates what public key algorithm is used for the public key and what hashing algorithm is used to sign the certificate
- Certificate-based authentication: It is the most secure option, but it requires more support and management overhead since every client must have a certificate
- Certificate Signature Value: The digital signature data itself
- CMACs (Cipher-based Message Authentication Codes): The process is similar to HMAC, but instead of using a hashing function to produce a digest, a symmetric cipher with a shared keys used to encrypt the message and the resulting output is used as the MAC
- Code signing certificates: It is used for signing executable programs and allows users of these signed applications to verify the signatures and ensure that the application was not tampered with
- Cryptanalysis: Looking for hidden messages or trying to decipher coded message
- Cryptography: The overarching discipline that covers the practice of coding and hiding messages from third parties
- Cryptology: The study of cryptography
- Cryptosystem: A collection of algorithms for key generation and encryption and decryption operations that comprise a cryptographic service 
- Cryptographic hashing: It is distinctly different from encryption because cryptographic hash functions should be one directional
- Data binding and sealing: It involves using the secret key to derive a unique key that's then used for encryption of data
- Decryption: The reverse process from encryption; taking the garbled output and transforming it back into the readable plain text
- DES (Data Encryption Standard): One of the earliest encryption standards 
- Deterministic: It means that the same input value should always return the same hash value
- DH (Diffie-Hellman): A popular key exchange algorithm, named for its co-inventors
- DSA (Digital Signature Algorithm): It is another example of an asymmetric encryption system, though its used for signing and verifying data
- ECDH & ECDSA: Elliptic curve variants of Diffie-Hellman and DSA, respectively
- Eliptic curve cryptography (ECC): A public key encryption system that uses the algebraic structure of elliptic curves over finite fields to generate secure keys
- Encapsulating security payload: It's a part of the IPsec suite of protocols, which encapsulates IP packets, providing confidentiality, integrity, and authentication of the packets
- Encryption: The act of taking a message (plaintext), and applying an operation to it (cipher), so that you receive a garbled, unreadable message as the output (ciphertext)
- Encryption algorithm: The underlying logic or process that's used to convert the plaintext into ciphertext
- End-entity (leaf certificate): A certificate that has no authority as a CA
- Entropy pool: A source of random data to help seed random number generators
- FIPS (Federal Information Processing Standard): The DES that was adopted as a federal standard for encrypting and securing government data
- Forward secrecy: This is a property of a cryptographic system so that even in the event that the private key is compromised, the session keys are still safe
- Frequency analysis: The practice of studying the frequency with which letters appear in ciphertext
- Full disk encryption (FDE): It is the practice of encrypting the entire drive in the system
- Hash collisions: Two different inputs mapping to the same output
- Hashing (Hash function): A type of function or operation that takes in an arbitrary data input and maps it to an output of a fixed size, called a hash or a digest
- HMAC (Keyed-Hash Message Authentication Codes): It uses a cryptographic hash function along with a secret key to generate a MAC
- HTTPS: Hypertext Transfer Protocol Secure is a secure version of HTTP that ensures the communication your web browser has with the website is secured through encryption
- Intermediary (subordinate) CA: It means that the entity that this certificate was issued to can now sign other certificates
- IPsec (Internet Protocol security): A VPN protocol that was designed in conjunction with IPv6
- Issuer Name: This field contains information about the authority that signed the certificate
- Kerckhoff's principle: A principle that states that a cryptosystem, or a collection of algorithms for key generation and encryption and decryption operations that comprise a cryptographic service should remain secure, even if everything about the system is known except for the key
- Key: A crucial component of a cipher, which introduces something unique into your cipher
- Key length: It defines the maximum potential strength of the system
- Key signing parties: Organized by people who are interested in establishing a web of trust, and participants perform the same verification and signing
- Key size: It is the total number of bits or data that comprises the encryption key
- L2TP (Layer 2 Tunneling Protocol): It is typically used to support VPNs
- MACs (Message Authentication Codes): A bit of information that allows authentication of a received message, ensuring that the message came from the alleged sender and not a third party masquerading as them
- MD5: A popular and widely used hash function designed in the early 1990s as a cryptographic hashing function
- MIC (Message Integrity Check): It is essentially a hash digest of the message in question
- NIST: National Institute of Standards and Technology 
- Password salt: Additional randomized data that's added into the hashing function to generate the hash that's unique to the password and salt combination
- PGP (Pretty Good Privacy) encryption: An encryption application that allows authentication of data along with privacy from third parties relying upon asymmetric encryption to achieve this
- PKI system: A system that defines the creation, storage and distribution of digital certificates
- Pseudo-random: Something that isn't truly random
- Public key authentication: A key pair is generated by the user who wants to authenticate
- Public key signatures: Digital signature generated by composing the message and combining it with the private key
- RA (Registration Authority): It is responsible for verifying the identities of any entities requesting certificates to be signed and stored with the CA
- Rainbow table attacks: To trade computational power for disk space by pre-computing the hashes and storing them in a table
- Rainbow tables: A pre-computed table of all possible password values and their corresponding hashes
- Random numbers: A very important concept in encryption because it avoids some kind of pattern that an adversary can discover through close observation and analysis of encrypted messages over time
- RC4 (Rivest Cipher 4): Asymmetric stream cipher that gained widespread adoption because of its simplicity and speed
- Remote attestation: The idea of a system authenticating its software and hardware configuration to a remote system
- Root certificate authority: They are self signed because they are the start of the chain of trust, so there's no higher authority that can sign on their behalf
- RSA: One of the first practical asymmetric cryptography systems to be developed, named for the initials of the three co-inventors: Ron Rivest, Adi Shamir and Leonard Adleman
- Secure channel: It is provided by IPsec, which provides confidentiality, integrity, and authentication of data being passed
- Secure element: It's a tamper resistant chip often embedded in the microprocessor or integrated into the mainboard of a mobile device
- Secure Shell (SSH): A secure network protocol that uses encryption to allow access to a network service over unsecured networks
- Security through obscurity: The principle that if no one knows what algorithm is being used or general security practices, then one is safe from attackers
- Self-signed certificate: This certificate has been signed by the same entity that issued the certificate
- Serial number: A unique identifier for their certificate assigned by the CA which allows the CA to manage and identify individual certificates
- Session key: The shared symmetric encryption key using TLS sessions to encrypt data being sent back and forth
- SHA1: It is part of the secure hash algorithm suite of functions, designed by the NSA and published in 1995
- Shannon's maxim: It states that the system should remain secure, even if your adversary knows exactly what kind of encryption systems you're employing, as long as your keys remain secure
- SSL 3.0: The latest revision of SSL that was deprecated in 2015
- SSL/TLS Client Certificate: Certificates that are bound to clients and are used to authenticate the client to the server, allowing access control to a SSL/TLS service
- SSL/TLS Server Certificate: A certificate that a web server presents to a client as part of the initial secure setup of an SSL, TLS connection
- Steganography: The practice of hiding information from observers, but not encoding it
- Stream ciphers: It takes a stream of input and encrypts the stream one character or one digit at a time, outputting one encrypted character or digit at a time
- Subject: This field contains identifying information about the entity the certificate was issued to
- Subject Public Key Info: These two subfields define the algorithm of the public key along with the public key itself
- Substitution cipher: An encryption mechanism that replaces parts of your plaintext with ciphertext
- Symmetric key algorithm: Encryption algorithms that use the same key to encrypt and decrypt messages
- TLS 1.2: The current recommended revision of SSL
- TLS 1.2 with AES GCM: A specific mode of operation for the AES block cipher that essentially turns it into a stream cipher
- TLS Handshake: A mechanism to initially establish a channel for an application to communicate with a service 
- TPM (Trusted Platform Module): This is a hardware device that's typically integrated into the hardware of a computer, that's a dedicated crypto processor
- Transport mode: One of the two modes of operations supported by IPsec. When used, only the payload of the IP packet is encrypted, leaving the IP headers untouched
- Trusted execution environment (TEE): It provides a full-blown isolated execution environment that runs alongside the main OS
- Tunnel: It is provided by L2TP, which permits the passing of unmodified packets from one network to another
- Tunnel mode: One of the two modes of operations supported by IPsec. When used, the entire IP packet, header, payload, and all, is encrypted and encapsulated inside a new IP packet with new headers
 - Username and password authentication: Can be used in conjunction with certificate authentication, providing additional layers of security
- Validity: This field contains two subfields, Not Before and Not After, which define the dates when the certificate is valid for
- Version: What version of the X.509 standard certificate adheres to
- VPN (Virtual Private Network): A secure method of connecting a device to a private network over the internet
- Web of trust: It is where individuals instead of certificate authorities sign other individuals' public keys
- X.509 standard: It is what defines the format of digital certificates, as well as a certificate revocation list or CRL

# Encryption Lab
Before you can encrypt or decrypt anything, you need a private and a public key, so let's generate those first!

### Generating a Private Key

Remember, a key pair consists of a public key that you can make publicly available, and a private key that you need to keep secret. Shhhh. :) When someone wants to send you data and make sure that no one else can view it, they can encrypt it with your public key. Data that's encrypted with your public key can only be decrypted with your private key, to ensure that only you can view the original data. This is why it's important to keep private keys a secret! If someone else had a copy of your private key, they'd be able to decrypt data that's meant for you. Not good!

First, let's generate a 2048-bit RSA private key, and take a look at it. To generate the key, enter this command into the terminal:

```ssh
openssl genrsa -out private_key.pem 2048
```

You should see the following output (or something very similar) :

```ssh
Generating RSA private key, 2048 bit long modulus (2 primes)
................+++++
..........................................+++++
e is 65537 (0x010001)
```

This command creates a 2048-bit RSA key, called "private_key.pem". The name of the key is specified after the "-out" flag, and typically ends in ".pem". The number of bits is specified with the last argument. To view your new private key, use "cat" to print it to the screen, just like any other file:

```ssh
cat private_key.pem
```

The contents of the private key file should look like a large jumble of random characters. This is actually correct, so don't worry about being able to read it:

```ssh
-----BEGIN RSA PRIVATE KEY-----
MIIEowIBAAKCAQEA4kNMSmssCSYbOnq/UAHGH5xx9gjZaOiST3JQQtJO11L/YeBO
8DOHc7UawNADA/XDBAnGZih1M8T1PGc6Vk5SW2Lb8FMf9zG2XhYpCACFFPJAW00q
s4s1JesdugOprHZ8Jmm/QJl4KuCjlY/XdviCvcbxROIQ2mglR8nW1QWrhECQNBfo
dRSuTwmW3qBSW/Xd5pmTpP4GHCyUfRO9YCF/tZYtVMYg4FOqdGaTHRZbs6peMV4D
lSjZHDonnsGK0UJpxQNbtJEcG7vr7Vl8ziVWY5RUDND7nZYlQlbqxvvqbPPt+px3
4pAZ58eyOqeAmYBc8mwNoXp4YrC2deFng7zrKwIDAQABAoIBAB6SR0Ga33VQ/8bU
BPtzceidg8xhf7asDfDMGkodDmgLn9QCscfEvp2Er9uzf2TOlQ37oCH3f3aCOzxx
GjHFHV2Zquv630vQHLrztZGOOG0PGmD7uTRPL9wyu26BxjA2RioOibfZxKHOfmvb
5pn9k/S+Z6UOAobwIXFktTFNNdKFgalax813FlxFfmmoOC8kE30W6mP6iecP+ojm
xf577RhwR+PdE5zNNvm2F8j5ZWP39pboX7e3eYUCsEyPmVu1MSMTXrHHg6KNhCty
Qu1JfrAaisch+6vrAzfuP7t0WiILzieQgZzFDpI9HziwwOtCw+EKQhHCOPurWcO6
ByZUBzkCgYEA9aEprwqutbXB5H3QinxqXLInAH+wy8oTAMS6nV1sisIos6dD3CLO
u2fLRegv8PEUopASnzyv5PWU/iS+VJjdBCco59hmwW+7CVpaOJXlJ1qpznPVJmyx
pWsinM9Ug23GDd/jd61yKux22773RSGCYs9N7FVww5WYcDlWHLUFPk0CgYEA69DQ
h2iFuDSPonG8GPS6hf/KVRQaJZqGAINCk/2txTWmaz9VPdWT25+rxBzIoQOYAC4P
NjPHo/gJLrO/y6X6lAKBCje/Otb9E7GZwH0pFc7MxtQVR4ik6/7To3ancXNmawHe
owWZHDBRK+Ot33nZ+tYvAq48zE7rxNxsctZ9O1cCgYASsd12UR3S/q5vMZQ5thZy
T6zgQNe36v1fRZneeEnWlch7Q/PKQWvyn4e9Hlrnv7GOXeDM9dV9W6OnZCyIS8om
ksRuQO4xMsvNfm73d5ElWaUq7W3/qq4qpOjRfoY0Kpq0W6H4bd8OnUi+mN5BCLff
xV9s6WPXvv8HK5X+QVjQ0QKBgBrMqGY7IrdEge5cLpxHc8s2vq/ckPwlC4WTZUWc
VttKtZcKo41bcGpNQyAOhV6HIgcjNOdcCxw/XAvKsclbG5cmkbOvkjQFqs1KKccO
clTgI7WU9LYkeVm4pCS3n1/tVX5jwAGW6Uei1ha+0UvMdVFkdgM/+fjeHz1IL6r9
ZU4RAoGBALi33UjlJUYVMXPZc/JyFk8yyvRpYMRhmW7mQxR8gx0i1rNolPSccRkj
3NO+e1k86yyk3RsqBdixGKYDp2JqS+Aj7eHlxvUcrCAnpk9l96q8yuhQ4mJUWqs7
/hW6bxUPjDZ9BxprGZRL4ZLgPL+6C4Q4rE8TZu/5qQYDIy+ab03t
-----END RSA PRIVATE KEY-----
```

__Head's up__: Your private key will look similar to this, but it won't be the same. This is super important, because if openssl was generating the same keys over and over, we'd be in serious trouble!

### Generating a public key

Now, let's generate the public key from the private key, and inspect that one, too. Now that you have a private key, you need to generate a public key that goes along with it. You can give that to anyone who wants to send you encrypted data. When data is hashed using your public key, nobody will be able to decrypt it unless they have your private key. To create a public key based on a private key, enter the command below. You should see the following output:

```ssh
openssl rsa -in private_key.pem -outform PEM -pubout -out public_key.pem
```

```ssh
-----BEGIN PUBLIC KEY-----
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA4kNMSmssCSYbOnq/UAHG
H5xx9gjZaOiST3JQQtJO11L/YeBO8DOHc7UawNADA/XDBAnGZih1M8T1PGc6Vk5S
W2Lb8FMf9zG2XhYpCACFFPJAW00qs4s1JesdugOprHZ8Jmm/QJl4KuCjlY/XdviC
vcbxROIQ2mglR8nW1QWrhECQNBfodRSuTwmW3qBSW/Xd5pmTpP4GHCyUfRO9YCF/
tZYtVMYg4FOqdGaTHRZbs6peMV4DlSjZHDonnsGK0UJpxQNbtJEcG7vr7Vl8ziVW
Y5RUDND7nZYlQlbqxvvqbPPt+px34pAZ58eyOqeAmYBc8mwNoXp4YrC2deFng7zr
KwIDAQAB
-----END PUBLIC KEY-----
```

__Head's up__: Like your private key, your public key will look different than the one in this image.

Now that both of your keys have been created, and you can start using them to encrypt and decrypt data. Let's dive in!

### Encrypting and decrypting
You'll simulate someone encrypting a file using your public key and sending it to you, which allows you (and only you!) to decrypt it using your private key. Similarly, you can encrypt files using other people's public keys, knowing that only they will be able to decrypt them.

You'll create a text file that contains some information you want to protect by encrypting it. Then, you'll encrypt and inspect it. To create the file, enter the command below. It will create a new text file called "secret.txt" which just contains the text, "This is a secret message, for authorized parties only". Feel free to change this message to anything you'd like.

```bash
echo 'This is a secret message, for authorized parties only' > secret.txt
```

Then, to encrypt the file using your public key, enter this command:

```ssh
openssl rsautl -encrypt -pubin -inkey public_key.pem -in secret.txt -out secret.enc
```

This creates the file "secret.enc", which is an encrypted version of "secret.txt". Notice that if you try to view the contents of the encrypted file, the output is garbled. This is totally normal for encrypted messages because they're not meant to have their contents displayed visually.

Here's an example of what displaying the encrypted file "secret.enc" looks like in the nano editor using the following command below:

```ssh
nano ~/secret.enc
```
The output will be all jargon:

```ssh
^? <     e ^@vmD  ^B% r*M o^R ^O 8 X  {  ^\(^B  ^}= 1i T 9~ ^RT^\^Px ^T^l n ^G ^O ^i  iN (W [ ^$
^a^d~m  , d Tq L   < J ^Q bdQ
=Q R[^kT  ^G iq   GG  ^T {  UZ^dV8^A ^~O#koj^N^^ K vT ^O3 ^Tn^oP^l^Pa ^u3^G^N^i0=c{ ^tR09  o@^d$
<br>
<br>
<br>
<br>
<br>
<br>
<br>
^G Get Help  ^O Write Out  ^W Where Is  ^K Cut Text  ^J Justify  ^C Cur Pos
^X Exit  ^R Read File  ^\ Replace  ^U Uncut Text  ^T To Spell  ^_ Go To Line
```
To exit from the nano editor, use the command `Ctrl-X`.

The encrypted file will now be ready to send to whoever holds the matching private key. Since that's you, you can decrypt it and get the original contents back. Remember that we must use the private key to decrypt the message, since it was encrypted using the public key. Go ahead and decrypt the file, using this command:

```ssh
openssl rsautl -decrypt -inkey private_key.pem -in secret.enc
```

This will print the contents of the decrypted file to the screen, which should match the contents of "secret.txt":

```ssh
This is a secret message, for authorized parties only
```

### Creating a hash digest
Now, you'll create a hash digest of the message, then create a digital signature of this digest. Once that's done, you'll verify the signature of the digest. This allows you to ensure that your message wasn't modified or forged. If the message was modified, the hash would be different from the signed one, and the verification would fail.

To create a hash digest of the message, enter this command:

```ssh
openssl dgst -sha256 -sign private_key.pem -out secret.txt.sha256 secret.txt
```

This creates a file called "secret.txt.sha256" using your private key, which contains the hash digest of your secret text file.

With this file, anyone can use your public key and the hash digest to verify that the file hasn't been modified since you created and hashed it. To perform this verification, enter this command:

```ssh
openssl dgst -sha256 -verify public_key.pem -signature secret.txt.sha256 secret.txt
```

This should show the following output, indicating that the verification was successful and the file hasn't been modified by a malicious third party:

```ssh
Verified OK
```

__Security Note__: If _any other output_ was shown, it would indicate that the contents of the file had been changed, and it's likely no longer safe.

# Hashing and Hash Verification Lab
#### MD5

Let's kick things off by creating a text file containing some data. Feel free to substitute your own text data, if you want. This command creates a text file called "file.txt" with a single line of basic text in it:

```ssh
echo 'This is some text in a file, just so we have some data' > file.txt
```

You'll now generate the MD5 sum for the file and store it. To generate the sum for your new file, enter this md5sum command:

```ssh
md5sum file.txt > file.txt.md5
```

This creates the MD5 hash, and saves it to a new file. You can take a look at the hash by printing its contents to the screen, using this command:

```ssh
cat file.txt.md5
```

This should print the hash to the terminal, which should look something like this:

```ssh
c7a8ef893898f9a6b380eb4ec1e87113  file.txt
```

More importantly, you can also verify that the hash is correct, and that the original file hasn't been tampered with since the sum was made. To do this, enter this command and see the following output, which indicates that the hash is valid:

```ssh
md5sum -c file.txt.md5
```

### Verifying an invalid file

Next, we'll demonstrate the security of this process by showing how even a single-character change to the file results in a different hash. First, you'll create a copy of the text file, and insert a single space at the end of the file. Feel free to use any text-editor that you'd like. Head's up that we've included instructions for making this change in Nano. To make a copy of the file, enter this command:

```ssh
cp file.txt badfile.txt
```

Then generate a new md5sum for the new file:

```ssh
md5sum badfile.txt > badfile.txt.md5
```

Note that the resulting hash is identical to the hash for our original file.txt despite the filenames being different. This is because hashing only looks at the data, not the metadata of the file.

```ssh
cat badfile.txt.md5
```

```ssh
cat file.txt.md5
```

To open the text file in Nano, enter this command:

```sh
nano badfile.txt
```

This will open the file in the text editor. To add a space to the end of the file, use the arrow keys (not the mouse!) to move the cursor to the end of the line of text. Then, press the spacebar to add a space character to the end of the file. Your screen should look like this image:

```ssh
This is some text in a file, just so we have some data 
<br>
<br>
<br>
<br>
<br>
<br>
^G Get Help  ^O Write Out  ^W Where Is  ^K Cut Text  ^J Justify  ^C Cur Pos
^X Exit  ^R Read File  ^\ Replace  ^U Uncut Text  ^T To Spell  ^_ Go To Line
```

To save the file, press `CTRL+X`. Confirm by typing `Y` for yes, then press `Enter` to confirm.

This will take you back to the normal terminal screen. Now that you've made a very minor change to the file, try verifying the hash again. It should fail verification this time, showing that any change at all will result in a different hash. Try to verify it by entering this command again:

```ssh
md5sum -c badfile.txt.md5
```

You should see a message that shows that the verification wasn't successful:

```ssh
badfile.txt: FAILED
md5sum: WARNING: 1 computed checksum did NOT match
```

To see how different the hash of the edited file is, generate a new hash and inspect it:

```ssh
md5sum badfile.txt > new.badfile.txt.md5
```

```ssh
cat new.badfile.txt.md5
```

Check out how it's different from our previously generated hash:

```
dcd879fd2c162dbfe9a186a67902e7ce  badfile.txt
```

For reference, here are the contents of the original sum:

```
c7a8ef893898f9a6b380eb4ec1e87113  file.txt
```

### SHA

Let's do the same steps, but for SHA1 and SHA256 hashes using the shasum tool. Functionally, the two work in very similar ways, and their purpose is the same. But SHA1 and SHA256 offer stronger security than MD5, and SHA256 is more secure than SHA1. This means that it's easier for a malicious third party to attack a system using MD5 than one using SHA1. And because SHA256 is the strongest of the three, it's currently widely used.

#### SHA1

To create the SHA1 sum and save it to a file, use this command:

```ssh
shasum file.txt > file.txt.sha1
```

View it by printing it to the screen, like you've done before:

```ssh
cat file.txt.sha1
```

```
65639a89992784291d769e05338085d1739645c6  file.txt
```

Now, verify the hash using the command below. (Like before, this would fail if the original file had been changed.)

```ssh
shasum -c file.txt.sha1
```

You should see the following output, indicating that the verification was a success:

```ssh
file.txt: OK
```

#### SHA256

The same tool can be used to create a SHA256 sum. The "-a" flag specifies the algorithm to use, and defaults to SHA1 if nothing is specified. To generate the SHA256 sum of the file, use this command:

```ssh
shasum -a 256 file.txt > file.txt.sha256
```

You can output the contents of this file, the same as before:

```ssh
cat file.txt.sha256
```
SHA256's increased security comes from it creating a longer hash that's harder to guess. You can see that the contents of the file here are much longer than the SHA1 file:

```ssh
7a54af37c15a82e157c8368324e7234d22778ce845219cd16172895a608030ff  file.txt
```

Finally, to verify the SHA256 sum, you can use the same command as before:

```ssh
shasum -c file.txt.sha256
```
#### Conclusion 
Congrats! You've successfully created and verified hashes using three of the most common hashing algorithms: MD5, SHA1, and SHA256. You've also demonstrated the security of these hashes by showing that even very small changes to the file result in a new hash and cause the verification to fail.

# Physical Privacy and Security Components
#### Physical privacy and security
In this reading, you will learn more about physical privacy and security, including biometric and Near Field Communication authentication. You will also revisit the “confidentiality” aspect of the CIA Principle (Confidentiality, Integrity, Availability), which was introduced previously in this certificate program.

#### CIA Principle: Confidentiality
Preventing unauthorized access to an organization’s data and networks is imperative in protecting a company’s information systems. Regulations, standards, and laws may also require that certain information be kept confidential, like health records. Failing to ensure the confidentiality of specific types of data could result in damage to reputation, loss of customers, liability lawsuits, financial losses, penalty fines, criminal charges, and more. It is vital for IT Support specialists to take all measures possible to protect confidential information.  

In a previous video, you learned about three types of authentication methods:

- __Something you know__ - password or pin number
- __Something you have__ - bank card, USB device, key fob, or OTP (one-time password)
- __Something you are__ - biometric data, like a fingerprint, voice signature, facial recognition, or retinal scan 

You will learn more about biometrics in this reading, along with two additional categories of authentication methods:

- __Somewhere you are__ - geofencing, GPS, Indoor Positioning Systems (IPS)
- __Something you do__ - gestures, swipe patterns, CAPTCHA, or patterns of behavior

Some authentication technologies inherently require two factors:

- __Somewhere you are + Something you have__ - Near Field Communication (NFC) uses both proximity to an NFC scanner and a device like an NFC-enabled smartphone or an RFID chip on an employee ID or bank card.

#### Something you are: Biometrics
Biometric authentication occurs in two steps: enrollment and authentication. Enrollment happens when the user provides their biometric data for the first time through a hardware scanner. Specific features of that biometric data are extracted, encrypted, and stored, often in a database or on a personal mobile device. Authentication, as the second step, happens when a user presents their biometric data again to the scanner to gain access to the secured item. This new scan is compared against the original stored biometric data to authenticate the person’s identity. 

##### Fingerprint scanning 
In a previous video, you learned about fingerprint scanners as an authentication method for mobile devices. Fingerprint scanners use small capacitive cells that are engineered to detect fingerprint ridges. Dirt and moisture can interfere with the scanner’s ability to do its job. As an IT Support specialist, you may need to replace damaged fingerprint scanners on customer devices.

##### Facial recognition
Many smartphone models provide the hardware and software to use facial recognition as a biometric authentication method. This often requires two cameras. The first camera uses normal color photography. The second camera uses infrared technology to measure depth and ensure your face is 3-dimensional. This prevents hackers from using photographs of the authorized users to unlock mobile devices. 

##### Iris and Retinal scanning 
Iris scanning is not a secure form of biometric authentication because a photograph of the user’s iris can be used to gain access. In contrast, retinal scanning is one of the more secure forms of biometric authentication. It is exceedingly difficult to impersonate the retinal features of a person’s eye. Our retinas have unique and complex patterns in how our blood vessels are arranged. These fingerprint-like patterns can be scanned by shining a beam of infrared light into the eye. Note that eye injuries and medical problems with the eyes can change retinal blood vessel patterns and cause users to be denied access to their devices.  Although retinal scanning is secure, the technology can be expensive and difficult to implement.

#### Somewhere you are: Geolocation
The geographical location of a user can serve as one part of a multi-factor authentication policy or to deny access to users based on their locations. Geolocation services can use GPS, IP ranges, WiFi access points, cell phone towers, and/or Bluetooth beacons to estimate a mobile user’s location. 

##### Geofencing
Geofencing is used to authenticate users who are physically within a certain radius of a specific location. For example, if you order food using McDonald’s smartphone app, the restaurant will not process your order until your smartphone is within a certain radius of the restaurant. You cannot send someone else to pick up your order either, as that person cannot authenticate without your smartphone being within the geofencing radius.  

##### Global Positioning Systems (GPS)
Global Positioning Systems (GPS) use satellites orbiting Earth to map a device's longitude and latitude. The mobile device needs to be equipped with GPS sensors and have GPS services enabled to take advantage of GPS-based authentication technologies. GPS could be used to authenticate a device based on the physical location of the user. Insurance companies use GPS data to verify the authenticity of disaster claims filed through mobile apps. 

##### Indoor Positioning Systems (IPS) 
Indoor Positioning Systems (IPS) triangulate a device’s location by using WiFi access points, cell phone towers, and/or Bluetooth beacons. Users must grant permission to apps to use this technology. IPS locations might be used to deny network access when the user has entered a restricted area.

#### Near-field communication (NFC) and scanners
You may have interacted with a near-field communication (NFC) scanner by using   contactless payments with a credit card, bank card, or smartphone. NFC technology can also be used for authentication and access to physical buildings through school or employment ID cards.

NFC transmits on the same frequency as high frequency RFID (13.56 MHz) and has a short distance range of 10 centimeters. The short distance range provides some protection from hackers attempting to intercept the connection to obtain your credit card information. However, NFC is not fully secure. An innocuous looking NFC scanner sitting next to an NFC-enabled payment device could record all NFC transactions that occur within the 10 cm of the device in a “man in the middle” security breach.    

#### Something you do: Gestures and Behaviors
You may already be familiar with using gestures like swipe patterns to unlock a smartphone. Another gesture-based authentication method is the Picture Password, which requires the user to touch specific, secret points on a photograph to unlock the device.

Patterns of people’s behaviors can be used to authenticate identity. For example, an organization might keep track of computer system login and logout times of employees. These patterns could be monitored for any unusual changes in employee behavior, which may indicate that the “employee” is instead an imposter. 

Turing tests are used to determine if an unknown entity is a human or a machine. You have probably responded to a CAPTCHA (Completely Automated Public Turing test to tell Computers and Humans Apart) to authenticate that you are indeed a human and not a bot. This is accomplished by asking the user to identify items within a set of photographs. Photos are used for this test because images are more difficult for bots to identify than text. 

### Key takeaways
There are a variety of MFA protocols that can be implemented to protect the confidentiality, privacy, and security of data and networks. The 5 types of authentication can be categorized as:

1. Something you know - password or pin number
1. Something you have - bank card, USB device, key fob, or OTP (one-time password)
1. Something you are - biometric data, like a fingerprint, voice signature, facial recognition, or retinal scan 
1. Somewhere you are - geolocation, geofencing, GPS, Indoor Positioning Systems (IPS), NFC scanning
1. Something you do - gestures, swipe patterns, CAPTCHA, or patterns of behavior

### Resources for more Information
For more information about methods of authentication to protect data, please visit:

[Geolocation—The Risk and Benefits of a Trending Technology](https://www.isaca.org/resources/isaca-journal/issues/2016/volume-5/geolocationthe-risk-and-benefits-of-a-trending-technology) - Discusses impacts, benefits, risks, risk mitigation, security, governance, and privacy concerns of geolocation technologies. 

[Understanding The 5 Factors Of Multi-Factor Authentication](https://analyticsindiamag.com/understanding-the-5-factors-of-multi-factor-authentication/) - Overview of the 5 Factors: Something you know, Something you have, Something you are, Somewhere you are, and Something you do.

[Homeland Security Biometrics](https://www.dhs.gov/biometrics) - History and use cases of biometrics for maximum security and identification of criminals in the United States Departments of Homeland Security, Defense, Justice, and Commerce, as well as the National Institute of Standards and Technology.

[A Review on Authentication Methods](https://hal.archives-ouvertes.fr/hal-00912435/PDF/A_Review_on_Authentication_Methods.pdf) - Informative peer-reviewed journal article on authentication methods.

[Modern Authentication Methods: A Comprehensive Survey](https://www.intechopen.com/journals/1/articles/100) - Peer-reviewed journal article with expanded coverage of two-factor and multi-factor authentication topics. Provides comprehensive comparisons of advantages and disadvantages of each authentication method. 

[What is the Difference Between NFC and RFID?](https://www.globalpaymentsintegrated.com/en-us/blog/2020/04/21/what-is-the-difference-between-nfc-and-rfid) - A comparison of NFC and RFID technologies.

[Fingerprint Reader Replacement Guide](https://guides.frame.work/Guide/Fingerprint+Reader+Replacement+Guide/91) - Provides photos of internal fingerprint scanner hardware parts, as well as instructions on how to replace a fingerprint scanner on a laptop. Like these [kids clever enough to skip school](https://www.hindustantimes.com/mumbai-news/you-will-be-glued-to-this-mumbai-college-s-students-trick-biometric-system/story-W64f1jdMtecxKDml2DakeI.html) did.

# Authorization
[oauth](https://i.imgur.com/Pdm0snx.png)

__OAuth__ _is an open standard that allows users to grant third party websites and applications access to their information without sharing account credentials._
- This can be thought of as a form of access delegation because access to the user's account is being delegated to the third party.
- Once confirmed, the identity provider will supply the third party with a token that gives them access to the user's information. This token can then be used by the third party to access data or services offered by the identity provider directly on behalf of the user.
- OAuth is commonly used to grant access to third party applications to APIs offered by large internet companies like Google, Microsoft and Facebook.
- Example: Let's say you want to use a third party meme creation website. This website lets you create memes using templates and gives you the option to save your creations and email them to your friends. Instead of the site sending the emails directly, which would appear to be coming from an address your friends wouldn't recognize. The site uses OAuth to get permission to send the memes using your email account directly. This is done by making an OAuth request to your email provider. Once you approve this request, the email provider issues an access token to the site which grants the site access to your email account. The access token would have a scope which says that it can only be used to access email, not other services associated with the account.
-  __OAuth permissions can be used in phishing style attacks to gain access to accounts without requiring credentials to be compromised__. This works by sending phishing emails to potential victims that look like legitimate OAuth authorization requests. Which asked the user to grant access to some aspects of their account through OAuth. Once the user grants access, the attacker has access to the account through the OAuth authorization token. [This was used in an OAuth based worm attack in early 2017.](https://www.theverge.com/2017/5/3/15534768/google-docs-phishing-attack-share-this-document-with-you-spam)
 - There was a rash of phishing emails that appear to be from a friend or colleague who wanted to share a Google doc. When the sharing link was followed, the victim was prompted to log in and authorized access to email, documents. And contacts for some third party service which only identified itself as the name Google Apps. But it was actually a malicious service that would then email contacts from their email account perpetuating the attack.

[oauthvopenid](https://i.imgur.com/y6zHBgq.png)

- It's important to distinguish between OAuth and open ID.
 - OAuth is specifically an authorization system and open ID is an authentication system though they're usually used together.
 - Open ID connect is an authentication layer built on top of OAuth point designed to improve upon open ID, and build better integration with OAuth authorizations.

[acl](https://i.imgur.com/e50qMhP.png)

__ACL__ is an _access control list_ is a way of defining permissions or authorizations for objects.
- A file system would have an ACL which is a table or database, with a list of entries specifying access rights for individuals or groups for various objects on the file system like folders, files, or programs.
- Network ACLs are used for restricting and controlling access to host their services running on hosts within your network. Network ACLs can be defined for incoming and outgoing traffic. They can also be used to restrict external access to systems and limit outgoing traffic to enforce policies or to prevent unauthorized outbound data transfers.

### Mobile Security Methods
Laptop computers, tablets, smartphones, and other mobile devices allow people to remain productive from various locations, such as at home or while traveling. This increased flexibility raises various security concerns that IT departments need to address. This reading provides information about the current security measures used to protect mobile devices. 

#### Common mobile security threats and challenges 
Many of the security threats associated with mobile devices are the same as those of traditionally networked devices, such as hacking and malware. However, mobile devices face additional threats that other devices do not. 

Here are some threats facing mobile device security:

- __Phishing__: Phishing attacks can use SMS messaging, email accounts, messages via numerous social media applications, or malicious links in browsers to target your mobile devices.

- __Malicious applications (malware)__: Malware can take the form of apps designed to collect and transmit personal and corporate information to third parties.

- __Insecure Wi-Fi and “meddler in the middle” attacks__: An attacker places themself in the middle of two hosts that think they're communicating directly. The attacker may monitor the information from these hosts and potentially modify it in transit. Open or "free" Wi-Fi hotspots are especially susceptible to meddler in the middle and similar attacks.

- __Poor update habits for devices and apps__: An example is failure to install security patches regularly deployed through software and firmware updates. Unpatched devices and applications often contain exploits and vulnerabilities that attackers may use to collect sensitive data.

You can imagine how all these issues could threaten confidentiality, integrity, or access (the CIA triad)—but confidentiality is of particular concern for mobile security.

Security measures used to protect mobile devices
There are several security measures in place to protect mobile devices from these security concerns. 

#### Screen Locks
Screen locks are methods for preventing unauthorized access to a device. They can be particularly effective for diminishing risks associated with the loss or theft of the device. These measures include: 

- __Facial recognition__: uses a device’s camera to unlock the device once the user’s face is recognized
- __PIN codes__: uses a sequence of four or more numbers to unlock the device
- __Fingerprint recognition__: matches a user’s fingerprint with a saved image of the fingerprint to unlock the device 
- __Pattern uses__: uses a pattern that users must trace to unlock the device

#### Remote wipes 
Remote wipes are methods to remove data from a device remotely. Remote wiping is another way to diminish risks associated with the loss or theft of a device and include:

- __Locator applications__: apps that help users find lost devices
- __OS updates__: security patches regularly deployed through Operating System updates (as well as firmware and application updates)
- __Device encryption__: encryption techniques that protect the device from unauthorized access
- __Remote backup applications__: apps that allow administrators to remotely remove applications that compromise security
- __Failed login attempt restrictions__: stops access, either completely or for a set period of time, after too many failed attempts to log in
- __Antivirus/Antimalware__: software packages for mobile devices often offered by the same vendors as desktop Antivirus programs
- __Firewalls__: either devices or software that check incoming network traffic and keep out unwanted traffic

#### Policies and procedures 
IT departments establish policies and procedures to ensure users don’t make security mistakes. They typically include mobile-specific policies such as acceptable use guidelines, preferred mobile security practices, and security platforms or services. 

Once IT staff and management collaborate to build a mobile security policy, there is still work to do. Organizations must find the best way to outline this policy and communicate it to users. A policy is only effective if users understand and adhere to it.

### Key takeaways:
As your organization embraces the advantages of mobile devices and wireless networks, your IT security strategies must account for the specific risks, vulnerabilities, and threats associated with mobile computing by: 

1. Monitoring for common mobile security concerns such as phishing, malicious applications, insecure Wi-Fi, and poor upgrade habits and applying the current methods for addressing them
1. Implementing security measures to protect mobile devices like screen lock and remote wipes 
1. Providing clear mobile security policies and procedures and communicating them to users

# Accounting
The final A of the triple AAA's of security is __accounting__.
- This means keeping records of what resources and services your users access or what they did when they were using your systems.
- A critical component of this is auditing which involves reviewing these records to ensure that nothing is out of the ordinary.
- For example:
 - a TACACS+ server would be more concerned with keeping track of user authentication. What systems they authenticated to and what commands they ran during their session. This is because TACACS+ is a device access AAA system that manages who has access to your network devices and what they do on them.
 - Cisco's AAA system supports accounting of individual commands executed connection to and from network devices. Commands executed in privileged mode and network services and system details like configuration reloads or reboots.
- Radius would track details like session duration, client location and bandwidth or other resources used during the session. This is because radius is a network access AAA system so it tracks details about network access and usage.

This data can also be used to enforce data or time quotas, limiting the duration of sessions or restricting the amount of data that can be sent or received. 

[isp_accounting](https://i.imgur.com/8RIxAtH.png)

# AAA Glossary

Access Control Entries: The individual access permissions per object that make up the ACL

Access Control List (ACL): It is a way of defining permissions or authorizations for objects

Accounting: Keeping records of what resources and services your users access or what they did when they were using your systems

Auditing: It involves reviewing records to ensure that nothing is out of the ordinary

Authentication: A crucial application for cryptographic hash functions

Authentication server (AS): It includes the user ID of the authenticating user

Authorization: It pertains to describing what the user account has access to or doesn't have access to

Bind: It is how clients authenticate to the server

Biometric authentication: Authentication that uses Biometric data 

Certificate Revocation List (CRL): A means to distribute a list of certificates that are no longer valid

Client certificates: They operate very similarly to server certificates but are presented by clients and allow servers to authenticate and verify clients

Counter-based tokens: They use a secret seed value along with the secret counter value that's incremented every time a one-time password is generated on the device

Data information tree: A structure where objects will have one parent and can have one or more children that belong to the parent object

Distinguished name (DN): A unique identifier for each entry in the directory 

Extensible authentication protocol (EAP over LAN, or EAPOL): A standard authentication protocol

Identification: The idea of describing an entity uniquely

Kerberos: A network authentication protocol that uses tickets to allow entities to prove their identity over potentially insecure channels to provide mutual authentication

Lightweight Directory Access Protocol (LDAP): An open industry-standard protocol for accessing and maintaining directory services; the most popular open-source alternative to the DAP

Multifactor authentication (MFA): A system where users are authenticated by presenting multiple pieces of information or objects

Network time protocol (NTP): A network protocol used to synchronize the time between the authenticator token and the authentication server

OAuth: An open standard that allows users to grant third-party websites and applications access to their information without sharing account credentials

One-time password (OTP): A short-lived token, typically a number that's entered along with a username and password

One-time password (OTP) tokens: Another very common method for handling multifactor

OpenID: An open standard that allows participating sites known as Relying Parties to allow authentication of users utilizing a third party authentication service

Organizational units (OUs): Folders that let us group related objects into units like people or groups to distinguish between individual user accounts and groups that accounts can belong to

Physical tokens: They take a few different forms, such as a USB device with a secret token on it, a standalone device which generates a token, or even a simple key used with a traditional lock

Remote Authentication Dial-in User Service (RADIUS): A protocol that provides AAA services for users on a network

Risk mitigation: Understanding the risks your systems face, take measures to reduce those risks, and monitor them

Security keys: Small embedded cryptoprocessors, that have secure storage of asymmetric keys and additional slots to run embedded code

Single Sign-on (SSO): An authentication concept that allows users to authenticate once to be granted access to a lot of different services and applications

StartTLS: It permits a client to communicate using LDAP v3 over TLS

TACACS+: It is a device access AAA system that manages who has access to your network devices and what they do on them

Ticket granting service (TGS): It decrypts the Ticket Granting Ticket using the Ticket Granting Service secret key, which provides the Ticket Granting Service with the client Ticket Granting Service session key

Time-based token (TOTP): A One-Time-Password that's rotated periodically

U2F (Universal 2nd Factor): It's a standard developed jointly by Google, Yubico and NXP Semiconductors that incorporates a challenge-response mechanism, along with public key cryptography to implement a more secure and more convenient second-factor authentication solution

Unbind: It closes the connection to the LDAP server

XTACACS: It stands for Extended TACACS, which was a Cisco proprietary extension on top of TACACS

# Securing Network Architecture

__Network hardening__ is the process of securing a network by reducing its potential vulnerabilities through configuration changes and taking specific steps.

__Implicit deny__ is a network security concept where anything not explicitly permitted or allowed should be denied. This is different from blocking all traffic, since an Implicit deny configuration will still let traffic pass that you've defined as allowed. You can do this through ACO configurations. 
- Instead of requiring you to specifically block all traffic you don't want, you can just create rules for traffic that you need to go through. _You can think of this as whitelisting as opposed to blacklisting._
- Before a new service will work, a new rule must be defined for it, reducing convenience a bit.

Another very important component of network security is monitoring and analyzing traffic on your network.
-  The first is that it lets you establish a baseline of what your typical network traffic looks like. This is key because in order to know what unusual or potential attack traffic looks like, you need to know what normal traffic looks like.

__Analyzing logs__ is the practice of collecting logs from different network and sometimes client devices on your network, then performing an automated analysis on them.
- This will highlight potential intrusions, signs of malware infections, or a typical behavior. You should pay close attention to any external facing devices or services. They're subject to a lot more potentially malicious traffic, which increases the risk of compromise.
- Analysis of logs would involve looking for a specific log messages of interests, like with firewall logs.
- Attempted connections to an internal service from an untrusted source address may be worth investigating. Connections from the internal network to known address ranges of botnet command and control servers could mean there's a compromised machine on the network.
- __Normalizing log data__ is an important step since logs from different devices and systems may not be formatted in a common way. You might need to convert log components into a common format to make analysis easier for analysts and rule-based detection systems.
Correlation analysis is the process of taking log data from different systems and matching events across the systems.
-  You'd want to analyze things like:
 - firewall logs,
 - authentication server logs,
 - and application logs. As an IT support specialist, 

__Logs analysis systems__ are configured using user-defined rules to match interesting or a typical log entries. These can then be surfaced through an alerting system to let security engineers investigate the alert. 

#### Firewall Rule Reading 
- [Cisco IOS firewall rules](https://www.cisco.com/en/US/docs/routers/access/800/850/software/configuration/guide/firewall.html)
- [Juniper firewall rules](https://www.juniper.net/documentation/en_US/junos/topics/usage-guidelines/services-configuring-stateful-firewall-rules.html)
- [Iptables firewall rules](https://www.digitalocean.com/community/tutorials/iptables-essentials-common-firewall-rules-and-commands)
- [UFW - Uncomplicated Firewall rules](https://www.digitalocean.com/community/tutorials/ufw-essentials-common-firewall-rules-and-commands)
- [Configuring Mac OS X firewall](https://support.apple.com/en-us/HT201642)
- [Microsoft firewall rules](https://technet.microsoft.com/en-us/library/cc754274(v=ws.11).aspx)

### Network Hardware Hardening

- To protect against this rogue DHCP server attack, enterprise switches off a feature called DHCP snooping. A switch that has DHCP snooping will monitor DHCP traffic being sent across it. It will also track IP assignments and map them to hosts connected to switch ports. This basically builds a map of assigned IP addresses to physical switch ports. This information can also be used to protect against IP spoofing and ARP poisoning attacks.

![dhcp_snooping](https://i.imgur.com/BnIGnFw.png)

- DHCP snooping also makes you designate either a trusted DHCP server IP if it's operating as a DHCP helper and forwarding DHCP requests to the server. Or you can enable DHCP snooping trust on the uplinked port, where legitimate DHCP responses would now come from.
- Any DHCP responses coming from either an untrusted IP address or from a downlink switch port would be detected as untrusted and discarded by the switch. 

![dynamic_ARP_inspection](https://i.imgur.com/ay5ZtLy.png)
-  ARP allows for a Layer 2 man-in-the-middle attack because of the unauthenticated nature of ARP. It allows an attacker to forge an ARP response advertising its MAC address as the physical address matching a victim's IP address. This type of ARP response is called a gratuitous ARP response, since it's effectively answering a query that no one made.
- The attacker could enable IP forwarding, which would let them transparently monitor traffic intended for the victim. They could also manipulate or modify data. Dynamic ARP Inspection or DAI, is another feature on enterprise switches that prevents this type of attack.
- __Dynamic ARP Inspection__ or __DAI__, is another feature on enterprise switches that prevents this type of attack. It requires the use of DHCP snooping to establish a trusted binding of IP addresses to switch ports.
- DAI would detect these forged gratuitous ARP packets and drop them. It does this because it has a table from DHCP snooping that has the authoritative IP address assignments per port. DAI also enforces rate-limiting of ARP packets per port to prevent ARP scanning. 
- To prevent IP spoofing attacks, __IP Source Guard__ or __IPSG__ can be enabled on enterprise switches along with DHCP snooping.
- This dropped packets that don't match the IP address for the port based on a DHCP snooping table. 
- If you really want to lock down your network, you can implement 802.1X. It's important for an IT support specialist to be aware of 802.1X. This is the IEEE standard for encapsulating __EAP or Extensible Authentication Protocol__ traffic over the 802 networks. This is also called __EAP over Lan or EAPoL__.

![extensible_authentication_protocol](https://i.imgur.com/i7y18fb.png)

- EAP-TLS since it's one of the more common and secure EAP methods. __EAP-TLS is an authentication type supported by EAP that uses TLS to provide mutual authentication of both the client and the authenticating server.__
- When a client wants to authenticate to a network using 802.1X, there are three parties involved. The client device is what we call the __supplicant__.
 - It's sometimes also used to refer to the software running on the client machine that handles the authentication process for the user.
 - The open source Linux utility, WPA supplicant is one of those.
- The supplicant communicates with the __authenticator, which acts as a gatekeeper for the network__. It requires clients to successfully authenticate to the network before they're allowed to communicate with the network. This is usually an enterprise switch or an access point in the case of wireless networks. It's important to call out that while the supplicant communicates with the authenticator, it's not actually the authenticator that makes the authentication decision. The authenticator acts like a go-between and forwards the authentication request to the authentication server. That's where the actual credential verification and authentication occurs. The authentication server is usually a radius server. 

 ![EAP-TLS](https://i.imgur.com/igsoGur.png)

 - Similarly, most EAP-TLS implementations require client-side certificates. Authentication can be certificate based, which requires a client to present a valid certificate that's signed by the authenticating CA. Or a client can use a certificate in conjunction with a username, password, and even a second factor of authentication like a onetime password. The security of EAP-TLS stems from the inherent security that the TLS protocol and PKI provide.
 - You have to safeguard private keys appropriately and ensure distribution of the CA certificate to client devices to allow verification of the server side.
 - Even more secure configuration for EAP-TLS would be to bind the client-side certificates to the client platforms using __TPMs__. This would prevent theft of the certificates from client machines.

![TPM](https://i.imgur.com/ISGmyih.png)
Example of a TMP (trusted platform module)

 - When you combine this with FDE, even theft of a computer would prevent compromise of the network.

#### IEEE 802.1X Protocol

- IEEE 802.1x is a protocol developed to let clients connect to port based networks using modern authentication methods.
  - There are three nodes in the authentication process: supplicant, authenticator, and authentication server.
  - The authentication server uses either a shared key system or open access system to control who is able to connect to the network.
  - Based on the criteria of the authentication server the supplicator will grant the authentication request and begin the connection process or it will be sent an Access Reject message and terminate the connection.
- When clients are trying to communicate on a local network, the devices must have a standard method of communication and authentication. The Institute of Electrical and Electronics Engineers (IEEE) created a standard called IEEE 802.1X. This standard specifies a common architecture, functional elements, and protocols that support authentication between the clients of ports attached to the same Local Area Network (LAN). 
- IEEE 802 networks are deployed in locations that provide access to critical data, support mission critical applications, or charge for service. Port-based network access control regulates access to the network, guarding against attacks by unauthorized parties, network disruption, and data loss.

#### 3 Compents of Authentication

The three main components in the authentication process are:
- Supplicant is the client making the request to access the LAN or wireless access point.
- Authenticator takes the packet from the supplicator and sends it to the authentication server until the session is authenticated. Any other information sent before authentication occurs is dropped.
- Authentication server provides a database of information required for authentication, and informs the authenticator to deny or permit access to the supplicant.

Authentication occurs when a client first connects to a network. The client sends a packet of information and the authenticator sends the packet to the authentication server. In some instances, the authenticator and authentication server may be integrated into a single point. The authentication server then verifies the identity or key against the information in its database. If the credentials are valid, the authentication succeeds. Then the server begins processing the connection request. If the credentials are not valid, the authentication fails. The authentication server sends an Access Reject message and the connection request is denied.

#### Authentication Methods 

When the request is sent to the authentication server there are a couple of methods for authentication.

- IEEE defines two different link-level authentication methods:
  - __Shared key system__ is a shared key or passphrase that is manually set on both the mobile device and the AP/router.
  - __Open system__ is when the authentication server has a list of authorized clients to check against when a client requests access. This list is usually in the form of MAC addresses but it varies by network.
- Shared Key authentication methods:
  - __Wired Equivalent Privacy (WEP)__ is _not_ recommended for a secure WLAN. The main security risk is hackers capturing the encrypted form of an authentication response frame, using widely available software applications, and using the information to crack WEP encryption.
  - __Wi-Fi Protected Access (WPA)__ complies with the wireless security standard and strongly increases the level of data protection and access control (authentication) for a wireless network. WPA enforces IEEE 802.1X authentication and key-exchange and only works with dynamic encryption keys. 
  - __Wi-Fi Protected Access 2 (WPA2)__ is a security enhancement to WPA. Users must ensure the mobile device and AP/router are configured using the same WPA version and pre-shared key (PSK).
  - __Association__ allows the access point or router to record each mobile device so that data is properly delivered. This occurs after authentication is complete. 

These authentication methods are standardized under the IEEE 802.1X protocol.
