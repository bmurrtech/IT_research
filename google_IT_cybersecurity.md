

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
