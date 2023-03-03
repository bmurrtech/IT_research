

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
- **Exploit**: Software that is used to take advantage of a security bug or vulnerability. Attackers will write up exploits for vulnerabilities they find in software to cause harm to the system.
-  **Threat**: The possibility of danger that could exploit a vulnerability. Threats are just possible attackers sort of like burglars. Not all burglars will attempt to break into your home to steal your most prized possessions, but they could and so they're considered threats.
-  **Hacker**: in the security world, a hacker is someone who attempts to break into or exploit a system. Most of us associate hackers with malicious figures, but there are actually two common types of hackers:
    - *Black Hat Hackers*: who try to get into systems to do something malicious.  
    - *White Hat Hackers* who attempt to find weaknesses in the system, but also alert the owners of those systems so that they can fix it before someone else does something malicious.
- **Attack**: An actual attempt at causing harm to a system.
- **Malware**: Malware is a type of malicious software that can be used to obtain your sensitive information or delete or modify files.
    -  **Virus** the virus attaches itself to some executable code like a program. When the program is running, it touches many files, each of which is now susceptible to being infected with the virus. The virus replicates itself on these files, does the malicious work it's intended to do and repeats this over and over until it spreads as far as it can.
    - **Worms** are similar to viruses, except that instead of having to attach themselves onto something to spread, worms can live on their own and spread through channels like the network. One case of a famous computer worm was the ILoveYou or Love Bug, which spread to millions of Windows machines. This is just one of the many reasons why _you should never open email attachments that you do not recognize_. 
    - **Adware** is one of the most visible forms of malware that you'll encounter. Most of us see it every day. Adware is just software that displays advertisements and collects data. Sometimes we legitimately download adware. That happens when you agree to the terms of service that allows you to use free software in exchange for showing you advertisements. 
    - **Trojan Horse** A Trojan is malware that disguises itself as one thing, but does something else. 
    - __Spyware__ is a type of malware that's meant to spy on you, which could mean monitoring your computer screens, key presses, webcams, and then reporting or streaming all of this information to another party. 
   - A __key logger__ is a common type of spyware that's used to record every keystroke you make. It can capture all of the messages you type, your confidential information, your passwords, and even more.
   - __Ransomware__ is a type of attack that holds your data or system hostage until you pay some ransom. Our case of ransomware was the WannaCry ransomware attack in May, of 2017. The malware took advantage of _a vulnerability in older Windows systems_, infecting hundreds of thousands of machines across the world. Most notably, the attacks shutdown the systems for the National Health Services in England, causing a health-related crisis.

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
    - Similar to a ping flood is a __SNC flood__ or __half-open attacks__ Remember that to make a TCP connection, a client sends a SYN packet to a server, it wants to connect to next, the server sends back a SYN-ACK message. Then the client sends an ACK message. In a SYN flood, the server is being bombarded with these sim packets. The server is sending back SYN-ACK packets, but the attacker is not sending ACK messages. _This means that the connection stays open and is taking up the server's resources. Other users will be unable to connect to the server_, which is a big problem, since the TCP connection is half open _we also refer to SYN floods as_ __half-open attacks__. [syn_flood](https://photos.app.goo.gl/EQpG1ofCdA5d2ikG7)
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

#### Targeted and in-person deceptive attacks 

__Shoulder surfing__: This malicious attack might have a specific victim or organization as their target. Shoulder surfing happens _when a person looks over a victim’s shoulder to watch them enter login credentials, credit card numbers, or other sensitive information_. For example, a temporary contractor for an organization may look over the shoulder of an employee to watch the employee enter their login info. The temporary employee’s goal might be to steal credentials in order to illegally obtain confidential company data or plant ransomware. 

__Tailgating__: This in-person attack is a form of social engineering in which an unauthorized party gains physical access to a restricted area by simply following a person or group of persons who have authorized access. For example, a criminal wanting to gain physical access to an organization’s computer network might dress in business clothing and follow a group of coworkers coming back from lunch. One member of the group may use their key card to open the door, then hold the door open for the rest of the group, as well as the criminal who is dressed and behaving as though they belong in the building. The criminal may even have a fake ID card to show anyone who questions them.   

__Impersonation__: This attack might happen over email, text messaging, or a phone call. The attacker impersonates someone who should have access to an organization’s computer network. For example, the attacker might call the IT Support team to request help with a password reset. Alternatively, the attacker might pretend to be a member of an organization’s IT Support team. They may call an employee to ask them to change some settings on their computer to fix a fake problem. These changes are intended to open a door for the cybercriminal to gain access to the organization’s network. 

__Dumpster Diving__: This in-person attack involves the attacker literally digging through the trash of an individual or organization to hunt for confidential information, like financial or customer information. Shredding all confidential documents is an easy way to prevent this type of attack. 

__Evil twin__: This type of attack involves the cybercriminal installing Wi-Fi routers that appear to belong to an organization's network. These Wi-Fi access points may not require a password and might appear to offer a stronger signal than the real Wi-Fi router. When victims connect to the fake Wi-Fi access point, the cybercriminal gains access to the victim’s wireless transmissions, which can include login credentials and other sensitive information.

## Terms Glossary

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

### Types of cryptanalysis attack
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

# Public Key (or Asymmetric Cryptography)

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
- __SHA1__ is part of the Secure Hash Algorithm suite of functions designed by the NSA and published in 1995. SHA1 is another widely used cryptographic hashing functions _used in popular protocols like TLS/SSL, PGP/SSH, and IPSec_. SHA1 is also used in version control systems like Git, which uses hashes to identify revisions and ensure data integrity by detecting corruption or tampering. However, significant computational is required to cause a hash collision.
    - For example: A full collisions using these methods requires significant computing power. One such attack was _estimated to require $2.77 million in Cloud computing CPU resources_.
    - However, due to increasing computational power of modern CPUs and GPUs,(especially in the space of GPU accelerated computations and Cloud resources), a full collision with _this attack method was estimated to be feasible using CPU and GPU Cloud computing for approximately $75K to $120,000_, much cheaper than previous attacks.
