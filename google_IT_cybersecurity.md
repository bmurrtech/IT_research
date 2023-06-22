Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

**Attribution NonCommercial ShareAlike 4.0 International**

You are free to:
- Share — copy and redistribute the material in any medium or format
- Adapt — remix, transform, and build upon the material
- The licensor cannot revoke these freedoms as long as you follow the license terms.
- Under the following terms:
  - Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
  - NonCommercial — You may not use the material for commercial purposes.
  - ShareAlike — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.
  - No additional restrictions — You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.

Notices:
You do not have to comply with the license for elements of the material in the public domain or where your use is permitted by an applicable exception or limitation.
No warranties are given. The license may not give you all of the permissions necessary for your intended use. For example, other rights such as publicity, privacy, or moral rights may limit how you use the material.[^lic]
[^lic]: [Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

# Table of Contents
- [Introdution to Cybersecurity](#intro-to-it-security)
- [Types of Malware](#malware)
- [About Network Attacks](#network-attacks)
- [Symetric Encryption](#symmetric-encryption)
- [Asymmetric Cryptography](#asymmetric-cryptography)
- [Cryptography Real-world Usecases](#cryptography-applications)
- [Encryption Generation Linux Lab](#encryption-lab)
- [Generating Hash and Verifying Linux Lab](#hashing-and-hash-verification-lab)
- [Various Secuirty Methods](physical-privacy-and-security-components)
- [Securing Network Architecture](#securing-network-architecture)
- [Cyber Risks at Work](#cyber-risk-in-the-workplace)
- [Malware Library](#malware-library)

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

![syn_flood](https://i.imgur.com/yvyz6Ny.png)

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

### Hashing Rainbow Tables

![rainbow_table](https://i.imgur.com/uvn7F29.png)

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

![web_trust](https://i.imgur.com/ppxAYgc.png)

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

![ipsec](https://i.imgur.com/c1MJJx9.png)

__IPsec__ works by encrypting an IP packet and encapsulating the encrypted packet inside an IPsec packet. This encrypted packet then gets routed to the VPN end-point where the packet is de-encapsulated and decrypted then sent to the final destination. IPsec supports two modes of operations, transport mode and tunnel mode.
- While not a VPN solution itself, [__L2TP or layer two tunneling protocol__](https://tools.ietf.org/html/rfc3193) is typically used to support VPNs. A common implementation of L2TP is in conjunction with IPsec when data confidentiality is needed. Since L2TP doesn't provide encryption itself, it's a simple tunneling protocol that allows encapsulation of different protocols or traffic over a network that may not support the type of traffic being sent. L2TP can also just segregate and manage the traffic. ISPs will use L2TP to deliver network access to a customer's end point.
- For example, the combination of L2TP and IPsec is referred to as L2TP IPsec and was officially standardized in IETF RFC 3193.
- An important distinction to make in this setup is the difference between the tunnel and the secure channel. The tunnel is provided by L2TP which permits the passing of unmodified packets from one network to another. The secure channel, on the other hand, is provided by IPsec which provides confidentiality, integrity and authentication of data being passed.

### Cryptographic Hardware

![tmp](https://i.imgur.com/ISGmyih.png)

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

![file_encrypt](https://i.imgur.com/0NRUxho.png)

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

![oauth](https://i.imgur.com/Pdm0snx.png)

__OAuth__ _is an open standard that allows users to grant third party websites and applications access to their information without sharing account credentials._
- This can be thought of as a form of access delegation because access to the user's account is being delegated to the third party.
- Once confirmed, the identity provider will supply the third party with a token that gives them access to the user's information. This token can then be used by the third party to access data or services offered by the identity provider directly on behalf of the user.
- OAuth is commonly used to grant access to third party applications to APIs offered by large internet companies like Google, Microsoft and Facebook.
- Example: Let's say you want to use a third party meme creation website. This website lets you create memes using templates and gives you the option to save your creations and email them to your friends. Instead of the site sending the emails directly, which would appear to be coming from an address your friends wouldn't recognize. The site uses OAuth to get permission to send the memes using your email account directly. This is done by making an OAuth request to your email provider. Once you approve this request, the email provider issues an access token to the site which grants the site access to your email account. The access token would have a scope which says that it can only be used to access email, not other services associated with the account.
-  __OAuth permissions can be used in phishing style attacks to gain access to accounts without requiring credentials to be compromised__. This works by sending phishing emails to potential victims that look like legitimate OAuth authorization requests. Which asked the user to grant access to some aspects of their account through OAuth. Once the user grants access, the attacker has access to the account through the OAuth authorization token. [This was used in an OAuth based worm attack in early 2017.](https://www.theverge.com/2017/5/3/15534768/google-docs-phishing-attack-share-this-document-with-you-spam)
 - There was a rash of phishing emails that appear to be from a friend or colleague who wanted to share a Google doc. When the sharing link was followed, the victim was prompted to log in and authorized access to email, documents. And contacts for some third party service which only identified itself as the name Google Apps. But it was actually a malicious service that would then email contacts from their email account perpetuating the attack.

![oauthvopenid](https://i.imgur.com/y6zHBgq.png)

- It's important to distinguish between OAuth and open ID.
 - OAuth is specifically an authorization system and open ID is an authentication system though they're usually used together.
 - Open ID connect is an authentication layer built on top of OAuth point designed to improve upon open ID, and build better integration with OAuth authorizations.

![acl](https://i.imgur.com/e50qMhP.png)

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

![isp_accounting](https://i.imgur.com/8RIxAtH.png)

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

- _To protect against this rogue DHCP server attack, enterprise switches off a feature called __DHCP snooping___. A switch that has DHCP snooping will monitor DHCP traffic being sent across it. It will also track IP assignments and map them to hosts connected to switch ports. This basically builds a map of assigned IP addresses to physical switch ports. This information can also be used to protect against IP spoofing and ARP poisoning attacks.

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
- 802.1X with EAP-TLS offers the best protection for wireless networks, assuming proper and secure handling of the PKI aspects of it. But this option also requires a ton of added complexity and overhead. This is because it requires the use of a _radius server_ and an _additional authentication back-end_ at a minimum. If EAP-TLS is implemented, then _all the public key infrastructure components will also be necessary_. This adds even more complexity and management overhead. Not only do you have to _securely deploy PKI on the back-end first certificate management_, but a _system must be in place to sign the client certificates_. You also have to distribute them to each client that would be authenticating to the network. This is usually more overhead than many companies are willing to take on because of the security versus convenience trade-off involved.
  - __WPA2 with AES is the second best alternative__. A long and complex passphrase that wouldn't be found in a dictionary would increase the amount of time and resources and attacker would need to break the passphrase. Changing the SSID to something uncommon and unique would also make rainbow tables attack less likely. It would require an attacker to do the computations themselves, increasing the time and resources required to pull off an attack. 

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

## Network Software Hardening

Implementing network software hardening includes things like _firewalls, proxies, and VPNs._

- A __host-based firewall__ provides protection for mobile devices, such as a laptop that could be used in an untrusted, potentially malicious environment, like an airport Wi-Fi hotspot.
- Host-based firewalls are also useful for protecting other hosts from being compromised by corrupt device on the internal network. That's something a __network-based firewall__ may _not_ be able to help defend against. All major operating systems have built-in ones today.

![network_firewall](https://i.imgur.com/QjuIaAV.png)

- A __network-based firewall__ your router at home even has a network-based firewall built-in. .

![site_to_site_VPN](https://i.imgur.com/R2OIJtQ.png)

-  Remember, VPNs are commonly used to provide secure remote access and link two networks securely. The __site-to-site VPN__ can link two offices. Using a _VPN tunnel_, all traffic between the two offices can be secured using encryption.
- This lets the two remote networks join each other seamlessly. This way, clients on one network can access devices on the other without requiring them to individually connect to a VPN service.

![standard_proxy](https://i.imgur.com/knwj2KW.png)
- __Proxies__ can be really useful to protect client devices and their traffic. They also provide secure remote access without using a VPN.
  - Proxies also provide secure remote access _without_ using a VPN.
  - A standard web proxy can be configured for client devices. This allows web traffic to be proxy through a proxy server that we control for lots of purposes.
  - This configuration can be used for logging web requests of client devices. The devices can be used for logs and traffic analysis and forensic investigation.
  - The proxy server can be configured to block content that might be malicious, dangerous, or just against company policy. 

![reverse_proxy](https://i.imgur.com/YAC6Il2.png)

- __Reverse Proxy__ A reverse proxy can be configured _to allow secure remote access to web-based services __without__ requiring a VPN_.
  - By configuring a reverse proxy at the edge of your network, connection requests to services inside the network coming from outside are _intercepted by the reverse proxy_. They are then forwarded onto the internal service with _the reverse proxy acting as a relay_. These bridges communications between the remote client outside the network and the internal service.
  - This proxy setup can be secured even more by requiring the use of client TLS certificates, along with username and password authentication.
  - Specific __ACLs__ can also be configured on the reverse proxy to restrict access even more. Lots of popular proxy solutions support a reverse proxy configuration like _HAProxy, Nginx, and even the Apache_ web server.


#### About Proxies

- [HAProxy main documentation](http://www.haproxy.org/#docs)
- [HAProxy reverse proxy documentation](http://cbonte.github.io/haproxy-dconv/1.8/intro.html#3.3.1)
- [nginx main documentation](http://nginx.org/en/docs/)
- [nginx reverse proxy documentation](http://nginx.org/en/docs/beginners_guide.html#proxy)
- [Apache HTTP server main documentation](http://httpd.apache.org/docs/)
- [Apache HTTP server reverse proxy documentation](https://httpd.apache.org/docs/2.4/howto/reverse_proxy.html)

## Wireless Security

#### WEP 
__WEP__ or __Wired Equivalent Privacy__ was proven to be seriously bad at providing confidentiality or security for wireless networks. It was quickly discounted in 2004 in favor of more secure systems. [No one should be using WEP anymore.](https://doi.org/10.1007/3-540-45537-X_1)

 - Originally, WEP encryption was limited to 64-bit only because of US export restrictions placed on encryption technologies. Now, once those laws were changed, 128-bit encryption became available for use.
 - But this actually reduces the available keyspace to only valid ASCII characters instead of all possible hex values.

![wired_equivalent_privacy](https://i.imgur.com/K8v8QlA.png)

- WEP authentication originally supported two different modes; open system authentication and shared key authentication.
- The __open system mode__ didn't require clients to supply credentials. Instead, they were allowed to authenticate and associate with the access point.
  - But the access point would begin communicating with the client encrypting data frames with the _pre-shared_ WEP key.
  - If the client didn't have the key or had an incorrect key, it wouldn't be able to decrypt the frames coming from the access point or AP. It also wouldn't be able to communicate back to the AP. 
- __Shared key authentication__ worked by requiring clients to authenticate through a _four-step challenge response process_. This basically has the AP asking the client to prove that they have the correct key. Here's how it works:

> ![four_step_challenge_response](https://i.imgur.com/lAfFzjL.png)
> 1) The client sends an authentication request to the AP.
> 2) The AP replies with a clear text challenge a bit of randomized data that the client is supposed to encrypt using the shared WEP key.
> 3) The client replies to the AP with the resulting ciphertexts from encrypting this challenge text.
> 4) The AP verifies this by decrypting the response and checking it against the plain text challenge text. If they match, a positive response is sent back. 

- Does anything jump out at us potentially insecure in the scheme?
- We're transmitting both the plaintext and the ciphertext in a way that exposes both of these messages to potential eavesdroppers. This opens the possibility for _the encryption key to be recovered by the attacker_.
- But WEP's true weakness wasn't related to the authentication schemes. Its _use of the RC4 stream cipher and how the IVs were used to generate encryption keys_ led to WEP's ultimate downfall.
- When using a stream cipher like RC4, it's _critically important than an encryption key doesn't get reused_. This would allow an attacker to compare two messages encrypted using the same key and recover information.
- But the encryption key in WEP is just made up of the shared key, which doesn't change frequently.  Since the IV is made up of 24 bits of data, then total number of possible values is not very big by modern computing standards. That's only about 17 million possible unique IVs, which means after roughly 5,000 packets, an IV will be reused.
-  It's also important to call out that the IV is transmitted in _plain text_. This means an attacker just has to keep track of IVs and watch for repeated ones. The actual attack that lets an attacker recover the WEP key relies on weaknesses in some IVs and how the RC4 cipher generates a key-stream used for encrypting the data payloads. This lets the attacker reconstruct this key-stream using packets encrypted using the weak IVs.
- You can also take a look at open source tools that demonstrate this attack in action, like __Aircrack-ng or AirSnort__. _They can recover a WEP key in a matter of minutes_.

#### WPA
WPA or Wi-Fi Protected Access. WPA was designed as a short-term replacement that would be compatible with older WEP-enabled hardware with a simple firmware update.
- Under WPA, the pre-shared key is the Wi-Fi password you share with people when they come over and want to use your wireless network. This helped with user adoption because it didn't require the purchase of new Wi-Fi hardware.
-  WPS supports PIN entry authentication, NFC or USB for out-of-band exchange of the network details, or push button authentication. 
- The passphrase is fed into the __PBKDF2 or Password-Based Key Derivation Function 2__ along with the Wi-Fi network's SSID as a salt.
- This is then run through the HMAC-SHA1 function 4,096 times to generate a unique encryption key. The SSID salt is incorporated to help defend against [rainbow table attacks](###hashing-rainbow-tables). The 4,096 rounds of HMAC-SHA1 increase the computational power required for a brute force attack.

- __TKIP__ or the __Temporal Key Integrity Protocol__ implemented three new features that made it more secure than WEP. 
  - a more secure key derivation method was used to more securely incorporate the IV into the per packet encryption key. 
  - a sequence counter was implemented to prevent replay attacks by rejecting out-of-order packets.
  - a 64-bit MIC or message integrity check was introduced to prevent forging, tampering, or corruption of packets. 
- TKIP still use the RC4 cipher as the underlying encryption algorithm, but it addressed the key generation weaknesses of web by using a key mixing function to generate unique encryption keys per packet. It also utilizes 256-bit long keys.

#### WPS
The Wi-Fi Alliance introduced WPS in 2006. It provides several different methods that allow our wireless client to securely join a wireless network without having to directly enter the pre-shared key. This facilitates the use of very long and secure passphrases without making it unnecessarily complicated.
- WPS supports PIN entry authentication, NFC or USB for out-of-band exchange of the network details, or push button authentication. You've probably seen the push button mechanism. The push button mechanism works by requiring a button to be pressed on both the AP side and the client side. This requires physical proximity and a short window of time that the client can authenticate with a button press of its own.

![wpa_button](https://i.imgur.com/iT1b0i7.png)

- The PIN methods are really interesting and also where critical flow was introduced. The PIN authentication mechanism supports two modes:
1) The client generates a pin, which is then entered into the AP.
2) The AP has a pin typically _hard-coded into the firmware_, which is entered into the client.

-  It's the _second mode_ that is [vulnerable to an online brute force attack](https://www.kb.cert.org/vuls/id/723755). The PIN  is authenticated by the AP in halves. This means the client will send the first four digits of the AP, wait for a positive or negative response, and then send the second half of the pin if the first half was correct. _This means the correct pin can be guessed in only a maximum of 11,000 tries_. It sounds like a lot, but it really isn't.
   - Without any rate limiting, an attacker could recover the PIN and the pre-shared key in less than _four hours_.
   - Introducing a lockout period of one minute after three incorrect PIN attempts. This increases the maximum time to guess the pin from four hours to _less than three days_.

![changing_wifi_password_no_fix](https://i.imgur.com/0vLVIb6.png)
  - Changing your Wi-Fi password in a WPS configuration _wouldn't help_, because the PIN _hard-coded into the firmware_, __the attacker could just reuse the already recovered WPS PIN to get the new password__.

> Security Tip: If your company values security over convenience, __you should make sure that WPS isn't enabled on your APs__. Makes sure this feature is disabled on your APs management council. You might want to also verify the feature is actually disabled using a tool like [Kali Linux Wash](https://www.hackingtutorials.org/wifi-hacking-tutorials/wps-wifi-networks-with-kali-linux-wash/), which scans and enumerates APs that have WPS enabled. 
 
#### WPA2 
WPA2 is the second-best security protocol compated to 802.1X with EAP-TLS. The WPA and WPA2 Standard, also introduced in 802.1X authentication to Wi-Fi networks. It's usually called WPA2- Enterprise. The non-802.1X configurations are called either WPA2-Personal or WPA 2- PSK. Since they use a pre-shared key to authenticate clients

![cracking_wifi](https://i.imgur.com/OAQkMPF.png)

- WPA2 uses __CCMP or Counter Mode CBC-MAC Protocol__. This utilizes AES in counter mode, which _turns a block cipher into a stream cipher using a random seed value along with an incremental counter to create a key stream to encrypt data with_. It is based on the _AES cipher_, finally getting away from the insecure RC4 cipher. The CBC MAC Digest is computed first, then the resulting authentication code is encrypted along with the message using a block cipher. We're using AES in this case operating encounter mode.
![counter_mode_CBCMAC](https://i.imgur.com/9jRqezV.png)

> Secuirty Note: WPA2 can still be hacked. There are plenty of reports and videos that demonstrate the hackability of WPA2.

- WPA2 is still susceptible to an offline brute-force attack. This dictionary-based attack is dependent on the quality of the password guesses, and it does require a fair amount of computational power to calculate the PMK from the passphrase guesses and SSID values.This requires 4096 iterations of a hashing function which can be massively accelerated through the use of GPU-accelerated computation.
- Because of the bulk of the computations involving computing the PMK by incorporating the password guesses with the SSIDs, it's possible to pre-compute PMKs in bulk for common SSIDs and password combinations. [Rainbow tables](###hashing-rainbow-tables) are available for download for the top 1000 most commonly seen SSIDs, and one million passwords.
- Let's walk through the four-way handshake process that authenticates clients of the network. It'll help you understand how WPA2 can be broken. This process also generates the temporary encryption key that will be used to encrypt data for this client.

![four_message_WPA2](https://i.imgur.com/86pV7hh.png)

The four messages exchanged in order are the AP which sends ANonce to the client. The client then sends its ANonce to the AP. The AP sends the GTK and the client replies with an ACK confirming successful negotiation.
- The PTK is actually made up of five individual keys, each with their own purpose. 
- Two keys are used for encryption and confirmation of EAPoL packets and the encapsulating protocol carries these messages. 
- Two keys are used for sending and receiving message integrity codes and finally, there's a temporal key which is actually used to encrypt data.

> Wi-Fi Password Best Practices: A long and complex passphrase that wouldn't be found in a dictionary would increase the amount of time and resources and attacker would need to break the passphrase. Changing the SSID to something uncommon and unique would also make rainbow tables attack less likely. It would require an attacker to do the computations themselves, increasing the time and resources required to pull off an attack.

## Network Monitoring

#### Sniffing the Network
![sniffing_network](https://i.imgur.com/irHncwt.png)

- In order to monitor what type of traffic is on your network you need a mechanism to capture packets from network traffic for analysis and potential logging. __Packet sniffing or packet capture__ _is the process of intercepting network packets in their entirety for analysis._
- __Promiscuous mode__ _is a special mode for ethernet network interfaces that basically says give me all the packets._

> Note: admin or root privileges are needed to place an interface into promiscuous mode and to begin to capture packets.

- __Port mirroring__ allows the switch to take all packets from a specified port, port range or the entire VLAN and mirror the packets to a specified switch port.
- There's another handy the less advanced way that you can get access to packets in a switch network environment. You can insert a hub into the topology with the device or devices you'd like to monitor traffic on connected to the hub and our monitoring machine. Hubs are a quick and dirty way of getting packets mirrored to your capture interface. 

> Note: Hubs obviously have drawbacks though like reduced throughput and the potential for introducing collisions.

- But _if we wanted to capture and analyze all wireless traffic that we're able to receive in the immediate area_, we can place our wireless interface into a mode called __monitor mode__ which allows us to scan across channels to see all wireless traffic being sent by APs and clients.  To capture wireless traffic all you need is an interface placed into monitor mode. 
- You need to be near enough to the AP and client to receive a signal, and then _you can begin capturing traffic right out of the air_. There are a number of open source __wireless capture and monitoring utilities__, like __aircrack-ng and Kismet__.

- > Note: It's important to call out that if a wireless network is encrypted, you can still capture the packets, _but you won't be able to decode the traffic payloads without knowing the password for the wireless network_.

#### Wireshark and TCPDump
- __Tcpdump__ is _a super popular lightweight command line-based utility_ that you can use to capture and analyze packets. It does things like converting the source and destination IP addresses into the dotted quad format we're most used to and it shows the port numbers being used by the communications. 

![tcpdump](https://i.imgur.com/eU0zB3L.png)

> Breakdown of TCPDump: The first bit of information is fairly straightforward. It's a timestamp that represents when the packet on this line was processed by the kernel in local time. Next the Layer 3 protocol is identified. In this case, it's IPV4. After this, the connection quad is shown. This is the source address, source port, destination address, and destination port. Next the TCP flags and the TCP sequence number are set on the packet, if there are any. This is followed by the act number, TCP window size, then TCP options if there are any set. Finally, we have payload size in bytes. 

![wireshark_GUI](https://i.imgur.com/7f1bo1Y.png)

- __Wireshark__ is a GUI packet capture and analysis tool, and is superious to TCPDump in numerous ways:
  -  Wireshark can decode encrypted payloads if the encryption key is known.
  -  It can identify and extract data payloads from file transfers through protocols like SMB or HTTP.
  -  It has filter string fucntions. This allows filter rules like finding HTTP requests with specific strings in the URL, which would look like `http.request.uri matches q=wireshark`.
  -  But it's way more powerful when it comes to application and packet analysis compared to Tcpdump.
  -  it also understands and can follow TCP stream or sessions. This lets you quickly reassemble and view both sides of the TCP session so you can easily view the full two-way exchange of information between parties. 
  -  ability to decode WPA and WEP encrypted wireless packets if the passphrase is known. 
  -  It's also able to view Bluetooth traffic with the right hardware, along with USB traffic in other protocols like Zigbee. 
  -  It also supports file carving or extracting data payloads from files transferred over unencrypted protocols like HTTP file transfers or FTP.
  -  It's able to extract audio streams from unencrypted VOIP traffic. 

> WireShark GUI Breakdown: The list of packets are up top, followed by the layered representation of a selected packet from the list. Lastly, the X and ascii representation of the selected packet are at the bottom. The packet list view is color-coded to distinguish between different types of traffic in the capture. The color-coded is user configurable. The defaults are green for TCP packets, light blue for UDP traffic, and dark blue for DNS traffic. Black also highlights problematic TCP packets, like out-of-order or repeated packets. Above the packet list pane is a display filter box which allows complex filtration of packets to be shown. 

- __Traffic analysis__ is done using packet captures and packet analysis. Traffic on a network is basically a flow of packets. Now being able to capture and inspect those packets is important to understanding what type of traffic is flowing on our networks that we'd like to protect.

> How-to [enable promiscuous mode on Mac OS X](https://danielmiessler.com/blog/entering-promiscuous-mode-os-x/) and [Windows](http://lifeofageekadmin.com/?p=3601).

#### Intrusion Detection/Prevention Systems
![ids_ips](https://i.imgur.com/8Iaky8H.png)

> Note: The location of the NIDS must be considered carefully When you deploy a system. It needs to be located in the network topology in a way that it has access to the traffic we'd like to monitor. A good way that you can get access to network traffic is using the port mirroring functionality found in many enterprise switches. This allows all packets on a port range or entire villain to be mirrored to another port where our needs hosts would be connected. With this configuration, our NIDS machine would be able to see all packets flowing in and out of hosts on the switch segment.

- __Intrusion detection and prevention systems__ or __IDS/IPS__. IDS or IPS systems operate by monitoring network traffic and analyzing it.
  -  The difference between an _IDS_ and an _IPS_ system is that __IDS__ is _only a detection system_. It won't take action to block or prevent an attack when one is detected, it will only log and alert.
  -  But an __IPS system__ _can adjust firewall rules on the fly to block or drop the malicious traffic_ when it's detected.
  - [Snort](https://www.snort.org/) and [Zeek](https://zeek.org/) are an examples of __IPS__ systems.

![NID_system](https://i.imgur.com/VvkHisH.png)

- A __NIDS device__ _is a passive observer that only watches the traffic and __sends an alert if it sees something___. This is unlike a __NIPS device__, which monitors traffic, and _can take action on the traffic it's monitoring usually __by blocking or dropping the traffic___. The detection of threats or malicious traffic is usually handled through _signature-based detection_. 
  - __Signatures__ _are unique characteristics of known malicious traffic_. They might be specific sequences of packets or packets with certain values encoded in the specific header field.
  - The detection of threats or malicious traffic is usually handled through signature-based detection. Similar to how antivirus software detects malware.  But similar to antivirus, _less common or targeted attacks might not be detected by a signature-based system, since there might not be signatures developed for these cases_. It's also possible to create custom rules to match traffic that might be considered suspicious but not necessarily malicious.
  - If the traffic is found to be malicious, _a __signature__ can be developed from the traffic and incorporated into the system_. What actually happens when a NID system to detect something malicious? This is configurable, but usually the NID system would log the detection event along with a full packet capture of the malicious traffic.

#### Unified Threat Management (UTM)
Previously, you learned about several network security topics, including network hardening best practices, firewall essentials, and the foundations of IEEE 802.1X. In this reading, you will learn about a robust solution for network security, Unified Threat Management (UTM), along with its features, benefits, and risks.

UTM solutions stretch beyond the traditional firewall to include an array of network security tools with a single management interface. UTM simplifies the configuration and enforcement of security controls and policies, saving time and resources. Security event logs and reporting are also centralized and simplified to provide a holistic view of network security events.

__UTM options and configurations__
UTM solutions are available with a variety of options and configurations to meet the network security needs of an organization

- __UTM hardware and software options:__
  - Stand-alone UTM network appliance
  - Set of UTM networked appliances or devices
  - UTM server software application(s)
- __Extent of UTM protection options:__
  - Single host
  - Entire network

- __UTM security service and tool options can include:__
  - __Firewall__: Can be the first line of defense in catching phishing attacks, spam, viruses, malware, and other potential threats that attempt to access an organization’s network. Firewalls can be hardware devices or software applications. Firewalls filter and inspect packets of data attempting to enter and exit a managed network. Rules can be configured to permit or prevent certain types of packets from entering the network. 
  - __Intrusion detection system (IDS)__: Passively monitors packets of data and network traffic for unusual patterns that could indicate an attack. IDS devices can monitor entire networks (NIDS) or just a single host (HIDS). IDS identifies, logs, and alerts IT Support about suspicious traffic. However, IDS does not prevent an attack from occurring. This system gives IT Support professionals the opportunity to inspect flagged events to determine how to handle the threat on a case by case basis.   
  - __Intrusion prevention system (IPS)__: Actively monitors packets and network traffic for potential malicious attacks. IPS systems can be configured to automatically block attacks or to allow manual interventions. IPS devices can monitor entire networks (NIPS) or just a single host (HIPS).
  - __Antivirus software__: Uses a signature database to obtain the profiles of malicious files, such as spyware, Trojans, malware, worms, and more. The antivirus software monitors the organization’s network and systems for these virus signatures. Once identified, the software will block, quarantine, or destroy them.
  - __Anti-malware software__: Scans information streams for known malicious malware signatures and blocks threats. Additionally, anti-malware software can use heuristic analysis to detect novel malware threats by identifying key behaviors and characteristics. The software can also use sandboxing to isolate suspicious files. 
  - __Spam gateway__: Filters, identifies, and quarantines spam email. Spam gateways are network servers that use Domain Name Server (DNS) management tools to protect against spam.
  - __Web and content filters__: Block user access to risky and malicious websites. When a user attempts to access an unauthorized or suspicious website using a browser, the UTM web filter can prevent the website from loading. The filter can also be customized to block certain types of websites or specific URLs, like social media or other websites that might be a distraction in the workplace. 
  - __Data leak/loss prevention (DLP)__: Monitors outgoing network traffic for personal, sensitive, and confidential data. DLP includes a verification system to determine if the external data transfer is authorized or malicious, and can block unauthorized attempts.  
  - __Virtual Private Network (VPN)__: Encrypts data and creates a private “tunnel” to safely transmit the data through a public network. 

__Stream-based vs. proxy-based UTM inspections__
- UTM solutions offers two methods for inspecting packets in UTM firewalls, IPS, IDS, and VPNs:
  - __Stream-based inspection, also called flow-based inspection__: UTM devices inspects data samples from packets for malicious content and threats as the packets flow through the device in a stream of data. This process minimizes the duration of the security inspection, which keeps network data flowing at a faster rate than a proxy-based inspection.  
  - __Proxy-based inspection__: A UTM network appliance works as a proxy server for the flow of network traffic. The UTM appliance intercepts packets and uses them to reconstruct files. Then the UTM device will analyze the file for threats before allowing the file to continue on to its intended destination. Although this security screening process is more thorough than the stream-based inspection technique, proxy-based inspections are slower in the transmission of data.

__Benefits of using UTM__
- UTM solutions can offer multiple benefits to an organization:
  - UTM can be cost-effective: Reduces the time and resources needed to manage multiple stand-alone security tools. Purchasing a suite of integrated tools may also be less expensive than buying each tool separately. 
  - UTM is flexible and adaptable: Offers flexible solutions and options for security management. The security services and tools in a UTM can be implemented in any combination that is appropriate for each network environment.
  - UTM offers integrated and centralized management: Consolidates multiple security tools into a central management console. This simplifies monitoring and addressing security threats, as well as streamlines the management of  updates to the UTM components. The central management feature also helps IT Support staff identify and stop the full extent of an attack across an entire network. 

- __Risks of using UTM__
  - __UTM can become a single point of failure in a network security attack__: If an attack disables an entire UTM solution, there would be no other backup security services or tools to stop that attack. One of the core principles of information systems management is to design and implement redundant, backup, and failover systems. When one element of an IT system is attacked or experiences a failure, there should always be a backup or parallel system to replace it. 
  - __UTM might be a waste of resources for small businesses__: Small businesses may not need a robust security solution like UTM. The time and money needed to purchase, implement, and manage a complex UTM system may not provide a significant return on security benefits for a smaller network. Cybercriminals are more likely to attack larger targets.

- __Key Takeaways__
  - Unified Threat Management (UTM) systems offer multiple options in a comprehensive suite of network security tools. UTM solutions can be implemented as hardware and/or software and can protect either a single host or an entire network. 
  - UTM security services and tool options include firewalls, IDS, IPS, antivirus and anti-malware software, spam gateways, web and content filters, data leak/loss prevention, and VPN services. 
  - The benefits of using a UTM solution include having a cost-effective network security system that is flexible and adaptable with a management console that is integrated and centralized. The risks of using UTM include creating a single point of failure for a network security system and it might be an unnecessary use of resources for small businesses.

#### Securing Home Network
Home networks have vulnerabilities to various types of attacks. The most common security attacks on home networks include:

- __Meddler in the middle attacks__ allows a meddler to get between two communication devices or applications. The meddler then replies as the sender and receiver without either one knowing they are not communicating with the correct person, device, or application. These attacks allow the meddler to obtain login credentials and other sensitive information. 

![meddlernmiddle](https://i.imgur.com/N8ABliD.png)

- __Data Theft__ is when data within the network is stolen, copied, sent, or viewed by someone who should not have access. 
- __Ransomware__ uses malware to keep users from accessing important files on their network. Hackers grant access to the files after receiving a ransom payment. 

- __Keeping Home Networks Secure__
To protect company data, employees working from home need to take steps to improve the security of their home networks. Home networks can have added protection without expensive equipment or software. You can take steps to keep home networks more secure: 
  - __Change the default name and password__ using the same password guidelines as your company. 
  - __Limit access to the home network__ by not sharing access credentials outside of trusted individuals. 
  - __Create a guest network__ that allows guests to connect to the internet but not your other devices.
  - __Turn on WiFi network encryption__ requiring a password before a device can access the internet. 
  - __Turn on the router’s firewall__ to prevent unwanted traffic from entering or leaving your wireless network without your knowledge. Regularly update your router firmware.
  - __Update to the newest WiFi standard__ which is the most secure standard for home WiFi.

Another security measure that a company can take is for employees to work over a virtual private network, or VPN. Using a VPN creates an encrypted, secure internet connection through which employees can access company data. 

# System Hardening
Our end goal overall is risk reduction. Two important terms to know when talking about security risks are attack vectors and attack surfaces.
-  An __attack vector__ is a method or mechanism by which an attacker or malware gains access to a network or system.
  -  Some attack vectors are email attachments, network protocols or services, network interfaces and user input. These are different approaches or paths that an attacker could use to compromise the system, if they're able to exploit it. 
- An __attack surface__ is the sum of all the different attack vectors in a given system.
  - Think of this as the combination of all possible ways an attacker could interact with our system regardless of known vulnerabilities.
  - Make sure to think of all avenues that an _outside actor could interact with our systems_ as a potential attack surface.
- The less complex something is, the less likely there will be undetected flaws. So make sure to disable any extra services or protocols, if they're not totally necessary, then get them out of there.
- Every additional surface that's operating represents additional attack surfaces that could have an undiscovered vulnerability. That vulnerability could be exploited and lead to compromise. __Only allow access when totally necessary.__
  - So for example, it's probably not necessary for employees to be able to access printers directly from outside of the local network. You can just adjust firewall rules to prevent that type of access.
  - Another way to keep things simple is to reduce your software deployments. Instead of having five different software solutions to accomplish five separate tasks, replace them with one unified solution, if you can.
  -  You should also make sure to disable unnecessary or unused components of software and systems deployed.
  -   Lots of consumer operating systems ship a bunch of default services and software enabled right out of the box, that you probably won't need. For example, TelNet access for a managed switch has no business being enabled in a real-world environment. You should disable it immediately if you find it on a device.
  -   Any vendor specific API access should also be disabled if you don't plan on using these services or tools. 

### Host-based Firewalls
A.K.A., Layered approach to security. What if our access control measures are bypassed or fail in some unforeseen way. As an IT support specialist, this is exactly what you want to think about. How do we keep this component secure if the security systems above it have failed?
- Host-based firewalls are important to creating multiple layers of security.
- Our network-based firewall has a duty to protect our internal network by filtering traffic in and out of it. While the host-based firewall on each individual host, protects that one machine.
- Start with an implicit deny rule, then only permit traffic that we know and trust through. You can think of this as starting with a perfectly secure firewall configuration and then poking holes in it for the specific traffic we require.
-  A host-based firewall plays a big part in reducing what's accessible to an outside attacker. It provides flexibility while only permitting connections to selective services on a given host from specific networks or IP ranges.

![bastion_hots](https://i.imgur.com/jQULZaD.png)
-  These are called __bastion hosts or networks__, and are specifically hardened and minimized to reduce what's permitted to run on them. __Bastion hosts__ are usually _exposed to the Internet_, so you should pay special attention to hardening and locking them down to reduce the chances of compromise.
   - They can also be used as a gateway or access portal into more sensitive services like core authentication servers or domain controllers.
   - Applications that are allowed to be installed and run on these hosts, would also be restricted to those that are strictly necessary since these machines have one specific purpose.
- Part of the __host-based firewall__ rules will likely also provide ackles that allow access from the VPN subnet. It's good practice to keep the network that VPN clients connect into separate using both subnetting and VLANs.
-  It's good practice to _keep the network that VPN clients connect into separate using both subnetting and VLANs_. This gives you more flexibility to enforce security on these VPN clients. It also lets you build additional layers of defenses.

![VPN_tunnel_bastion](https://i.imgur.com/zQUHNcI.png)

- If the users of the system have administrative rights than they have the ability to change firewall rules and configurations.
- If management tools allow it, you should also prevent the disabling of the host-based firewall. This can be done with Microsoft Windows machines when administered using Active Directory as an example.

### Logging and Alerting
![log_alert](https://i.imgur.com/A5IKTIm.png)
All systems and services running on hosts will create logs of some kind with different levels of detail. It depends on what its logging and what events it's configured to log.
- So an authentication server would log every authentication attempt whether it's successful or not.
- A firewall would log traffic that matches rules with details like source and destination addresses and ports being used.
- When there are a large number of systems located around your network, each with their own log format, it can be challenging to make meaningful sense of all this data. This is where __security information and event management systems or SIEMS__ come in.
  - A SIEM can be thought of as a centralized log server it is some extra analysis features too.
  - You can _think of SIEM as a form of centralized logging_ for security administration purposes. Some examples of logging servers and SIEM solutions are the open source, rsyslog, Splunk Enterprise Security, IBM Security Qradar and RSA Security Analytics.
  - A SIEM system gets logs from a bunch of other systems. It consolidates the logs from all different places and places it in one centralized location. This makes handling logs a lot easier.
  - By maintaining logs on a dedicated system, it's easier to secure the system from attack. _Logs are usually targeted by attackers after a breach so that they can cover their tracks._ By having critical systems send logs to remote logging server that's locked down, the details of a breach should still be logged.
  - A forensics team will be able to reconstruct the events that led to the compromise.
- __Normalization__ is the process of taking log data in different formats and converting it into a standardized format that's consistent with a defined log structure.
  - For example, log entries from our firewall may have a timestamp using a year, month and day format. While logs from our client machines may use day, month, year format.
  - To normalize this data, you choose one standard date format then you define what the fields are for the log types that need to be converted. When logs are received from these machines, the log entries are converted into the standard that we defined and stored by the logging server.
  - If you log too much info, it's difficult to analyze the data and find useful information plus storage requirements for saving the logs become expensive very quickly.
  - But if you log too little then the information won't provide any useful insights into your systems and network. Finding that middle ground can be difficult. It will vary depending on the unique characteristics of the systems being monitored and the type of activity on the network.
  - No matter what events are logged, all of them should have information that will help understand what happened and reconstruct the events.
  - Timestamps are super important to understanding when an event occurred. Fields like source and destination addresses will tell us who was talking to whom. For application logs you can grab useful information from the logged in user associated with the event and from what client they used.
  - __You should pay attention to patterns and connections between traffic__.
    - So if you're seeing a _large percentage of Windows hosts, all connecting to specific address outside your network_ that might be worth investigating, it could signal a malware infection. 
  - Once logs are centralized and standardized you can write automated alerting based on rules.
    - Maybe you'll want to define an alert rule for repeated unsuccessful attempts to authenticate to a critical authentication server.
    - You can also write some of your own monitoring and alert systems. 
    - It can be useful to break down things like commonly used protocols in the network. Quickly see the top talkers in the network and view reported errors over time to reveal patterns.

__User Account Control (UAC)__
User Account Control (UAC) allows IT administrators to create standard user accounts with limited access rights and privileges for end users. This configuration can prevent users from installing unauthorized programs, changing system settings, tampering with firewalls, and more. In order to perform these types of tasks, administrator credentials must be provided. For less restrictive controls, UAC provides the option to grant end users local administrative privileges for approved activities that require administrative privileges. For more restrictive controls, UAC can require global administrator credentials be entered for each and every administrative change the user attempts to make.

### Anti-virus Protection
Antivirus software is _signature-based_. This means that it has a database of signatures that identify known malware like the unique file hash of a malicious binary or the file associated with an infection. Antivirus software will monitor and analyze things like new files being created or being modified on the system in order to watch for any behavior that matches a known malware signature. If it detects activity that matches the signature, depending on the signature type, it will attempt to block the malware from harming the system. But some signatures might only be able to detect the malware after the infection has occurred. In that case, it may attempt to quarantine the infected files. If that's not possible, it'll just log and alert the detection event at a high level. This is how all antivirus products work.
 - There are two issues with antivirus software though.
   - The first is that they depend on antivirus signatures distributed by the antivirus software vendor.
   - The second is that they depend on the antivirus vendor discovering new malware and writing new signatures for newly discovered threats.
 -  Antivirus which is designed to protect systems, actually represents an additional attack surface that attackers can exploit.
   - It takes arbitrary and potentially malicious binaries as input and performs various operations on them. Because of this, there are a lot of complex code where very serious bugs could exist. Exactly, this kind of vulnerability was found in the sofas antivirus engine back in 2012.
   - Then why are we still recommending it as a core piece of security design? The short answer is this, it protects against the most common attacks out there on the Internet. The really obvious stuff that still poses a threat to your systems still needs to be defended against. Antivirus is an easy solution to provide that protection.
   - It doesn't matter how much user education you instill in your employees, there will still be some folks who will click on an email that has an infected attachment. A good way to think about antivirus in today's very noisy external threat environment, is like a filter for the attack noise on the internet today. It lets you remove the background noise and focus on the more important targeted or specific threats.

__Binary Whitelisting Anti-virus__

![binary_whitelisting](https://i.imgur.com/idLkdO7.png)

- If antivirus can't protect us from the threats we don't know about, how do we protect against the unknown that's out there? Well, anti virus operates on a blacklist model, checking against a list of known bad things and blocking what gets matched.
- There's a class of anti malware software that does the opposite. Binary whitelisting software operates off a white list. It's a list of known good and trusted software and only things that are on the list are permitted to run. Everything else is blocked.
- Now, imagine if you had to get approval before you could download and install any new software, that would be really annoying, don't you think? Now, imagine that every system update had to be white listed before it could be applied. Obviously, not trusting everything wouldn't be very sustainable. It's for this reason that binary whitelisting software can trust software using a couple different mechanisms.
  - The _first is using the unique cryptographic hash_ of binaries which are used to identify unique binaries. This is used to whitelist individual executables. The other trust mechanism is a software signing certificate.

![binary_whitelisting2](https://i.imgur.com/qdUlFNk.png)

- Can you guess the downside here? Each new code signing certificate that's trusted represents an increase in attack surface. _An attacker could compromise the code signing certificate of a software vendor that your company trusts. And use that to sign malware that targets your company._ __That would bypass any binary whitelisting defenses in place.__ Not good.

> This exact scenario happened back in [http://www.crn.com/news/security/240148192/bit9-admits-systems-breach-stolen-code-signing-certificates.htm](2013 to a binary whitelisting software company when Bit9 was hacked). Hackers managed to breach their internal network and found an unsecured virtual machine. It had a copy of the code signing certificates private key. _They stole that key and used it to sign malware_ that would have been trusted by all their software installations by default.

### Disk Encryption
![FDE](https://i.imgur.com/GTat92O.png)

- __Full disk encryption or FDE__ is an important factor in a defense in depth security model. It provides protection from some physical forms of attack.
- Having the disk fully encrypted protects from data theft and unauthorized tampering even if an attacker has physical access to the disk.
- Without also knowing the encryption password or having access to the encryption key the data on the hard drive is just meaningless gibberish.
- FDE drives are _still vulnerable to cyber attacks_:
  - In order for a system to boot if it has an FDE set up, there are some critical files that must be accessible. They need to be available before the primary disk can be unlocked and the boot process can continue. Because of this all FDE setups have an unencrypted partition on the disk which holds these critical boot files. Examples include things like the kernel and bootloader that are critical to booting the operating system.
  - These bootup files are actually vulnerable to being replaced with modified potentially malicious files by an attacker with physical access.
  - While it's possible to compromise a machine this way it would take a sophisticated and determined attacker to do it. There's also protection against this attack in the form of the __secure boot protocol__ which is part of the UEFI specifications.

![secure_boot](https://i.imgur.com/NjkcfWL.png)

- __Secure boot__ _uses public key cryptography to secure these encrypted elements of the boot process_. It does this by integrated code signing and verification of the boot files. Initially secure boot is configured with what's called a platform key, which is the public key corresponding to the private key used to sign the boot files.
  - Initially secure boot is configured with what's called a __platform key__, _which is the public key corresponding to the private key used to sign the boot files_. This platform key is written to firmware and is used at boot time to verify the signature of the boot files. Only files correctly signed and trusted will be allowed to execute.
  - When you implement a full disk encryption solution at scale, it's super important to think about how to handle cases where passwords are forgotten. 
  - If the pass phrases forgotten then the contents of the disk aren't recoverable, _yikes_. This is why lots of enterprise disk encryption solutions have a __key escrow__ functionality. __Key escrow__ _allows the encryption key to be securely stored for later retrieval by an authorized party._ So if someone forgets the passphrase to unlock their encrypted disk for their laptop the systems administrators are able to retrieve the escrow key or recovery pass phrase to unlock the disk.
- You should compare full disk encryption against __file based encryption__. _That's where only some files or folders are encrypted and not the entire disk._ This is usually implemented as home directory encryption. It serves a slightly different purpose compared to FDE. Home directory or file based encryption only guarantees confidentiality and integrity of files protected by encryption.

# Cyber Risk in the Workplace
If you're responsible for an organization of users, there's a delicate balance between security and user productivity. We've seen this balance in action when we dove into the different security tools and systems together. Before you start to design a security architecture, you need to define exactly what you'd like it to accomplish. This will depend on what your company thinks is most important. It will probably have a way it wants different data to be handled and stored.

### Security Goals
- Does your cyber security instance require certain compliance standards? For example:

- Protected Health Information: This information is regulated by the Health Insurance Portability and Accountability Act (HIPAA). It is personally identifiable health information that relates to:
  - Past, present, or future physical or mental health or condition of an individual
  - Administration of health care to the individual by a covered provider (for example, a hospital or doctor)
  - Past, present, or future payment for the provision of health care to the individual
- Credit Card or **Payment Card Industry** (**PCI**) Information: __PCI DSS__, or __Payment Card Industry Data Security Standard__ This is information related to credit, debit, or other payment cards. PCI data is governed by the Payment Card Industry Data Security Standard (PCI DSS), a global information security standard designed to prevent fraud through increased control of credit card data.
- **Personally Identifiable Information** (**PII**): PII is a category of sensitive information associated with a person. Examples include addresses, Social Security Numbers, or similar personal ID numbers.
- **Federal Information Security Management Act** (**FISMA**) compliance: FISMA requires federal agencies and those providing services on their behalf to develop, document, and implement specific IT security programs and to store data on U.S. soil. For example, organizations like NASA, the National Institutes of Health, the Department of Veteran Affairs—and any contractors processing or storing data for them—need to comply with FISMA.
- **Export Administration Regulations** (**EAR**) compliance: EAR is a set of U.S. government regulations administered by the U.S. Department of Commerce’s Bureau of Industry and Security (BIS). These regulations govern the export and re-export of commercial and dual-use goods, software, and technology. Dual-use goods are items that can be used both for civilian and military applications. These goods are heavily regulated because they can be classified for civilian use and then transformed for military purposes.
- **Digital rights management** (**DRM**): Digital Rights Management (DRM) technologies can help ensure data regulations compliance. DRM technology comes in the form of either software or hardware solutions. Organizations can use these DRM capabilities to protect sensitive data. DRM enables organizations to track who has viewed files, control access, and manage how people use the files. It also prevents files from being altered, duplicated, saved, or printed. DRM can help organizations comply with data protection regulations. Content creators can also use DRM applications to restrict what users can do with their material. They can encrypt digital media so only someone with the decryption key can access it. This gives content creators and copyright holders a way to:
  - Restrict users from editing, saving, sharing, printing, or taking screenshots of content or products
  - Set expiration dates on media to prevent access beyond that date or limit the number of times users can access the media
  - Limit access to specific devices, Internet Protocol (IP) addresses, or locations, such as limiting content to people in a specific country
- Build and maintain a secure network and systems
- Protect cardholder data
- Maintain a vulnerability management program
  - The first requirement is to protect all systems against malware and regularly update antivirus software or programs.
  - The second is to develop and maintain secure systems and applications. You'll find more detailed implementation procedures within these requirements. They'll cover things like ensuring all systems have anti-virus software installed and making sure the software is kept up-to-date.
  - They also require that scans are run regularly and logs are maintained.
  - There are also requirements for ensuring systems and software are protected against known vulnerabilities by applying security patches at least one month from the release of a security patch.
- Implement strong access control measures
  - The first is to restrict access to cardholder data by business need to know (password authentication for system access and two-factor authentication for remote access)
  - The second is to identify and authenticate access to system components.
  - The third is to restrict physical access to cardholder data (keep in mind since we need to protect systems and data from both _physical_ theft and _virtual_ attacks.)
-  Regularly monitor and test networks
  - This refers to things like setting up and configuring intrusion detection systems and conducting vulnerability scans of the network
  - Just having the systems in place isn't enough. It's really helpful to test defense systems regularly to make sure that they provide the protection that you want. It also ensures that the alerting systems are functional.
-  Maintain an information security policy
  - Maintain a policy that addresses information security for all personnel.
  - The responsibility of information security isn't only on the security teams. Every member of an organization is responsible for information security.
  - That's why having well-thought-out security policies in place also need to be easy to find and easy to read.
  
  ### Measuring and Assessing Risk
  Security is all about determining risks or exposure, understanding the likelihood of attacks, and designing defenses around these risks to minimize the impact of an attack. Security risk assessment starts with __threat modeling__.
- First, we identify likely threats to our systems, then we assign them priorities that correspond to severity and probability. We do this by brainstorming from the perspective of an outside attacker, putting ourselves in a hacker shoes. It helps to start by figuring out what high-value targets an attacker may want to go after. From there, you can start to look at possible attack vectors that could be used to gain access to high-value assets.
  - High-value data usually includes account information like usernames and passwords. Typically, any kind of user data is considered high-value, especially if payment processing is involved.
- __Vulnerability scanners__ are services that run on your system within your control that conduct periodic scans of configured networks. 
![vul_scanners](https://i.imgur.com/3HHRclN.png)
  - One way to find these out is to perform regular vulnerability scanning. Some of these tools are [Nessus](https://www.tenable.com/products/nessus-vulnerability-scanner), [OpenVAS](http://www.openvas.org/), and [Qualys](https://www.qualys.com/forms/freescan/).
  - The service then conducts scans to find and discover hosts on the network. Once hosts are found, either through a ping sweep or port scanning, more detailed scans are run against discovered hosts. Scans upon scans upon scans.
  - A port scan of either common ports or all possible valid ports is conducted against discovered hosts to determine what services are listening. These services are then probed to try to discover more info about the type of service and what version is listening on the relevant port.
  - This information can then be checked against databases of known vulnerabilities. If a vulnerable version of a service is discovered, the scanner will add it to its report. Once the scan is finished, the discovered vulnerabilities and hosts are compiled in a report. That way an analyst can quickly and easily see where the problem areas are on the network.
  - Vulnerability scanning can _only detect __known__ and disclosed vulnerabilities_ and insecure configurations. That's why it's important for you to have an automated vulnerability scan conducted regularly.
  - Severity of vulnerability or __Common Vulnerability Scoring System__ (__CVSS__) takes into account a number of things like:
    - how likely the vulnerability is to be exploited
    - type of access the vulnerability would provide to an attacker and whether or not it can be exploited remotely or not
- __Penetration testing__ is the _practice of attempting to break into a system_ or network to verify the systems in place.
  - The results of the penetration testing reports will also show you where weak points or blind spots exist. These tests help improve defenses and guide future security projects.

### Privacy Policy
When you're supporting systems that handle customer data, it's super-important to protect it from unauthorized and inappropriate access. It's not to defend against external threats. It also protects the data against misuse by employees. This type of behavior would fall under your company's privacy policies.
-  Privacy policies oversee the access and use of sensitive data. They also define what appropriate and authorized use is and what provisions or restrictions are in place when it comes to how the data is used.
- you also need a way to enforce these policies. Periodic audits on cases where sensitive data was accessed can get you there. This was enabled by our logging and monitoring systems.
- Auditing data access logs is super important. It helps us ensure that sensitive data is only accessed by people who are authorized to access it and that they use it for the right reasons.
- It's good practice to apply the principle of least privilege here. By not allowing access to this type of data by default, you should require anyone that needs access to first make an access request with a justification for getting the data.
  - They should be required to specify what data they need access to.
  - Also have a time limit that should be called out in the request.
  - Any access that doesn't have a corresponding request should be flagged as a high priority potential breach.
- Divide data into two types: _sensitive data_ and _non-sensitive_.
  - If something is considered sensitive or confidential, have stipulations that this data shouldn't be stored on media that's easily lost or stolen, like USB sticks or portable hard drives.
  - It also makes sense to include laptops and mobile devices, like phones and tablets in the removable media classification. 

### Data Destruction
Data destruction is removing or destroying data stored on electronic devices  so that an operating system or application cannot read it. Data destruction is required when a company no longer needs a device, when there are unused or multiple copies of data, or you are required to destroy specific data. 

There are three categories of data destruction methods: recycling, physical destruction, and third-party destruction.

#### Recycling
Recycling includes methods that allow for device reuse after data destruction. This option is recommended if you hope to reuse devices internally, sell surplus equipment, or your devices are on loan and are due to be returned. Standard recycling methods include the following:
- __Erasing/wiping__: cleans all data off a device’s hard drive by overwriting it. Erasing or wiping data can be done manually or with data-destruction software. This method is practical when you only have a few devices that need data destroyed, as it takes a long time. Note that it may take multiple passes to wipe highly sensitive data completely. 
- __Low-level formatting__: erases all data written on the hard drive by replacing it with zeros. Low-level reformatting can be done using a tool such as [HDDGURU](https://hddguru.com/) on a PC or the Disk Utility function on a Mac. 
- __Standard formatting__: erases the path to the data and not the data itself. Both PCs and Macs have internal tools that can perform a standard format, Disk Management on a PC or Disk Utility on a Mac. _Note that standard formatting does not remove the data from the device, enabling data rediscovery using software._

#### Physical Destruction
Physical destruction includes any method that physically destroys a device to make it difficult to retrieve data from it. You should only use physical destruction if you do not need to reuse the device. However, _only completely destroying the device ensures the destruction of all data with physical methods_. Physical destruction methods include the following:

- __Drilling__ holes directly into the device wipes data out on the sections where there are holes. However, _individuals can recover data from the areas that are still intact_.
- __Shredding__ includes the physical shredding of hard drives, memory cards, CDs, DVDs, and other electronic storage devices. Shredding reduces the potential for recovery. Shredding requires special equipment or outsourcing to another facility. 
- __Degaussing__ uses a high-powered magnet which destroys the data on the device. This method effectively destroys large data storage devices and renders the hard drive unusable. As electronic technology changes, _this method may become obsolete_.
- __Incinerating__ destroys data by burning the device. Most companies do not have an incinerator on-site. Devices need to be transported to a facility for incineration. Due to this, _devices can be lost or stolen in transit_.

### User Habit
You can build the world's best security systems, but they won't protect you if the users are going to be practicing unsafe security. If a user writes their password on a Post-it Note, sticks it to their laptop, then leaves the laptop unlocked and unintended at a cafe, you could have a disaster on your hands.
- You should never upload confidential information onto a third-party service that hasn't been evaluated by your company.
-  If we require 20-character passwords that have to be changed every three months, our _users will almost definitely write them down_.  Since direct brute-force attacks against authentication infrastructure should be easily detected and blocked by intrusion prevention systems, they can be considered pretty low-risk, but the theft of a password database would be a super serious breach.
-  Now, we can relax the password requirements a bit and not ask for overly long passwords because of password databases. Password reuse is another common user behavior. People don't want a bunch of passwords to memorize.
-  it's important to make sure employees use new and unique passwords and don't reuse them from other services. It's also important to have a password change system check against old passwords.
-   A much greater risk in the workplace that users should be educated on is credential theft from phishing emails. Phishing emails are pretty effective. If an email that seems authentic actually leads to a fake login page, users can blindly enter their credentials into the fake site and disclose their credentials to an attacker.
-  You can also combat phishing attacks with good spam filtering combined with good user education. 

> If someone enter their password into a phishing site or even suspects they did, it's important to change their password as soon as possible. If you can, your organization should try to detect these types of password disclosures using tools like Password Alert.

### Third-party Security
In some cases, you have to trust that third party with a lot of potentially sensitive data or access. So how do you make sure that you aren't opening yourself up to a ton of unnecessary risk? Sometimes, vendors will perform tasks for you so they have access to your network and systems. In these cases, it's also important to understand how well secured third party is, a compromise of their infrastructure could lead to a breach of your systems.  
- Vendor security assessments/questionnaire
  - You ask vendors to complete a questionnaire that covers different aspects of their security policies, procedures and defenses. The questionnaire is designed to determine whether or not they've implemented good security designs in their organization.
  - Google recently made their __[vendor security assessment questionnaires available for free](https://vsaq-demo.withgoogle.com/)__. This is a great starting point to design your own vendor security assessment questionnaire.
  - without a way to verify or prove what's stated in the questionnaire. You have to trust that the company is answering honestly
- Some of the information on the questionnaire can be verified like third party security audit results and penetration testing reports. In the case of third party software, you might be able to conduct some basic vulnerability assessments and tests to ensure the product has some reasonable security.
  - Let's say the vendor company requires remote access to the infrastructure device to perform maintenance. If that's the case, then make appropriate adjustments to firewall rules to restrict this access.
  - If the vendor lets you, evaluate the hardware in a lab environment, first, there you can run in depth vulnerability assessments and penetration testing of the hardware.

### Security Training & Awareness
To help create this context, it's important for employees to __have a way that they can ask security questions and raise security concerns__. This could be a mailing list where users can ask questions about security concerns or to report things they suspect are security risks. Having the designated communication channel where people can feel comfortable asking questions and getting clear answers back is super important.

- Think of the small things we do every day when we use our computers:
  - Just entering your password to log in
  - Locking your screen when you walk away from your computer is helpful.
  - Being careful about entering your password on websites and check the address of the site you're authenticating against.

- Mandated security training should cover the most common attack types and how to avoid falling victim to them. This includes things like phishing emails and best practices around password use. These trainings often include scenarios that can help test the user's understanding of a particular topic.

### Inicent Response and Recovery
- Contain the incident (isolate infected machine from rest of network to prevent any lateral spread of malware).
- Power down, disconnect, and set aside for forensic analysis.
  - Forensic analysis may need to be done to analyze the attack. This is especially true when it comes to a malware infection. In the case of forensic analysis, affected machines might be investigated very closely to determine exactly what the attacker did. This is usually done by taking an image of the disk, essentially making a virtual copy of the hard drive. This lets the investigator analyze the contents of the disk without the risk of modifying or altering the original files. If that happened, it would compromise the integrity of any forensic evidence. Usually evidence gathering is also part of the incident response process. This provides evidenced to law enforcement if the organization wants to pursue legal action against the attackers.
- Restore using a _clean_ backup (pre-malware infection) of  machine to a new machine for the enduser to continue workflow.
  - Depending on the severity of the compromise or infection, it might be necessary to rebuild the system from the ground up. Clean up will typically involve restoring from a backup point to a known good configuration. Infected or corrupted system files can be restored from known good copies. Sometimes cleanup can be very simple and quick.
- Monitor victim's machine extra closely.
  - That's when systems need to be thoroughly tested to make sure proper functionality has been restored. Usually, affected systems would also remain under close watch, sometimes with additional detailed monitoring and logging enabled. This is to watch for any additional signs of an intrusion in case something was missed during the cleanup. It's also possible that the attacker will attempt to attack the same target again. There's a very high chance that they use the same or similar attack methodology on other targets in your network.
- Get a lawyer involved.
   - Because an incident can have legal implications for the company, a lawyer should be available to consult and advise on the legal aspects of the investigation. It's crucial in order to avoid complications or issues of liability.
- Work with forensics team to determine how the machine was breached and make necessary improvements.
  - Update firewall rules and ACLs if an exposure was discovered in the course of the investigation. Create new definitions and rules for intrusion detection systems that can watch for the signs of the same attack again. Stay vigilant and prepared to protect your system from attacks. Remember that at some point, some security breach will happen, just they come and execute your plan to counter attack the breach.

### Bring Your on Device (BYOD)
Today, an increasing number of companies permit employees to bring their own devices to work. This trend started with employees requesting permission to carry a single smartphone rather than carrying one phone for work and one for personal use. BYODs can become dangerous security threats to companies’ data and networks. IT departments do not have the same level of control over the security of BYOD devices as they would with company-owned devices. Some of the potential threats BYODs pose to company networks, resources, and data include:
- __Loss or theft__ could result in an organization’s data being stolen or the lost device being used to gain unauthorized access to a company’s network.
- __Data leakage__ losses can happen when a computing device is lost or compromised; when an employee accidentally saves or sends confidential information to the wrong destination; when a disgruntled employee exposes data maliciously; or when viruses, malware, phishing attacks, etc. penetrate organizations’ networks.   
- __Data portability__ losses can occur when former employees take company data with them on their BYOD when they resign or are fired by the organization. 
- __Security vulnerabilities__ are any type of weakness in the security of a device or network that provides access for a threat to penetrate the system.
- __Meddler in the middle attacks (MITM)__ occur when an attacker monitors the data transfers between two sources with the intent to copy and/or interfere with that information. One of the most common opportunities for an MITM attack arises  when a mobile device accesses important information through a public Wi-Fi connection, such as at a hotel or restaurant. 
- __Malware__ is malicious software that can be used to steal, modify, or delete data. It can also be used to gain unauthorized access to a device or network.
- __Jailbreaking__ happens when a manufacturer’s protective restrictions are removed on a mobile device. Without these restrictions, a device becomes vulnerable to the risk of the user unknowingly installing malicious software.

#### BYOD Solutions
To mitigate these threats, organizations and their IT departments should design security policies for BYOD use inside company networks. Some preventative steps could include:

- Develop a bring your own device (BYOD) policy: IT departments and organizations can create written policies that detail the minimum technology requirements for permitted BYODs, provide instructions for employees on how to properly secure their devices, and list the rules for safe data access and storage. 

- __Use Mobile Device Management (MDM) software__: MDM software can be used to enforce BYOD policy requirements for mobile devices to help secure company data and networks. IT departments can use MDM software to: 
  - Automatically install apps and updates, including antivirus and anti-malware software
  - Configure secure connections to an organization’s wireless networks 
  - Encrypt storage on devices
  - Require a lock screen and password
  - Remote wipe a mobile device that is lost or stolen
  - Block the execution of certain apps
  - Meet compliance standards
  - Prevent data being shared or stored in unauthorized locations
  - Manage devices remotely

- __Use an Enterprise Mobile Management (EMM) system__: MDM policies are specific to mobile operating systems. In order to distribute MDM policies across Android, iOS, and other mobile operating systems, the BYODs can be enrolled through an Enterprise Mobility Management (EMM) system.
- __Require the use of multi-factor authentication (MFA)__: Users can be authenticated by presenting more than one method of identification. Some common identification factors include:
  - Something you know: a password or pin number
  - Something you have: a physical token, like an ATM or bank card, USB device, key fob, or OTP (one-time password)
  - Something you are: biometric data, like a fingerprint, voice signature, facial recognition, or retina scan 
  - Somewhere you are: location-dependent access, like a Global Positioning System (GPS) location
 - Something you do: gestures, like swipe patterns; Turing tests, like CAPTCHA; or normal patterns of behavior, like regular login and logout times
- __Set an acceptable use policy (AUP)__: Organizations could create policies that set a code of conduct for use of the companies’ data, systems, network, and other resources.
- __Use non-disclosure agreements (NDA)__: Organizations can create legally binding contracts with employees to assert the confidentiality and security policies for the companies’ data and intellectual property.
- __Restrict data access__: IT departments should protect company data by limiting access to only those employees who need access to perform their jobs.
- __Educate staff about data security__: Organizations can provide training manuals and seminars to inform employees about network security risks and to instruct on how to secure their BYODs.
- __Back up device data__: IT departments need to create backup policies for all important data. This should include a schedule for frequency of backups, storage space for the back-up copies, how long back-ups should be stored, and disaster recovery plans.
- __Data leakage prevention (DLP)__: IT departments can implement DLP software solutions to help manage and protect confidential information.

Resources for more information

[BYOD](https://www.techtarget.com/whatis/definition/BYOD-bring-your-own-device)
 - Additional information on how BYOD works, why is it important, level of access options, risks, challenges, policy comparisons, best practices, how to implement a BYOD policy.
[BYOD policy: An in-depth guide from an IT leader](https://www.dialpad.com/blog/byod-policy/)
 - Compares BYOD advantages and disadvantages, what should be included in a BYOD policy, tips for reducing security risks, and more.
[What is MDM?](https://www.manageengine.com/mobile-device-management/what-is-mdm.html)
 - Introduces the purpose of MDM software, how it works, advantages of using MDM, use cases, and more.
[Enterprise Mobility Management](https://www.manageengine.com/mobile-device-management/enterprise-mobility-management-emm.html?network=g&device=c&keyword=enterprise%20mobility%20management&campaignid=10047966928&creative=479014654278&matchtype=p&adposition=&placement=&adgroup=108476453023&targetid=kwd-10879221579&gclid=Cj0KCQjwkruVBhCHARIsACVIiOxm1_vkFiOK2IXWj2cw2f_7lJGQdIzjl9sn0nY9nl9i9_TKolc9i_IaAluCEALw_wcB)
 - Outlines the features, services, and benefits of EMM systems. 

# Malware Library
A growing library and of various malware and how they attack/harm endpoints.

### HTML Smuggling Phishing Attack
Sorce: [Bleepingcompter](https://www.bleepingcomputer.com/news/security/microsoft-warns-of-surge-in-html-smuggling-phishing-attacks/)

![html_phish](https://i.imgur.com/xUtphRT.png)

__What is an HTML smuggling phishing attack?__

- A phishing email that contains a seemingly harmless HTML email attachment.

__How does it get past security filters?_

- Attackers behind these phishing campaigns have stolen more than 400,000 legitimate Office 365 and Outlook Web Access credentials which are used to bypass secure email gateways (SEGs).

- "Phishers continue to find success in using compromised accounts on email marketing services to send malicious emails from legitimate IP ranges and domains," Microsoft's security experts said.

- "They take advantage of configuration settings that ensure delivery of emails even when the email solution detects phishing."

- In order to better avoid being caught by endpoint security solutions, some archives are given password-protection encryption to make them harder to detect.

__How does HTML turn into ransomware?__

- A phishing HTML attachment could include a harmless link to a known website, thus not being seen as malicious. However, when a user clicks on the link the HTML file decodes a Base64 code of a JavaScript file which then auto-downloads malware files from a command and control server (C2) to install on the victim's device.

- HTML smuggling has been used to install malicious software like AsyncRAT, NJRAT, and TrickBot. These trojans can be used to gain access to networks and deploy ransomware.


__How can I defend myself and my organization?__

- Microsoft advises administrators to use behavioral rules to identify any signs of HTML smuggling, such as:
   - An attached ZIP file contains JavaScript
   - An attachment is password-protected
   - An HTML file contains a suspicious script code
   - An HTML file decodes a Base64 code or obfuscates a JavaScript

- For endpoints, admins should block or audit activity associated with HTML smuggling, including:
  - Block JavaScript or VBScript from launching downloaded executable content
  - Block execution of potentially obfuscated scripts
  - Block executable files from running unless they meet a prevalence, age, or trusted list criterion

- IT admins should implement blocking or auditing protocols for endpoints when it comes to HTML smuggling activities, such as:
  - Search for __Folder Options__ in the Windows 10 Start Menu and when 'File Explorer Options' appears, click on it.
  - When the File Explorer Options screen appears, click on the __View__ tab and scroll through the Advanced settings until you see an option labeled __"Hide extensions for known file types"__.
  - Uncheck the option: __Hide extensions for known file types__.
  - Click __Apply__ and __OK__ to close the window.
  - Now, you should be able to see (malicious) file extensions.

![file_ext](https://i.imgur.com/ibYwonK.png)

- JavaScript attachments with .js extension should never be opened or downloaded. If it's accidentally downloaded, it should be immediately deleted.

- Furthermore, if an attachment or email link downloads an attachment ending with a _.js extension (JavaScript), it should never be opened_ and automatically be deleted.

  - In addition, endusers could prevent automatic JavaScript code execution by configuring `.js` and `.jse` files top open with a text editor like Notepad.

- Ultimately, the best way to secure an organization from malicious attacks is to educate the users on the dangers associated with opening files coming from emails or attachments. Awareness and caution should be exercised when dealing with these types of files.


