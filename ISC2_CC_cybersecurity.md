### **Any and all copyright materials used are for educational, non-commercial, illustrative (research, criticism, & comment), unpublished purposes only. Facts themselves are not copyrightable.**

### **Any other works of mine are under the Attribution NonCommercial ShareAlike 4.0 International license.**

Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

# Table of Contents
- [Chapter 1: Security Principles](#chapter-1)
- [Chapter 2: Incident Response, Business Continuity and Disaster Recovery Concepts](#chapter-2)
- [Chapter 3: Access Control Concepts](#chapter-3)
- [Chapter 4: Network Security](#chapter-4)
- [Chapter 5: Security Operations](#chapter-5)

# Chapter 1
- [Module 1: Understand the Security Concepts of Information Assurance (D1.1)](#understand-security)
- [Module 2: Understand the Risk Management Process (D1.2)](#understand-risk-management)
- [Module 3: Understand Security Controls (D1.3)](#security-controls)
- [Module 4: Understand Governance Elements (D1.5)](#understand-governance)
- [Module 5: Understand ISC2 Code of Ethics (D1.4)](#isc2-code-of-ethics)
- [Chapter 1 Glossary](#chapter-1-glossary)

# Understand Security
(D1.1)

### Confidentiality 

is a difficult balance to achieve when many system users are guests or customers, and it is not known if they are accessing the system from a compromised machine or vulnerable mobile application. So, the security professional’s obligation is to regulate access—protect the data that needs protection, yet permit access to authorized individuals.

Personally Identifiable Information (PII) is a term related to the area of confidentiality. It pertains to any data about an individual that could be used to identify them. Other terms related to confidentiality are protected health information (PHI) , which is information regarding one’s health status, and classified or sensitive information, which includes trade secrets, research, business plans and intellectual property.

Another useful definition is sensitivity, which is a measure of the importance assigned to information by its owner, or the purpose of denoting its need for protection. Sensitive information is information that if improperly disclosed (confidentiality) or modified (integrity) would harm an organization or individual. In many cases, sensitivity is related to the harm to external stakeholders; that is, people or organizations that may not be a part of the organization that processes or uses the information

### Integrity 

measures the degree to which something is whole and complete, internally consistent and correct. The concept of integrity applies to:

- information or data
- systems and processes for business operations
- organizations
- people and their actions
__Data integrity is the assurance that data has not been altered in an unauthorized manner__. This requires the protection of the data in systems and during processing to ensure that it is free from improper modification, errors or loss of information and is recorded, used and maintained in a way that ensures its completeness. Data integrity covers data in storage, during processing and while in transit.

Information must be accurate, internally consistent and useful for a stated purpose. The internal consistency of information ensures that information is correct on all related systems so that it is displayed and stored in the same way on all systems. Consistency, as part of data integrity, requires that all instances of the data be identical in form, content and meaning.

System integrity refers to the maintenance of a known good configuration and expected operational function as the system processes the information. Ensuring integrity begins with an awareness of state, which is the current condition of the system. Specifically, this awareness concerns the ability to document and understand the state of data or a system at a certain point, creating a baseline. For example, a baseline can refer to the current state of the information—whether it is protected. Then, to preserve that state, the information must always continue to be protected through a transaction.

Going forward from that baseline, the integrity of the data or the system can always be ascertained by comparing the baseline with the current state. If the two match, then the integrity of the data or the system is intact; if the two do not match, then the integrity of the data or the system has been compromised. Integrity is a primary factor in the reliability of information and systems.

The need to safeguard information and system integrity may be dictated by laws and regulations. Often, it is dictated by the needs of the organization to access and use reliable, accurate information.

### Availability 
can be defined as (1) timely and reliable access to information and the ability to use it, and (2) for authorized users, timely and reliable access to data and information services.

The core concept of __availability is ensuring timely and reliable access to data to authorized users__ and in the form and format required. This does not mean that data or systems are available 100% of the time. Instead, the systems and data meet the requirements of the business for timely and reliable access.

Some systems and data are far more critical than others, so the security professional must ensure that the appropriate levels of availability are provided. This requires consultation with the involved business to ensure that critical systems are identified and available. Availability is often associated with the term criticality, because it represents the importance an organization gives to data or an information system in performing its operations or achieving its mission.

### Authentication

When users have stated their identity, it is necessary to validate that they are the rightful owners of that identity. This process of verifying or proving the user’s identification is known as authentication. Simply put, authentication is a process to prove the identity of the requestor.

There are three common methods of authentication:

- Something you know: Passwords or passphrases
- Something you have: Tokens, memory cards, smart cards
- Something you are: Biometrics, measurable characteristics

#### Methods of Authentication
There are two types of authentication. Using only one of the methods of authentication stated previously is known as single-factor authentication (SFA), but __MFA is an access control process that compares one or more factors of identification to validate that the idenity claimed by the user or entity is known to the system.__ Granting users access only after successfully demonstrating or displaying two or more of these methods is known as multi-factor authentication (MFA) . 

Common best practice is to implement at least two of the three common techniques for authentication: 
- Knowledge-based 
- Token-based 
- Characteristic-based 

Knowledge-based authentication uses a passphrase or secret code to differentiate between an authorized and unauthorized user. If you have selected a personal identification number (PIN), created a password or some other secret value that only you know, then you have experienced knowledge-based authentication. The problem with using this type of authentication alone is that it is often vulnerable to a variety of attacks. For example, the help desk might receive a call to reset a user’s password. The challenge is ensuring that the password is reset only for the correct user and not someone else pretending to be that user. For better security, a second or third form of authentication that is based on a token or characteristic would be required prior to resetting the password. The combined use of a user ID and a password consists of two things that are known, and because it does not meet the requirement of using two or more of the authentication methods stated, it is not considered MFA. 

#### Non-repudiation
__Non-repudiation is the inability to deny taking an action, such as sending an email__. It's a legal term and is defined as the protection against an individual falsely denying having performed a particular action. It provides the capability to determine whether a given individual took a particular action, such as created information, approved information or sent or received a message.

In today’s world of e-commerce and electronic transactions, there are opportunities for the impersonation of others or denial of an action, such as making a purchase online and later denying it. It is important that all participants trust online transactions. Non-repudiation methodologies ensure that people are held responsible for transactions they conducted. 

#### Privacy
__Privacy is the right of an individual to control the distribution of information about themselves.__ While security and privacy both focus on the protection of personal and sensitive data, there is a difference between them. With the increasing rate at which data is collected and digitally stored across all industries, the push for privacy legislation and compliance with existing policies steadily grows. In today’s global economy, privacy legislation and regulations on privacy and data protection can impact corporations and industries regardless of physical location. Global privacy is an especially crucial issue when considering requirements regarding the collection and security of personal information. There are several laws that define privacy and data protection, which periodically change. Ensuring that protective security measures are in place is not enough to meet privacy regulations or to protect a company from incurring penalties or fines from mishandling, misuse, or improper protection of personal or private information. An example of a law with multinational implications is the European Union’s General Data Protection Regulation (GDPR) which applies to all organizations, foreign or domestic, doing business in the EU or any persons in the EU. Companies operating or doing business within the United States may also fall under several state legislations that regulate the collection and use of consumer data and privacy. Likewise, member nations of the EU enact laws to put GDPR into practice and sometimes add more stringent requirements. These laws, including national- and state-level laws, dictate that any entity anywhere in the world handling the private data of people in a particular legal jurisdiction must abide by its privacy requirements. As a member of an organization's data protection team, you will not be required to interpret these laws, but you will need an understanding of how they apply to your organization.

# Understand Risk Management
(D1.2.1, D1.2.2)

Risks and security-related issues represent an ongoing concern of businesses as well as the field of cybersecurity, but far too often organizations fail to proactively manage risk. Assessing and analyzing risk should be a continuous and comprehensive exercise in any organization. As a member of an organization’s security team, you will work through risk assessment, analysis, mitigation, remediation and communication.

There are many frameworks and models used to facilitate the risk management process, and each organization makes its own determination of what constitutes risk and the level of risk it is willing to accept. However, there are commonalities among the terms, concepts and skills needed to measure and manage risk. This module gets you started by presenting foundational terminology and introducing you to the risk management process.

First, a definition of  risk  is  a measure of the extent to which an entity is threatened by a potential circumstance or event. It is often expressed as a combination of:

- the adverse impacts that would arise if the circumstance or event occurs,  and 
- the likelihood of occurrence. 

Information security risk reflects the potential adverse impacts that result from the possibility of unauthorized access, use, disclosure, disruption, modification or destruction of information and/or information systems. This definition represents that risk is associated with threats, impact and likelihood, and it also indicates that IT risk is a subset of business risk. 

### Risk Management Terminology
Security professionals use their knowledge and skills to examine operational risk management, determine how to use risk data effectively, work cross-functionally and report actionable information and findings to the stakeholders concerned. Terms such as threats, vulnerabilities and assets are familiar to most cybersecurity professionals.

- An __asset is something of value (hardware, intellectual property, etc). in need of protection.__
- A __vulnerability is an inherent weakness or flaw in a system or component__, a gap or weakness in those protection efforts.
- A __threat is something or someone that aims to exploit a vulnerability to exploit a target.__

Risk is the intersection of these terms. Let's look at them more closely.

### Threats
A threat is a person or thing that takes action to exploit (or make use of) a target organization’s system vulnerabilities, as part of achieving or furthering its goal or objectives. To better understand threats, consider the following scenario:

In the context of cybersecurity, typical threat actors include the following:

- Insiders (either deliberately, by simple human error, or by gross incompetence).
- Outside individuals or informal groups (either planned or opportunistic, discovering vulnerability).
- Formal entities that are nonpolitical (such as business competitors and cybercriminals).
- Formal entities that are political (such as terrorists, nation-states, and hacktivists).
- Intelligence or information gatherers (could be any of the above).
- Technology (such as free-running bots and artificial intelligence , which could be part of any of the above).

*Threat Vector: The means by which a threat actor carries out their objectives.

### Vulnerabilities
__A vulnerability is an inherent weakness or flaw in a system or component__, which, if triggered or acted upon, could cause a risk event to occur. Consider the pickpocket scenario from below.

An organization’s security team strives to decrease its vulnerability. To do so, they view their organization with the eyes of the threat actor, asking themselves, “Why would we be an attractive target?” The answers might provide steps to take that will discourage threat actors, cause them to look elsewhere or simply make it more difficult to launch an attack successfully. For example, to protect yourself from the pickpocket, you could carry your wallet in an inside pocket instead of the back pant pocket or behave alertly instead of ignoring your surroundings. Managing vulnerabilities starts with one simple step: Learn what they are.

### Likelihood
When determining an organization’s vulnerabilities, the security team will consider the probability, or likelihood , of a potential vulnerability being exploited within the construct of the organization’s threat environment. __Likelihood of occurrence is a weighted factor based on a subjective analysis of the probability that a given threat or set of threats is capable of exploiting a given vulnerability__ or set of vulnerabilities.

Finally, the security team will consider the likely results if a threat is realized and an event occurs. Impact is the magnitude of harm that can be expected to result from the consequences of unauthorized disclosure of information, unauthorized modification of information, unauthorized destruction of information, or loss of information or information system availability.

 Think about the impact and the chain of reaction that can result when an event occurs by revisiting the pickpocket scenario:


### Risk Identification
How do you identify risks? Do you walk down the street watching out for traffic and looking for puddles on the ground? Maybe you’ve noticed loose wires at your desk or water on the office floor? If you’re already on the lookout for risks, you’ll fit with other security professionals who know it’s necessary to dig deeper to find possible problems.  

In the world of cyber, identifying risks is not a one-and-done activity. It’s a recurring process of identifying different possible risks, characterizing them and then estimating their potential for disrupting the organization.  

It involves looking at your unique company and analyzing its unique situation. Security professionals know their organization’s strategic, tactical and operational plans.

Takeaways to remember about risk identification: 

- Identify risk to communicate it clearly. 
- Employees at all levels of the organization are responsible for identifying risk.
- Identify risk to protect against it. 

As a security professional, you are likely to assist in risk assessment at a system level, focusing on process, control, monitoring or incident response and recovery activities. If you’re working with a smaller organization, or one that lacks any kind of risk management and mitigation plan and program, you might have the opportunity to help fill that planning void.

### Risk Assessment
__Risk assessment is defined as the process of identifying, estimating and prioritizing risks to an organization’s operations (including its mission, functions, image and reputation), assets, individuals, other organizations and even the nation.__ Risk assessment should result in aligning (or associating) each identified risk resulting from the operation of an information system with the goals, objectives, assets or processes that the organization uses, which in turn aligns with or directly supports achieving the organization’s goals and objectives. 

A common risk assessment activity identifies the risk of fire to a building. While there are many ways to mitigate that risk, the primary goal of a risk assessment is to estimate and prioritize. For example, fire alarms are the lowest cost and can alert personnel to evacuate and reduce the risk of personal injury, but they won’t keep a fire from spreading or causing more damage. Sprinkler systems won’t prevent a fire but can minimize the amount of damage done. However, while sprinklers in a data center limit the fire’s spread, it is likely they will destroy all the systems and data on them. A gas-based system may be the best solution to protect the systems, but it might be cost-prohibitive. A risk assessment can prioritize these items for management to determine the method of mitigation that best suits the assets being protected. 

The result of the risk assessment process is often documented as a report or presentation given to management for their use in prioritizing the identified risk(s). This report is provided to management for review and approval. In some cases, management may indicate a need for a more in-depth or detailed risk assessment performed by internal or external resources.

### Risk Treatment 
Risk treatment relates to making decisions about the best actions to take regarding the identified and prioritized risk. The decisions made are dependent on the attitude of management toward risk and the availability — and cost — of risk mitigation. The options commonly used to respond to risk are:

![risk_treatment](https://i.imgur.com/qabuAXx.png)

- __Risk AVOIDANCE is the decision to cease the risky activity to remove the likelihood that an event will occure__ to attempt to eliminate the risk entirely. This could include ceasing operation for some or all of the activities of the organization that are exposed to a particular risk. Organization leadership may choose risk avoidance when the potential impact of a given risk is too high or if the likelihood of the risk being realized is simply too great.
- __Risk ACCEPTANCE is taking no action, ignoring the risks, and continuing risky activity.__ Management may opt for conducting the business function that is associated with the risk without any further action on the part of the organization, either because the impact or likelihood of occurrence is negligible, or because the benefit is more than enough to offset that risk.
- __Risk MITIGATION is taking actions to prevent or reduce the impact of an event.__ Mitigation can involve remediation measures, or controls, such as security controls, establishing policies, procedures, and standards to minimize adverse risk. Risk cannot always be mitigated, but mitigations such as safety measures should always be in place.
- __Risk TRANSFERENCE is passing the risk to third party__ who will accept the financial impact of the harm resulting from a risk being realized in exchange for payment.__ Typically, this is an insurance policy.

![risk_terms](https://i.imgur.com/Q2NQQpB.png)

When a company chooses to ignore a risk and proceed with a risky activity, which treatment is being applied by default? (D1, L1.2.2)
- [ ] Mitigation
- [ ] Avoidance
- [ ] Acceptance
- [ ] Transference

# Security Controls
__Security Controls are the physical, technical and administrative mechanisms that act as safeguards or countermeasures prescribed for an information system to protect the confidentiality, integrity and availability of the system__ and its information. The implementation of controls should reduce risk, hopefully to an acceptable level.

- __Physical Controls are any physical deterants or tangible secuirty measures that prevent unwanted access.__
  - Badge reader
  - Stop Sign in Parking
  - Door Lock
  - Gates
  - Fire Extinguisher

- __Technical Controls (also called logical controls) can be configuration settings or parameters managed through a software, or firmware, or hardware settings__ done with switches, jumper plugs or other means.
  - ACL: Access Control List
  - Passwords
  - Encryption
- __Administrative controls (also known as managerial controls) are POLICIES and PROCEDURES aimed at the people within the organization.__ Even the simplest security awareness policies can be an effective control, if you can help the organization fully implement them through systematic training and practice.
  - Acceptable Use Policy
  - Emergency Operations Procedures
  - Secuirty Awareness Training
  - Password Policy
 
# Understand Governance
(Domain D1.5.1, D1.5.2, D1.5.3, D1.5.4)

- __Procedures are the detailed step-by-step instructions to complete a task__ that support departmental or organizational policies.
- __Policies are the hightles-level goverance documents and provide guidance in all activities__ to ensure that the organization supports industry standards and regulations.
- __Standards to provide a framework to guide__ organizational towards policy compliance.
- __Regulations/laws are commonly issued in the form of laws by governments__ and typically carry financial penalties for noncompliance.

# ISC2 Code of Ethics
(Domain D1.4.1)

### IC2 Code of Ethics Preamble
The Preamble states the purpose and intent of the ISC2 Code of Ethics. 
- The safety and welfare of society and the common good, duty to our principals, and to each other, requires that we adhere, and be seen to adhere, to the highest ethical standards of behavior.
- Therefore, strict adherence to this Code is a condition of certification. 

### IC2 Code of Ethics Canons
The Canons represent the important beliefs held in common by the members of ISC2. Cybersecurity professionals who are members of ISC2 have a duty to the following four entities in the Canons.  

- Protect society, the common good, necessary public trust and confidence, and the infrastructure.
- Act honorably, honestly, justly, responsibly and legally.
- Provide diligent and competent service to principals.
- Advance and protect the profession.

# Chapter 1 Summary
- [Chapter 1 Quizlet Flashcards](https://quizlet.com/669177667/chapter-1-security-principles-flash-cards/)
- [Chapter 1 Overview](https://learn.isc2.org/content/enforced/9541-CC-SPT-GLOBAL-1ED-1M/build/chapter_01/assets/EDU-CC-70175-ch01_Takeaway.pdf?_&d2lSessionVal=6eLDFtTzOfyS237SfA6UBMP3K&ou=9541)

### Chapter 1 Glossary

- Adequate Security - Security commensurate with the risk and the magnitude of harm resulting from the loss, misuse or unauthorized access to or modification of information. Source: OMB Circular A-130
- Administrative Controls - Controls implemented through policy and procedures. Examples include access control processes and requiring multiple personnel to conduct a specific operation. Administrative controls in modern environments are often enforced in conjunction wit physical and/or technical controls, such as an access-granting policy for new users that requires login and approval by the hiring manager.
- Artificial Intelligence - The ability of computers and robots to simulate human intelligence and behavior.
- Asset - Anything of value that is owned by an organization. Assets include both tangible items such as information systems and physical property and intangible assets such as intellectual property.
- Authentication - Access control process validating that the identity being claimed by a user or entity is known to the system, by comparing one (single factor or SFA) or more (multi-factor authentication or MFA) factors of identification.
- Authorization - The right or a permission that is granted to a system entity to access a system resource. NIST 800-82 Rev.2
Availability - Ensuring timely and reliable access to and use of information by authorized users.
Baseline - A documented, lowest level of security configuration allowed by a standard or organization.
- Bot - Malicious code that acts like a remotely controlled “robot” for an attacker, with other Trojan and worm capabilities.
- Classified or Sensitive Information - Information that has been determined to require protection against unauthorized disclosure and is marked to indicate its classified status and classification level when in documentary form.
Confidentiality - The characteristic of data or information when it is not made available or disclosed to unauthorized persons or processes. NIST 800-66
- Criticality  - A measure of the degree to which an organization depends on the information or information system for the success of a mission or of a business function. NIST SP 800-60 Vol. 1, Rev. 1
- Data Integrity - The property that data has not been altered in an unauthorized manner. Data integrity covers data in storage, during processing and while in transit. Source: NIST SP 800-27 Rev A
- Encryption - The process and act of converting the message from its plaintext to ciphertext. Sometimes it is also referred to as enciphering. The two terms are sometimes used interchangeably in literature and have similar meanings.
- General Data Protection Regulation (GDPR) - In 2016, the European Union passed comprehensive legislation that addresses personal privacy, deeming it an individual human right.
- Governance -The process of how an organization is managed; usually includes all aspects of how decisions are made for that organization, such as policies, roles, and procedures the organization uses to make those decisions.
- Health Insurance Portability and Accountability Act (HIPAA) - This U.S. federal law is the most important healthcare information regulation in the United States. It directs the adoption of national standards for electronic healthcare transactions while protecting the privacy of individual's health information. Other provisions address fraud reduction, protections for individuals with health insurance and a wide range of other healthcare-related activities. Est. 1996.
- Impact - The magnitude of harm that could be caused by a threat’s exercise of a vulnerability.
Information Security Risk - The potential adverse impacts to an organization’s operations (including its mission, functions and image and reputation), assets, individuals, other organizations, and even the nation, which results from the possibility of unauthorized access, use, disclosure, disruption, modification or destruction of information and/or information systems.
- Institute of Electrical and Electronics Engineers - IEEE is a professional organization that sets standards for telecommunications, computer engineering and similar disciplines.
- Integrity - The property of information whereby it is recorded, used and maintained in a way that ensures its completeness, accuracy, internal consistency and usefulness for a stated purpose.
- International Organization of Standards (ISO) - The ISO develops voluntary international standards in collaboration with its partners in international standardization, the International Electro-technical Commission (IEC) and the International Telecommunication Union (ITU), particularly in the field of information and communication technologies.
- Internet Engineering Task Force (IETF) - The internet standards organization, made up of network designers, operators, vendors and researchers, that defines protocol standards (e.g., IP, TCP, DNS) through a process of collaboration and consensus. Source: NIST SP 1800-16B
- Likelihood - The probability that a potential vulnerability may be exercised within the construct of the associated threat environment.
Likelihood of Occurrence - A weighted factor based on a subjective analysis of the probability that a given threat is capable of exploiting a given vulnerability or set of vulnerabilities.
- Multi-Factor Authentication - Using two or more distinct instances of the three factors of authentication (something you know, something you have, something you are) for identity verification.
- Non-repudiation - The inability to deny taking an action such as creating information, approving information and sending or receiving a message.
- Personally Identifiable Information (PII) - The National Institute of Standards and Technology, known as NIST, in its Special Publication 800-122 defines PII as “any information about an individual maintained by an agency, including (1) any information that can be used to distinguish or trace an individual’s identity, such as name, Social Security number, date and place of birth, mother’s maiden name, or biometric records; and (2) any other information that is linked or linkable to an individual, such as medical, educational, financial and employment information.”
- Physical Controls - Controls implemented through a tangible mechanism. Examples include walls, fences, guards, locks, etc. In modern organizations, many physical control systems are linked to technical/logical systems, such as badge readers connected to door locks.
- Privacy - The right of an individual to control the distribution of information about themselves.
- Probability - The chances, or likelihood, that a given threat is capable of exploiting a given vulnerability or a set of vulnerabilities. Source: NIST SP 800-30 Rev. 1
Protected Health Information (PHI) - Information regarding health status, the provision of healthcare or payment for healthcare as defined in HIPAA (Health Insurance Portability and Accountability Act).
- Qualitative Risk Analysis - A method for risk analysis that is based on the assignment of a descriptor such as low, medium or high. Source: NISTIR 8286
- Quantitative Risk Analysis - A method for risk analysis where numerical values are assigned to both impact and likelihood based on statistical probabilities and monetarized valuation of loss or gain. Source: NISTIR 8286
- Risk - A measure of the extent to which an entity is threatened by a potential circumstance or event.
- Risk Acceptance - Determining that the potential benefits of a business function outweigh the possible risk impact/likelihood and performing that business function with no other action.
- Risk Assessment - The process of identifying and analyzing risks to organizational operations (including mission, functions, image, or reputation), organizational assets, individuals and other organizations. The analysis performed as part of risk management which incorporates threat and vulnerability analyses and considers mitigations provided by security controls planned or in place.
- Risk Avoidance - Determining that the impact and/or likelihood of a specific risk is too great to be offset by the potential benefits and not performing a certain business function because of that determination.
- Risk Management - The process of identifying, evaluating and controlling threats, including all the phases of risk context (or frame), risk assessment, risk treatment and risk monitoring.
- Risk Management Framework - A structured approach used to oversee and manage risk for an enterprise. Source: CNSSI 4009
- Risk Mitigation - Putting security controls in place to reduce the possible impact and/or likelihood of a specific risk.
- Risk Tolerance - The level of risk an entity is willing to assume in order to achieve a potential desired result. Source: NIST SP 800-32. Risk threshold, risk appetite and acceptable risk are also terms used synonymously with risk tolerance.
- Risk Transference - Paying an external party to accept the financial impact of a given risk.
- Risk Treatment - The determination of the best way to address an identified risk.

# Chapter 2
- [Module 1: Understand incident response D2.3](#understanding-incident-response)
- [Module 2: Understand business continuity D2.1](#understand-business-continuity)
- [Module 3: Understand disaster recovery D2.2](#understand-disaster-recovery)
- [Chapter 2 Glossary](#chapter-2-glossary)

# Understanding Incident Response

### Incident Terminology 
- Breach: The loss of control, compromise, unauthorized disclosure, unauthorized acquisition, or any similar occurrence where: a person other than an authorized user accesses or potentially accesses personally identifiable information; or an authorized user accesses personally identifiable information for other than an authorized purpose. NIST SP 800-53 Rev. 5
- Event: Any observable occurrence in a network or system. NIST SP 800-61 Rev 2
- Exploit: A particular attack. It is named this way because these attacks exploit system vulnerabilities.
- Incident: An event that actually or potentially jeopardizes the confidentiality, integrity or availability of an information system or the information the system processes, stores or transmits.
- Intrusion: A security event, or combination of events, that constitutes a deliberate security incident in which an intruder gains, or attempts to gain, access to a system or system resource without authorization. IETF RFC 4949 Ver 2
- Threat: Any circumstance or event with the potential to adversely impact organizational operations (including mission, functions, image or reputation), organizational assets, individuals, other organizations or the nation through an information system via unauthorized access, destruction, disclosure, modification of information and/or denial of service. NIST SP 800-30 Rev 1
- Vulnerability: Weakness in an information system, system security procedures, internal controls or implementation that could be exploited by a threat source. NIST SP 800-30 Rev 1
- Zero Day: A previously unknown system vulnerability with the potential of exploitation without risk of detection or prevention because it does not, in general, fit recognized patterns, signatures or methods.

![incident_response](https://i.imgur.com/OyHf7Pb.png)

- Preparation: Develop a policy approved by management
  - Identify critical data and systems, single points of failure
  - Train staff on incident response
  - Implement an incident response team.(covered in subsequent topic)
  - Practice Incident Identification (First Response)
  - Identify Roles and Responsibilities
  - Plan the coordination of communication between stakeholders
  - Consider the possibility that a primary method of communication may not be available
- Detection and Analysis
  - Monitor all possible attack vectors
  - Analyze incident using known data and threat intelligence
  - Prioritize incident response
  - Standardize incident documentation
- Containment
  - Gather evidence
  - Choose an appropriate containment strategy
  - Identify the attacker
  - Isolate the attack
- Post-Incident Activit
- Identify evidence that may need to be retained
  - Document lessons learned

# Understand Business Continuity

- The purpose of implementing a business continuity plan is to ensure the continuity of business operations, particularly during times of significant disruption. In light of an unforeseen event that has caused disturbances in the environment, it is crucial to understand how to effectively sustain and maintain the ongoing functioning of your business.
- Business continuity planning (BCP) refers to the proactive implementation of protocols and processes aimed at effectively restoring business operations following a disaster or any other major disruption to the organization.
- Here are some common components of a comprehensive business continuity plan:
  - List of the BCP team members, including multiple contact methods and backup members
  - Immediate response procedures and checklists (security and safety procedures, fire suppression procedures, notification of appropriate emergency-response agencies, etc.)
  - Notification systems and call trees for alerting personnel that the BCP is being enacted
  - Guidance for management, including designation of authority for specific managers
  - How/when to enact the plan
  - Contact numbers for critical members of the supply chain (vendors, customers, possible external emergency providers, third-party partners)
 
- What does business continuity look like in action?

_Imagine that the billing department of a company suffers a complete loss in a fire. The fire occurred overnight, so no personnel were in the building at the time. A Business Impact Analysis (BIA) was performed four months ago and identified the functions of the billing department as very important to the company, but not immediately affecting other areas of work. Through a previously signed agreement, the company has an alternative area in which the billing department can work, and it can be available in less than one week. Until that area can be fully ready, customer billing inquiries will be answered by customer service staff. The billing department personnel will remain in the alternate working area until a new permanent area is available._

# Understand Disaster Recovery
- The Goal of Disaster Recovery
  - During the examination of the Business Continuity module, we thoroughly examined the fundamental components of business continuity planning. Following this, disaster recovery planning takes over and completes the necessary steps to mitigate potential risks.
  - In the unfortunate event of a disaster or business disruption, the Disaster Recovery Plan (DRP) plays a crucial role in directing emergency response personnel. Its ultimate objective is to ensure the complete restoration of normal business operations to their most recent reliable state.
 
_At a hospital in Los Angeles, it took 260 days (about 8 and a half months) to discover that there was a compromise. In this case, the hospital could not return to doing business by using the last backup because it was riddled with a time-based malware that would corrupt all the data on the system as soon as it was restored. The hospital needed to go back nearly a year prior to discovering the incident to restore the entire system, and then restore the remaining data piece-by-piece to avoid reinfection. This scenario highlights the need for multiple levels of backup and retention periods to address the needs of the organization._

- Components of a Disaster Recovery Plan. The following list includes various types of documents worth considering:
  - Executive summary providing a high-level overview of the plan
  - Department-specific plans
  - Technical guides for IT personnel responsible for implementing and maintaining critical backup systems
  - Full copies of the plan for critical disaster recovery team members
  - Checklists for certain individuals:
    - Critical disaster recovery team members will have checklists to help guide their actions amid the chaotic atmosphere of a disaster.
    - IT personnel will have technical guides helping them get the alternate sites up and running.
    - Managers and public relations personnel will have simple-to-follow, high-level documents to help them communicate the issue accurately without requiring input from team members who are busy working on the recovery.
   
# Chapter 2 Summary
- [Chapter 2 Quizlet Flashcards](https://quizlet.com/669183755/chapter-2-incident-response-business-continuity-bc-and-disaster-recovery-dr-concepts-flash-cards/)
- [Chapter 2 Overview](https://learn.isc2.org/content/enforced/9541-CC-SPT-GLOBAL-1ED-1M/build/chapter_02/assets/EDU-CC-70185-ch02_Takeaway.pdf?_&d2lSessionVal=6eLDFtTzOfyS237SfA6UBMP3K&ou=9541)

### Chapter 3 Glossary
- Adverse Events - Events with a negative consequence, such as system crashes, network packet floods, unauthorized use of system privileges, defacement of a web page or execution of malicious code that destroys data.
- Breach - The loss of control, compromise, unauthorized disclosure, unauthorized acquisition or any similar occurrence where: a person other than an authorized user accesses or potentially accesses personally identifiable information; or an authorized user accesses personally identifiable information for other than an authorized purpose. Source: NIST SP 800-53 Rev. 5
- Business Continuity (BC) - Actions, processes and tools for ensuring an organization can continue critical operations during a contingency. 
- Business Continuity Plan (BCP) - The documentation of a predetermined set of instructions or procedures that describe how an organization’s mission/business processes will be sustained during and after a significant disruption.
- Business Impact Analysis (BIA) - An analysis of an information system’s requirements, functions, and interdependencies used to characterize system contingency requirements and priorities in the event of a significant disruption. Reference: https://csrc.nist.gov/glossary/term/business-impact-analysis
- Disaster Recovery (DR) - In information systems terms, the activities necessary to restore IT and communications services to an organization during and after an outage, disruption or disturbance of any kind or scale. 
- Disaster Recovery Plan (DRP) - The processes, policies and procedures related to preparing for recovery or continuation of an organization's critical business functions, technology infrastructure, systems and applications after the organization experiences a disaster. A disaster is when an organization’s critical business function(s) cannot be performed at an acceptable level within a predetermined period following a disruption.
- Event - Any observable occurrence in a network or system. Source: NIST SP 800-61 Rev 2 
- Exploit - A particular attack. It is named this way because these attacks exploit system vulnerabilities.
- Incident - An event that actually or potentially jeopardizes the confidentiality, integrity or availability of an information system or the information the system processes, stores or transmits.
- Incident Handling - The mitigation of violations of security policies and recommended practices. Source: NIST SP 800-61 Rev 2
- Incident Response (IR) - The mitigation of violations of security policies and recommended practices. Source: NIST SP 800-61 Rev 2
- Incident Response Plan (IRP) - The documentation of a predetermined set of instructions or procedures to detect, respond to and limit consequences of a malicious cyberattack against an organization’s information systems(s). Source: NIST SP 800-34 Rev 1
- Intrusion - A security event, or combination of security events, that constitutes a security incident in which an intruder gains, or attempts to gain, access to a system or system resource without authorization. Source: IETF RFC 4949 Ver 2
- Security Operations Center - A centralized organizational function fulfilled by an information security team that monitors, detects and analyzes events on the network or system to prevent and resolve issues before they result in business disruptions.
- Vulnerability - Weakness in an information system, system security procedures, internal controls or implementation that could be exploited or triggered by a threat source. Source: NIST SP 800-128.
- Zero Day - A previously unknown system vulnerability with the potential of exploitation without risk of detection or prevention because it does not, in general, fit recognized patterns, signatures or methods.

# Chapter 3
- [Module 1: Understand Access Control Concepts D3.1, D3.1.3, D3.1.5, D3.2, D3.2.1, D3.2.2, D3.2.5](#understand-access-control-concepts)
- [Module 2: Understand Physical Access Controls D3.1, D3.1.1, D3.1.2](#understand-physical-access-controls)
- [Module 3: Understand Logical Access Controls D3.2, D3.2.3, D3.2.4, D3.2.5](#understand-logical-access-controls)
- [Module 4: Chapter 3 Summary D3.1, D3.1.1, D3.1.2, D3.1.3, D3.2, D3.2.1, D3.2.2, D3.2.3, D3.2.4, D3.2.5](#chapter-2-glossary)
- [Module 4: Chapter 3 Summary](#chapter-2-glossary)

# Understand Access Control Concepts

What is Security Control?
A control is a safeguard or countermeasure designed to preserve Confidentiality, Integrity and Availability of data. This, of course, is the CIA Triad.  

Access control involves limiting what objects can be available to what subjects according to what rules. We will further define objects, subjects and rules later in this chapter. For now, remember these three words, as they are the foundation upon which we will build. 

One brief example of a control is a firewall, which is included in a system or network to prevent something from the outside from coming in and disturbing or compromising the environment. The firewall can also prevent information on the inside from going out into the Web where it could be viewed or accessed by unauthorized individuals. 

### Controls Overview
Access controls are not just about restricting access to information systems and data, but also about allowing access. It is about granting the appropriate level of access to authorized personnel and processes and denying access to unauthorized functions or individuals.

#### A subject:
A **subject** can be defined as **any entity that requests access to our assets**. The entity requesting access may be a user, a client, a process or a program, for example. A subject is the initiator of a request for service; therefore, a subject is referred to as “active.”
- Is a user, a process, a procedure, a client (or a server), a program, a device such as an endpoint, workstation, smartphone or removable storage device with onboard firmware.
- Is active: It initiates a request for access to resources or services.
- Requests a service from an object.
- Should have a level of clearance (permissions) that relates to its ability to successfully access services or resources.

#### An Object
**An object is a device, process, person, user, program, server, client or other entity that responds to a request for service.** By definition, anything that a subject attempts to access is referred to as an object. 
- Is a building, a computer, a file, a database, a printer or scanner, a server, a communications resource, a block of memory, an input/output port, a person, a software task, thread or process.
- Is anything that provides service to a user.
- Is passive.
- Responds to a request.
- May have a classification.

#### A Rule
An access **rule is an instruction developed to allow or deny access to an object by comparing the validated identity of the subject to an access control list**. One example of a rule is a firewall access control list. A rule can:
- Compare multiple attributes to determine appropriate access.
- Allow access to an object.
- Define how much access is allowed.
- Deny access to an object.
- Apply time-based access.

### Defense in Depth
![defense_n_depth](https://i.imgur.com/amjngig.png)
As you can see, we are not just looking at system access. We are looking at all access permissions including building access, access to server rooms, access to networks and applications and utilities. These are all implementations of access control and are part of a **layered defense** strategy, also known as **defense in depth**, developed by an organization. **Defense in depth describes an information security strategy that integrates people, technology and operations capabilities to establish variable barriers across multiple layers and missions of the organization. It applies multiple countermeasures in a layered fashion to fulfill security objectives.** 
- A **technical** example of defense in depth is when a **username and password** are required for logging in to your account, **followed by a code sent to your phone** to verify your identity. Another example of multiple technical layers is when additional **firewalls** are used to separate untrusted networks with differing security requirements, such as the internet from trusted networks that house servers with sensitive data in the organization.
- For a **non-technical** example, consider the multiple layers of access required to get to the actual data in a data center. First, **a lock** on the door provides a physical barrier to access the data storage devices. Second, a **technical access rule** prevents access to the data via the network. Finally, **a policy, or administrative control defines the rules** that assign access to authorized individuals.

### Principle of Least Privilege
...is a **standard of permitting only minimum access necessary for users or programs to fulfill their function**. Users are provided access only to the systems and programs they need to perform their specific job or tasks. For example, only individuals working in billing will be allowed to view consumer financial data, and even fewer individuals will have the authority to change or delete that data. This maintains confidentiality and integrity while also allowing availability by providing administrative access with an appropriate password or sign-on that proves the user has the appropriate permissions to access that data.

#### Privileged Access Management
Privileged access management provides the first and perhaps most familiar use case. Consider a human user identity that is granted various create, read, update, and delete privileges on a database. Without privileged access management, the system’s access control would have those privileges assigned to the administrative user in a static way, effectively “on” 24 hours a day, every day.
- **Privileged accounts are those with permissions beyond those of normal users, such as managers and administrators.** Broadly speaking, these accounts have elevated privileges and are used by many different classes of users, including:
  - Systems administrators, who have the principal responsibilities for operating systems, applications deployment and performance management. 
  - Help desk or IT support staff, who often need to view or manipulate endpoints, servers and applications platforms by using privileged or restricted operations. 
  - Security analysts, who may require rapid access to the entire IT infrastructure, systems, endpoints and data environment of the organization. 
Typical measures used for moderating the potential for elevated risks from misuse or abuse of privileged accounts include the following: 
- More extensive and detailed logging than regular user accounts. The record of privileged actions is vitally important, as both a deterrent (for privileged account holders that might be tempted to engage in untoward activity) and an administrative control (the logs can be audited and reviewed to detect and respond to malicious activity). 
- More stringent access control than regular user accounts. As we will see emphasized in this course, even nonprivileged users should be required to use MFA methods to gain access to organizational systems and networks. - Privileged users—or more accurately, highly trusted users with access to privileged accounts—should be required to go through additional or more rigorous authentication prior to those privileges. Just-in-time identity should also be considered as a way to restrict the use of these privileges to specific tasks and the times in which the user is executing them. 
- Deeper trust verification than regular user accounts. Privileged account holders should be subject to more detailed background checks, stricter nondisclosure agreements and acceptable use policies, and be willing to be subject to financial investigation. Periodic or event-triggered updates to these background checks may also be in order, depending on the nature of the organization’s activities and the risks it faces. 
- More auditing than regular user accounts. Privileged account activity should be monitored and audited at a greater rate and extent than regular usage.

### Segregation of Duties 
**Segregation of duties is based on the security practice that no one person should control an entire high-risk transaction from start to finish**. Segregation of duties breaks the transaction into separate parts and requires a different person to execute each part of the transaction. For example, an employee may submit an invoice for payment to a vendor (or for reimbursement to themselves), but it must be approved by a manager prior to payment

### Two-Person Integrity 
- The two-person rule is a security strategy that requires a minimum of two people to be in an area together, making it impossible for a person to be in the area alone. Many access control systems prevent an individual cardholder from entering a selected high-security area unless accompanied by at least one other person. Use of the two-person rule can help reduce insider threats to critical areas by requiring at least two individuals to be present at any time.
- It is also used for life safety within a security area; if one person has a medical emergency, there will be assistance present.

# Understand Physical Access Controls
- **Physical access controls are items you can physically touch**. They include physical mechanisms deployed to prevent, monitor, or detect direct contact with systems or areas within a facility. Examples of physical access controls include security guards, fences, motion detectors, locked doors/gates, sealed windows, lights, cable protection, laptop locks, badges, swipe cards, guard dogs, cameras, mantraps/turnstiles, and alarms.
- Physical access controls include fences, barriers, turnstiles, locks and other features that prevent unauthorized individuals from entering a physical site, such as a workplace.
- Monitoring - the use of physical access controls and monitoring personnel and equipment entering and leaving as well as auditing/logging all physical events are primary elements in maintaining overall organizational security.
  - Cameras are normally integrated into the overall security program and centrally monitored. Cameras provide a flexible method of surveillance and monitoring.
  - A log is a record of events that have occurred. Electronic systems that capture system and security logs within software will be covered in another section.
  - Security guards are an effective physical security control.
  - Alarm systems are commonly found on doors and windows in homes and office buildings. In their simplest form, they are designed to alert the appropriate personnel when a door or window is opened unexpectedly.

# Understand Logical Access Controls

- Logical access controls are electronic methods that limit someone from getting access to systems, and sometimes even to tangible assets or areas. Types of logical access controls include: 
  - Passwords
  - Biometrics (implemented on a system, such as a smartphone or laptop)
  - Badge/token readers connected to a system

- **Discretionary access control (DAC) is a specific type of access control policy that is enforced over all subjects and objects in an information system**. In DAC, the policy specifies that a subject who has been granted access to information can do one or more of the following:
  - Pass the information to other subjects or objects 
  - Grant its privileges to other subjects 
  - Change security attributes on subjects, objects, information systems or system components 
  - Choose the security attributes to be associated with newly created or revised objects; and/or 
  - Change the rules governing access control; mandatory access controls restrict this capability
 
- Mandatory Access Control (MAC)
**A mandatory access control (MAC) policy is one that is uniformly enforced across all subjects and objects within the boundary of an information system.** In simplest terms, this means that only properly designated security administrators, as trusted subjects, can modify any of the security rules that are established for subjects and objects within the system. This also means that for all subjects defined by the organization (that is, known to its integrated identity management and access control system), the organization assigns a subset of total privileges for a subset of objects, such that the subject is constrained from doing any of the following:
- Passing the information to unauthorized subjects or objects
- Granting its privileges to other subjects
- Changing one or more security attributes on subjects, objects, the information system or system components
- Choosing the security attributes to be associated with newly created or modified objects
- Changing the rules governing access control

- Role-based Access Control
  - Role-based access control (RBAC), as the name suggests, sets up user permissions based on roles. Each role represents users with similar or identical permissions.
  - Provides each worker privileges based on what role they have in the organization.
  - Only Human Resources staff have access to personnel files, for example; only Finance has access to bank accounts; each manager has access to their own direct reports and their own department.
  - Very high-level system administrators may have access to everything; new employees would have very limited access, the minimum required to do their jobs.
 
# Chapter 3 Summary
- [Chapter 3 Quizlet Flashcards](https://quizlet.com/669187151/chapter-3-access-controls-concepts-flash-cards/)
- [Chapter 3 Overview](https://learn.isc2.org/content/enforced/9541-CC-SPT-GLOBAL-1ED-1M/build/chapter_03/assets/EDU-CC-70255-ch03_Takeaway.pdf?_&d2lSessionVal=6eLDFtTzOfyS237SfA6UBMP3K&ou=9541)

### Chapter 3 Glossary
- Audit - Independent review and examination of records and activities to assess the adequacy of system controls, to ensure compliance with established policies and operational procedures. NIST SP 1800-15B
- Crime Prevention through Environmental Design (CPTED) - An architectural approach to the design of buildings and spaces which emphasizes passive features to reduce the likelihood of criminal activity.
- Defense in Depth - Information security strategy integrating people, technology, and operations capabilities to establish variable barriers across multiple layers and missions of the organization. Source: NIST SP 800-53 Rev 4
- Discretionary Access Control (DAC) - A certain amount of access control is left to the discretion of the object’s owner, or anyone else who is authorized to control the object’s access. The owner can determine who should have access rights to an object and what those rights should be. NIST SP 800-192
- Encrypt - To protect private information by putting it into a form that can only be read by people who have permission to do so.
- Firewalls - Devices that enforce administrative security policies by filtering incoming traffic based on a set of rules.
- Insider Threat - An entity with authorized access that has the potential to harm an information system through destruction, disclosure, modification of data, and/or denial of service. NIST SP 800-32
- iOS - An operating system manufactured by Apple Inc. Used for mobile devices.
- Layered Defense - The use of multiple controls arranged in series to provide several consecutive controls to protect an asset; also called defense in depth.
- Linux - An operating system that is open source, making its source code legally available to end users.
- Log Anomaly - A system irregularity that is identified when studying log entries which could represent events of interest for further surveillance.
- Logging - Collecting and storing user activities in a log, which is a record of the events occurring within an organization’s systems and networks. NIST SP 1800-25B.
- Logical Access Control Systems - An automated system that controls an individual’s ability to access one or more computer system resources, such as a workstation, network, application or database. A logical access control system requires the validation of an individual’s identity through some mechanism, such as a PIN, card, biometric or other token. It has the capability to assign different access privileges to different individuals depending on their roles and responsibilities in an organization. NIST SP 800-53 Rev.5.
- Mandatory Access Control - Access control that requires the system itself to manage access controls in accordance with the organization’s security policies.
- Mantrap - An entrance to a building or an area that requires people to pass through two doors with only one door opened at a time.
- Object - Passive information system-related entity (e.g., devices, files, records, tables, processes, programs, domains) containing or receiving information. Access to an object (by a subject) implies access to the information it contains. See subject. Source: NIST SP 800-53 Rev 4
- Physical Access Controls - Controls implemented through a tangible mechanism. Examples include walls, fences, guards, locks, etc. In modern organizations, many physical control systems are linked to technical/logical systems, such as badge readers connected to door locks.
- Principle of Least Privilege - The principle that users and programs should have only the minimum privileges necessary to complete their tasks. NIST SP 800-179
- Privileged Account - An information system account with approved authorizations of a privileged user. NIST SP 800-53 Rev. 4
- Ransomware - A type of malicious software that locks the computer screen or files, thus preventing or limiting a user from accessing their system and data until money is paid.
- Role-based access control (RBAC) - An access control system that sets up user permissions based on roles.
- Rule - An instruction developed to allow or deny access to a system by comparing the validated identity of the subject to an access control list.
- Segregation of Duties - The practice of ensuring that an organizational process cannot be completed by a single person; forces collusion as a means to reduce insider threats. Also commonly known as Separation of Duties.
- Subject - Generally an individual, process or device causing information to flow among objects or change to the system state. Source: NIST SP800-53 R4
- Technical Controls - The security controls (i.e., safeguards or countermeasures) for an information system that are primarily implemented and executed by the information system through mechanisms contained in the hardware, software or firmware components of the system.
- Turnstile - A one-way spinning door or barrier that allows only one person at a time to enter a building or pass through an area.
- Unix - An operating system used in software development.
- User Provisioning - The process of creating, maintaining and deactivating user identities on a system. 

# Chapter 4
- [Module 1: Understand Computer Networking (D4.1.1, D4.1.2)](#understand-computer-networking)
- [Module 2: Understand Network Cyber Threats and Attacks (D4.1.2, D4.2.2, D4.2.3)](#understand-network-cyber-threats-and-attacks)
- [Module 3: Understand Network Security Infrastructure (D4.3.1, D4.3.2)](#understand-network-security-infrastructure)
- [Modual 4: Summary](#chapter-4-summary)

# Understand Computer Networking 
![ISC2_biz_networking](https://i.imgur.com/Ayox7HD.png)

This diagram represents a small business network, which we will build upon during this lesson. The lines depict wired connections. Notice how all devices behind the firewall connect via the network switch, and the firewall lies between the network switch and the internet. 

![ISC2_home_network](https://i.imgur.com/7I8zuwO.png)

The network diagram below represents a typical home network. Notice the primary difference between the home network and the business network is that the router, firewall, and network switch are often combined into one device supplied by your internet provider and shown here as the wireless access point. 

### Networking Models
- Many different models, architectures and standards exist that provide ways to interconnect different hardware and software systems with each other for the purposes of sharing information, coordinating their activities and accomplishing joint or shared tasks.
- Computers and networks emerge from the integration of communication devices, storage devices, processing devices, security devices, input devices, output devices, operating systems, software, services, data and people.
- Translating the organization’s security needs into safe, reliable and effective network systems needs to start with a simple premise. The purpose of all communications is to exchange information and ideas between people and organizations so that they can get work done.
- Those simple goals can be re-expressed in network (and security) terms such as:
  - Provide reliable, managed communications between hosts (and users)
  - Isolate functions in layers
  - Use packets as the basis of communication
  - Standardize routing, addressing and control
  - Allow layers beyond internetworking to add functionality
  - Be vendor-agnostic, scalable and resilient
- Networking Terms and Models
  - 

### Open Systems Interconnection (OSI) Model 
![ISC2_network_models](https://i.imgur.com/aVp8ynM.png)

The Application, Presentation, and Session Layers (5-7) are commonly referred to simply as data. However, each layer has the potential to perform encapsulation. Encapsulation is the addition of header and possibly a footer (trailer) data by a protocol used at that layer of the OSI model. Encapsulation is particularly important when discussing Transport, Network and Data Link layers (2-4), which all generally include some form of header. 

- It's worth mapping some common networking terminology to the OSI Model so you can see the value in the conceptual model. Consider the following examples: 
  - When someone references an image file like a JPEG or PNG, we are talking about the Presentation Layer (6). 
  - When discussing logical ports such as NetBIOS, we are discussing the Session Layer (5).
  - When discussing TCP/UDP, we are discussing the Transport Layer (4).
  - When discussing routers sending packets, we are discussing the Network Layer (3). 
  - When discussing switches, bridges or WAPs sending frames, we are discussing the Data Link Layer (2).

The inverse action occurs as data moves up the OSI model layers from Physical to Application. This process is known as de-encapsulation  (or decapsulation). The header and footer are used to properly interpret the data payload and are then discarded. As we move up the OSI model, the data unit becomes smaller. The encapsulation/de-encapsulation process is best depicted visually below: 

![de-encapsulation](https://i.imgur.com/HaiqF5N.png)

### Transmission Control Protocol/Internet Protocol (TCP/IP)
At the Application Layer, TCP/IP protocols include Telnet, **File Transfer Protocol (FTP), Simple Mail Transport Protocol (SMTP)**, and Domain Name Service (DNS). The two primary Transport Layer protocols of TCP/IP are TCP and UDP. TCP is a full-duplex connection-oriented protocol, whereas UDP is a simplex connectionless protocol. In the Internet Layer, **Internet Control Message Protocol (ICMP)** is used to determine the health of a network or a specific link. ICMP is utilized by ping, traceroute and other network management tools. The ping utility employs ICMP echo packets and bounces them off remote systems. 

![TCP_IP](https://i.imgur.com/5ycfUN7.png)

The most widely used protocol suite is TCP/IP, but it is not just a single protocol; rather, it is a protocol stack comprising dozens of individual protocols. TCP/IP is a platform-independent protocol based on open standards. However, this is both a benefit and a drawback. TCP/IP can be found in just about every available operating system, but it consumes a significant amount of resources and is relatively easy to hack into because it was designed for ease of use rather than for security.

### Internet Protocol (IPv4 and IPv6)
IP hosts/devices associate an address with a unique logical address. An IPv4 address is expressed as four octets separated by a dot (.), for example, 216.12.146.140. Each octet may have a value between 0 and 255. However, 0 is the network itself (not a device on that network), and 255 is generally reserved for broadcast purposes. Each address is subdivided into two parts: the network number and the host. The network number assigned by an external organization, such as the Internet Corporation for Assigned Names and Numbers (ICANN), represents the organization’s network. The host represents the network interface within the network.  

![IPv4_32bit](https://i.imgur.com/LLLH4Uo.png)

To ease network administration, networks are typically divided into subnets. Because subnets cannot be distinguished with the addressing scheme discussed so far, a separate mechanism, the subnet mask, is used to define the part of the address used for the subnet. The mask is usually converted to decimal notation like 255.255.255.0.  

| Start Range | End Range |
| ----------- | ----------- |
| 10.0.0.0 | 10.255.255.254 |
| 172.16.0.0 | 172.31.255.254 |
| 192.168.0.0 | 192.168.255.254 |

The first octet of 127 is reserved for a **computer’s loopback address**. Usually, **the address 127.0.0.1** is used. The loopback address is used to provide a mechanism for self-diagnosis and troubleshooting at the machine level. 

IPv6 is a modernization of IPv4, which addressed a number of weaknesses in the IPv4 environment:

- A much larger address field: IPv6 addresses are 128 bits, which supports 2128 or 340,282,366,920,938,463,463,374,607,431,768,211,456 hosts. This ensures that we will not run out of addresses.
- Improved security: IPsec is an optional part of IPv4 networks, but a mandatory component of IPv6 networks. This will help ensure the integrity and confidentiality of IP packets and allow communicating partners to authenticate with each other.
- Improved quality of service (QoS): This will help services obtain an appropriate share of a network’s bandwidth.

An IPv6 address is shown as 8 groups of four digits. Instead of numeric (0-9) digits like IPv4, IPv6 addresses use the hexadecimal range (0000-ffff) and are separated by colons (:) rather than periods (.). An example IPv6 address is **2001:0db8:0000:0000:0000:ffff:0000:0001**. To make it easier for humans to read and type, it can be shortened **by removing the leading zeros at the beginning of each field** and substituting two colons (::) for the longest consecutive zero fields. All fields must retain at least one digit. **After shortening, the example address above is rendered as 2001:db8::ffff:0:1**, which is much easier to type.
- ::1 is the local loopback address, used the same as 127.0.0.1 in IPv4.
- The range 2001:db8:: to 2001:db8:ffff:ffff:ffff:ffff:ffff:ffff is reserved for documentation use, just like in the examples above.
- fc00:: to fdff:ffff:ffff:ffff:ffff:ffff:ffff:ffff are addresses reserved for internal network use and are not routable on the internet.

### Ports and Protocols (Applications/Services)
- Physcial Ports
  - Physical ports are the ports on the routers, switches, servers, computers, etc. that you connect the wires, e.g., fiber optic cables, Cat5 cables, etc., to create a network.
- Logical Ports
  - In the Application Layer of the TCP/IP model (which includes the Session, Presentation, and Application Layers of the OSI model) reside numerous application- or service-specific protocols. Data types are mapped using port numbers associated with services. For example, web traffic (or HTTP) is port 80. Secure web traffic (or HTTPS) is port 443.
  - Well-known ports (0–1023): These ports are related to the common protocols that are at the core of the Transport Control Protocol/Internet Protocol (TCP/IP) model, Domain Name Service (DNS), Simple Mail Transfer Protocol (SMTP), etc.
  - Registered ports (1024–49151): These ports are often associated with proprietary applications from vendors and developers. While they are officially approved by the Internet Assigned Numbers Authority (IANA), in practice many vendors simply implement a port of their choosing. Examples include Remote Authentication Dial-In User Service (RADIUS) authentication (1812), Microsoft SQL Server (1433/1434) and the Docker REST API (2375/2376).
  - Dynamic or private ports (49152–65535): Whenever a service is requested that is associated with well-known or registered ports, those services will respond with a dynamic port that is used for that session and then released.

Secure Ports
Some network protocols transmit information in clear text, meaning it is not encrypted and should not be used. Clear text information is subject to network sniffing. Network sniffing could also reveal the content of documents and other files if they are sent via insecure protocols. The table below shows some of the insecure protocols along with recommended secure alternatives.

| Insecure Port | Description | Protocol | Secure Alt Port | Protocol |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| 21 - FTP | Port 21, File Transfer Protocol (FTP) sends the username and password using plaintext from the client to the server. This could be intercepted by an attacker and later used to retrieve confidential information from the server. The secure alternative, SFTP, on port 22 uses encryption to protect the user credentials and packets of data being transferred. | File Transfer Protocol | 22* - SFTP | Secure File Transfer Protocol |
| 23 - Telnet | Port 23, telnet, is used by many Linux systems and any other systems as a basic text-based terminal. All information to and from the host on a telnet connection is sent in plaintext and can be intercepted by an attacker. This includes username and password as well as all information that is being presented on the screen, since this interface is all text. Secure Shell (SSH) on port 22 uses encryption to ensure that traffic between the host and terminal is not sent in a plaintext format. | Telnet | 22* - SFTP | Secure Shell |
| 25 - SMTP | Port 25, Simple Mail Transfer Protocol (SMTP) is the default unencrypted port for sending email messages. Since it is unencrypted, data contained within the emails could be discovered by network sniffing. The secure alternative is to use port 587 for SMTP using Transport Layer Security (TLS) which will encrypt the data between the mail client and the mail server. | Simple Mail Transfer Protocol | 587 - SMTP | SMTP with TLS |
| 37 - Time | Port 37, Time Protocol, may be in use by legacy equipment and has mostly been replaced by using port 123 for Network Time Protocol (NTP). NTP on port 123 offers better error-handling capabilities, which reduces the likelihood of unexpected errors. | Time Protocol | 123 - NTP | Network Time Protocol |
| 53 - DNS | Port 53, Domain Name Service (DNS), is still used widely. However, using DNS over TLS (DoT) on port 853 protects DNS information from being modified in transit. | Domain Name Service | 853 - DoT | DNS over TLS (DoT) |
| 80 - HTTP | Port 80, HyperText Transfer Protocol (HTTP) is the basis of nearly all web browser traffic on the internet. Information sent via HTTP is not encrypted and is susceptible to sniffing attacks. HTTPS using TLS encryption is preferred, as it protects the data in transit between the server and the browser. Note that this is often notated as SSL/TLS. Secure Sockets Layer (SSL) has been compromised is no longer considered secure. It is now recommended for web servers and clients to use Transport Layer Security (TLS) 1.3 or higher for the best protection. | HyperText Transfer Protocol | 443 - HTTPS | HyperText Transfer Protocol (SSL/TLS) |
| 143 - IMAP | Port 143, Internet Message Access Protocol (IMAP) is a protocol used for retrieving emails. IMAP traffic on port 143 is not encrypted and susceptible to network sniffing. The secure alternative is to use port 993 for IMAP, which adds SSL/TLS security to encrypt the data between the mail client and the mail server. | Internet Message Access Protocol | 993 - IMAP | IMAP for SSL/TLS |
| 161/162 - SNMP | Ports 161 and 162, Simple Network Management Protocol, are commonly used to send and receive data used for managing infrastructure devices. Because sensitive information is often included in these messages, it is recommended to use SNMP version 2 or 3 (abbreviated SNMPv2 or SNMPv3) to include encryption and additional security features. Unlike many others discussed here, all versions of SNMP use the same ports, so there is not a definitive secure and insecure pairing. Additional context will be needed to determine if information on ports 161 and 162 is secured or not. | Simple Network Management Protocol | 161/162 - SNMP | SNMPv3 |
| 445 - SMB | Port 445, Server Message Block (SMB), is used by many versions of Windows for accessing files over the network. Files are transmitted unencrypted, and many vulnerabilities are well-known. Therefore, it is recommended that traffic on port 445 should not be allowed to pass through a firewall at the network perimeter. A more secure alternative is port 2049, Network File System (NFS). Although NFS can use encryption, it is recommended that NFS not be allowed through firewalls either. | Server Message Block | 2049 - NFS | Network File System |
| 389 - LDAP | Port 389, Lightweight Directory Access Protocol (LDAP), is used to communicate directory information from servers to clients. This can be an address book for email or usernames for logins. The LDAP protocol also allows records in the directory to be updated, introducing additional risk. Since LDAP is not encrypted, it is susceptible to sniffing and manipulation attacks. Lightweight Directory Access Protocol Secure (LDAPS) adds SSL/TLS security to protect the information while it is in transit. | Lightweight Directory Access Protocol | 636 - LDAPS | Lightweight Directory Access Protocol Secure |

# Understand Network Cyber Threats and Attacks
### Types of Threats
- Spoofing: An attack with the goal of gaining access to a target system through the use of a falsified identity. Spoofing can be used against IP addresses, MAC address, usernames, system names, wireless network SSIDs, email addresses, and many other types of logical identification.
- Phishing - An attack that attempts to misdirect legitimate users to malicious websites through the abuse of URLs or hyperlinks in emails could be considered phishing.
- DoS/DDoS: A denial-of-service (DoS) attack is a network resource consumption attack that has the primary goal of preventing legitimate activity on a victimized system. Attacks involving numerous unsuspecting secondary victim systems are known as distributed denial-of-service (DDoS) attacks.
- Virus: The computer virus is perhaps the earliest form of malicious code to plague security administrators. As with biological viruses, computer viruses have two main functions—propagation and destruction. A virus is a self-replicating piece of code that spreads without the consent of a user, but frequently with their assistance (a user has to click on a link or open a file).
- Worm: Worms pose a significant risk to network security. They contain the same destructive potential as other malicious code objects with an added twist—they propagate themselves without requiring any human intervention.
- Trojan: Named after the ancient story of the Trojan horse, the Trojan is a software program that appears benevolent but carries a malicious, behind-the-scenes payload that has the potential to wreak havoc on a system or network. For example, ransomware often uses a Trojan to infect a target machine and then uses encryption technology to encrypt documents, spreadsheets and other files stored on the system with a key known only to the malware creator
- On-path Attack: In an on-path attack, attackers place themselves between two devices, often between a web browser and a web server, to intercept or modify information that is intended for one or both of the endpoints. On-path attacks are also known as man-in-the-middle (MITM) attacks.
- Side-channel: A side-channel attack is a passive, noninvasive attack to observe the operation of a device. Methods include power monitoring, timing and fault analysis attacks.
- Advanced Persistent Threat (APT): Advanced persistent threat (APT) refers to threats that demonstrate an unusually high level of technical and operational sophistication spanning months or even years. APT attacks are often conducted by highly organized groups of attackers.
- Insider Threat: Insider threats are threats that arise from individuals who are trusted by the organization. These could be disgruntled employees or employees involved in espionage. Insider threats are not always willing participants. A trusted user who falls victim to a scam could be an unwilling insider threat.
- Malware: A program that is inserted into a system, usually covertly, with the intent of compromising the confidentiality, integrity or availability of the victim’s data, applications or operating system or otherwise annoying or disrupting the victim.
- Ransomware: Malware used for the purpose of facilitating a ransom attack. Ransomware attacks often use cryptography to “lock” the files on an affected computer and require the payment of a ransom fee in return for the “unlock” code.

### Intrusion Detection System (IDS)
An intrusion occurs when an attacker is able to bypass or thwart security mechanisms and gain access to an organization’s resources. Intrusion detection is a specific form of monitoring that monitors recorded information and real-time events to detect abnormal activity indicating a potential incident or intrusion. An intrusion detection system (IDS) automates the inspection of logs and real-time system events to detect intrusion attempts and system failures. An IDS is intended as part of a defense-in-depth security plan. It will work with, and complement, other security mechanisms such as firewalls, but it does not replace them. 

IDSs can recognize attacks that come from external connections, such as an attack from the internet, and attacks that spread internally, such as a malicious worm. Once they detect a suspicious event, they respond by sending alerts or raising alarms. A primary goal of an IDS is to provide a means for a timely and accurate response to intrusions. 

Intrusion detection and prevention refer to capabilities that are part of isolating and protecting a more secure or more trusted domain or zone from one that is less trusted or less secure. These are natural functions to expect of a firewall, for example.  

IDS types are commonly classified as host-based and network-based. A host-based IDS (HIDS) monitors a single computer or host. A network-based IDS (NIDS) monitors a network by observing network traffic patterns. 

### Preventing Threats
While there is no single step you can take to protect against all threats, there are some basic steps you can take that help reduce the risk of many types of threats.
- Keep systems and applications up to date. Vendors regularly release patches to correct bugs and security flaws, but these only help when they are applied. Patch management ensures that systems and applications are kept up to date with relevant patches.
- Remove or disable unneeded services and protocols. If a system doesn’t need a service or protocol, it should not be running. Attackers cannot exploit a vulnerability in a service or protocol that isn’t running on a system. As an extreme contrast, imagine a web server is running every available service and protocol. It is vulnerable to potential attacks on any of these services and protocols.
- Use intrusion detection and prevention systems. As discussed, intrusion detection and prevention systems observe activity, attempt to detect threats and provide alerts. They can often block or stop attacks.
- Use up-to-date anti-malware software. We have already covered the various types of malicious code such as viruses and worms. A primary countermeasure is anti-malware software.
- Use firewalls. Firewalls can prevent many different types of threats. Network-based firewalls protect entire networks, and host-based firewalls protect individual systems. This chapter included a section describing how firewalls can prevent attacks.

# Understand Network Security Infrastructure
### Memorandum of Understanding (MOU)/Memorandum of Agreement (MOA) 
Some organizations seeking to minimize downtime and enhance BC (Business Continuity) and DR (Disaster Recovery) capabilities will create agreements with other, similar organizations. They agree that if one of the parties experiences an emergency and cannot operate within their own facility, the other party will share its resources and let them operate within theirs in order to maintain critical functions. These agreements often even include competitors, because their facilities and resources meet the needs of their particular industry. 

These agreements are called joint operating agreements (JOA) or memoranda of understanding (MOU) or memoranda of agreement (MOA). Sometimes these agreements are mandated by regulatory requirements, or they might just be part of the administrative safeguards instituted by an entity within the guidelines of its industry. 

The difference between an MOA or MOU  and an SLA is that a Memorandum of Understanding is more directly related to what can be done with a system or the information. 

We must be very cautious when outsourcing with cloud-based services, because we have to make sure that we understand exactly what we are agreeing to. If the SLA promises 100 percent accessibility to information, is the access directly to you at the moment, or is it access to their website or through their portal when they open on Monday? That's where you'll rely on your legal team, who can supervise and review the conditions carefully before you sign the dotted line at the bottom. 

### Cloud Computing
Usually associated with an internet-based set of computing resources, and typically sold as a service, provided by a cloud service provider (CSP). 

Cloud computing is very similar to the electrical or power grid. It is provisioned in a geographic location and is sourced using an electrical means that is not necessarily obvious to the consumer. But when you want electricity, it’s available to you via a common standard interface and you pay only for what you use. In these ways, cloud computing is very similar. It is a very scalable, elastic and easy-to-use “utility” for the provisioning and deployment of Information Technology (IT) services.  

There are various definitions of what cloud computing means according to the leading standards, including NIST. This NIST definition is commonly used around the globe, cited by professionals and others alike to clarify what the term “cloud” means:   “a model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources (such as networks, servers, storage, applications, and services) that can be rapidly provisioned and released with minimal management effort or service provider interaction.” -- NIST SP 800-145 

### Cloud Characteristics
Cloud-based assets include any resources that an organization accesses using cloud computing. Cloud computing refers to on-demand access to computing resources available from almost anywhere, and cloud computing resources are highly available and easily scalable. Organizations typically lease cloud-based resources from outside the organization. Cloud computing has many benefits for organizations, which include but are not limited to: 
- Usage is metered and priced according to units (or instances) consumed. This can also be billed back to specific departments or functions.
- Reduced cost of ownership. There is no need to buy any assets for everyday use, no loss of asset value over time and a reduction of other related costs of maintenance and support.
- Reduced energy and cooling costs, along with “green IT” environment effect with optimum use of IT resources and systems.
- Allows an enterprise to scale up new software or data-based services/solutions through cloud systems quickly and without having to install massive hardware locally.

### Service Models
Some cloud-based services only provide data storage and access. When storing data in the cloud, organizations must ensure that security controls are in place to prevent unauthorized access to the data. 

There are varying levels of responsibility for assets depending on the service model. This includes maintaining the assets, ensuring they remain functional, and keeping the systems and applications up to date with current patches. In some cases, the cloud service provider is responsible for these steps. In other cases, the consumer is responsible for these steps. 

Types of cloud computing service models include **Software as a Service (SaaS)** , **Platform as a Service (PaaS)** and **Infrastructure as a Service (IaaS)**. There are four cloud deployment models. The cloud deployment model also affects the breakdown of responsibilities of the cloud-based assets. The four cloud models available are public, private, hybrid and community .

- Public: Public clouds are what we commonly refer to as the cloud for the public user. It is very easy to get access to a public cloud. There is no real mechanism, other than applying for and paying for the cloud service. It is open to the public and is, therefore, a shared resource that many people will be able to use as part of a resource pool. A public cloud deployment model includes assets available for any consumers to rent or lease and is hosted by an external cloud service provider (CSP). Service level agreements can be effective at ensuring the CSP provides the cloud-based services at a level acceptable to the organization.
- Private: Private clouds begin with the same technical concept as public clouds, except that instead of being shared with the public, they are generally developed and deployed for a private organization that builds its own cloud. Organizations can create and host private clouds using their own resources. Therefore, this deployment model includes cloud-based assets for a single organization. As such, the organization is responsible for all maintenance. However, an organization can also rent resources from a third party and split maintenance requirements based on the service model (SaaS, PaaS or IaaS). Private clouds provide organizations and their departments private access to the computing, storage, networking and software assets that are available in the private cloud.
- Hybrid: A hybrid cloud deployment model is created by combining two forms of cloud computing deployment models, typically a public and private cloud. Hybrid cloud computing is gaining popularity with organizations by providing them with the ability to retain control of their IT environments, conveniently allowing them to use public cloud service to fulfill non-mission-critical workloads, and taking advantage of flexibility, scalability and cost savings. Important drivers or benefits of hybrid cloud deployments include: Retaining ownership and oversight of critical tasks and processes related to technology, Reusing previous investments in technology within the organization, Control over most critical business components and systems, and Cost-effective means to fulfilling noncritical business functions (utilizing public cloud components).
- Community: Community clouds can be either public or private. What makes them unique is that they are generally developed for a particular community. An example could be a public community cloud focused primarily on organic food, or maybe a community cloud focused specifically on financial services. The idea behind the community cloud is that people of like minds or similar interests can get together, share IT capabilities and services, and use them in a way that is beneficial for the particular interests that they share.

### Managed Service Provider (MSP)
A managed service provider (MSP) is a company that manages information technology assets for another company. Small- and medium-sized businesses commonly outsource part or all of their information technology functions to an MSP to manage day-to-day operations or to provide expertise in areas the company does not have. Organizations may also use an MSP to provide network and security monitoring and patching services. Today, many MSPs offer cloud-based services augmenting SaaS solutions with active incident investigation and response activities. One such example is a managed detection and response (MDR) service, where a vendor monitors firewall and other security tools to provide expertise in triaging events. 

Some other common MSP implementations are: 
- Augment in-house staff for projects
- Utilize expertise for implementation of a product or service
- Provide payroll services
- Provide Help Desk service management
- Monitor and respond to security incidents
- Manage all in-house IT infrastructure

### Service-Level Agreement (SLA)
The cloud computing service-level agreement (cloud SLA) is an agreement between a cloud service provider and a cloud service customer based on a taxonomy of cloud computing– specific terms to set the quality of the cloud services delivered. It characterizes quality of the cloud services delivered in terms of a set of measurable properties specific to cloud computing (business and technical) and a given set of cloud computing roles (cloud service customer, cloud service provider, and related sub-roles).

Think of a rule book and legal contract—that combination is what you have in a service-level agreement (SLA). Let us not underestimate or downplay the importance of this document/ agreement. In it, the minimum level of service, availability, security, controls, processes, communications, support and many other crucial business elements are stated and agreed to by both parties.  

The purpose of an SLA is to document specific parameters, minimum service levels and remedies for any failure to meet the specified requirements. It should also affirm data ownership and specify data return and destruction details. Other important SLA points to consider include the following:
- Cloud system infrastructure details and security standards
- Customer right to audit legal and regulatory compliance by the CSP
- Rights and costs associated with continuing and discontinuing service use
- Service availability
- Service performance
- Data security and privacy
- Disaster recovery processes
- Data location
- Data access
- Data portability
- Problem identification and resolution expectations
- Change management processes
- Dispute mediation processes
- Exit strategy

### Network Design
The objective of network design is to satisfy data communication requirements and result in efficient overall performance.
- Network segmentation involves controlling traffic among networked devices. Complete or physical network segmentation occurs when a network is isolated from all outside communications, so transactions can only occur between devices within the segmented network.
- A DMZ (Demilitarized Zone) is a network area that is designed to be accessed by outside visitors but is still isolated from the private network of the organization. The DMZ is often the host of public web, email, file and other resource servers.
- VLANs (Virtual Local Area Network) are created by switches to logically segment a network without altering its physical topology.
- A virtual private network (VPN) is a communication tunnel that provides point-to-point transmission of both authentication and data traffic over an untrusted network.
- Defense in depth uses multiple types of access controls in literal or theoretical layers to help an organization avoid a monolithic security stance.
- Network access control (NAC) is a concept of controlling access to an environment through strict adherence to and implementation of security policy.

![defense_in_depth](https://i.imgur.com/igE7REm.png)

Defense in depth provides more of a starting point for considering all types of controls—administrative, technological, and physical—that empower insiders and operators to work together to protect their organization and its systems. Here are some examples that further explain the concept of defense in depth: 
- Data: Controls that protect the actual data with technologies such as encryption, data leak prevention, identity and access management and data controls.
- Application: Controls that protect the application itself with technologies such as data leak prevention, application firewalls and database monitors.
- Host: Every control that is placed at the endpoint level, such as antivirus, endpoint firewall, configuration and patch management.
- Internal network: Controls that are in place to protect uncontrolled data flow and user access across the organizational network. Relevant technologies include intrusion detection systems, intrusion prevention systems, internal firewalls and network access controls.
- Perimeter: Controls that protect against unauthorized access to the network. This level includes the use of technologies such as gateway firewalls, honeypots, malware analysis and secure demilitarized zones (DMZs).
- Physical: Controls that provide a physical barrier, such as locks, walls or access control.
- Policies, procedures and awareness: Administrative controls that reduce insider threats (intentional and unintentional) and identify risks as soon as they appear.

### Zero trust networks
are often microsegmented networks, with firewalls at nearly every connecting point. Zero trust encapsulates information assets, the services that apply to them and their security properties. This concept recognizes that once inside a trust-but-verify environment, a user has perhaps unlimited capabilities to roam around, identify assets and systems and potentially find exploitable vulnerabilities. 

### Network Access Control (NAC)
An organization’s network is perhaps one of its most critical assets. As such, it is vital that we both know and control access to it, both from insiders (e.g., employees, contractors) and outsiders (e.g., customers, corporate partners, vendors). We need to be able to see who and what is attempting to make a network connection. At one time, network access was limited to internal devices. Gradually, that was extended to remote connections, although initially those were the exceptions rather than the norm. This started to change with the concepts of bring your own device (BYOD) and Internet of Things (IoT). Let’s consider some possible use cases for NAC deployment: 
- Medical devices
- IoT devices
- BYOD/mobile devices (laptops, tablets, smartphones)
- Guest users and contractors

### Network Segmentation (Demilitarized Zone (DMZ))
![IoT](https://i.imgur.com/yXtDBnY.png)
Network segmentation is also an effective way to achieve defense in depth for distributed or multi-tiered applications. The use of a demilitarized zone (DMZ), for example, is a common practice in security architecture. With a DMZ, host systems that are accessible through the firewall are physically separated from the internal network by means of secured switches or by using an additional firewall to control traffic between the web server and the internal network. Application DMZs (or semi-trusted networks) are frequently used today to limit access to application servers to those networks or systems that have a legitimate need to connect.

Segmentation for Embedded Systems and IoT
An embedded system is a computer implemented as part of a larger system. The embedded system is typically designed around a limited set of specific functions in relation to the larger product of which it is a component. Examples of embedded systems include network-attached printers, smart TVs, HVAC controls, smart appliances, smart thermostats and medical devices. 

Network-enabled devices are any type of portable or nonportable device that has native network capabilities. This generally assumes the network in question is a wireless type of network, typically provided by a mobile telecommunications company. Network-enabled devices include smartphones, mobile phones, tablets, smart TVs or streaming media players (such as a Roku Player, Amazon Fire TV, or Google Android TV/Chromecast), network-attached printers, game systems, and much more. 

The Internet of Things (IoT) is the collection of devices that can communicate over the internet with one another or with a control console in order to affect and monitor the real world. IoT devices might be labeled as smart devices or smart-home equipment. Many of the ideas of industrial environmental control found in office buildings are finding their way into more consumer-available solutions for small offices or personal homes. 

Embedded systems and network-enabled devices that communicate with the internet are considered IoT devices and need special attention to ensure that communication is not used in a malicious manner. Because an embedded system is often in control of a mechanism in the physical world, a security breach could cause harm to people and property. Since many of these devices have multiple access routes, such as ethernet, wireless, Bluetooth, etc., special care should be taken to isolate them from other devices on the network. You can impose logical network segmentation with switches using VLANs, or through other traffic-control means, including MAC addresses, IP addresses, physical ports, protocols, or application filtering, routing, and access control management. Network segmentation can be used to isolate IoT environments. 

### Microsegmentation
The toolsets of current adversaries are polymorphic in nature and allow threats to bypass static security controls. Modern cyberattacks take advantage of traditional security models to move easily between systems within a data center. Microsegmentation aids in protecting against these threats. A fundamental design requirement of microsegmentation is to understand the protection requirements for traffic within a data center and traffic to and from the internet traffic flows. When organizations avoid infrastructure-centric design paradigms, they are more likely to become more efficient at service delivery in the data center and become apt at detecting and preventing advanced persistent threats. 

### Virtual Local Area Network (VLAN)
Virtual local area networks (VLANs) allow network administrators to use switches to create software-based LAN segments, which can segregate or consolidate traffic across multiple switch ports. Devices that share a VLAN communicate through switches as if they were on the same Layer 2 network. This image shows different VLANs — red, green and blue — connecting separate sets of ports together, while sharing the same network segment (consisting of the two switches and their connection). Since VLANs act as discrete networks, communications between VLANs must be enabled. Broadcast traffic is limited to the VLAN, reducing congestion and reducing the effectiveness of some attacks. Administration of the environment is simplified, as the VLANs can be reconfigured when individuals change their physical location or need access to different services. VLANs can be configured based on switch port, IP subnet, MAC address and protocols.

VLANs do not guarantee a network’s security. At first glance, it may seem that traffic cannot be intercepted because communication within a VLAN is restricted to member devices. However, there are attacks that allow a malicious user to see traffic from other VLANs (so-called VLAN hopping). The VLAN technology is only one tool that can improve the overall security of the network environment.

# Chapter 4 Summary
- [Chapter 4 Overview](https://learn.isc2.org/content/enforced/9541-CC-SPT-GLOBAL-1ED-1M/build/chapter_04/assets/EDU-CC-70405-ch04_Takeaway.pdf?_&d2lSessionVal=1gkTk3sBiX8MbBYEruFhawQsI&ou=9541)
- [Chapter 4 Glossary Flash Cards](https://quizlet.com/669190409/chapter-4-network-security-flash-cards/)

### Chapter 4 Glossary
Application programming interface (API) - A set of routines, standards, protocols, and tools for building software applications to access a web-based software application or web tool.
Bit - The most essential representation of data (zero or one) at Layer 1 of the Open Systems Interconnection (OSI) model.
Broadcast - Broadcast transmission is a one-to-many (one-to-everyone) form of sending internet traffic.
Byte - The byte is a unit of digital information that most commonly consists of eight bits.
Cloud computing - A model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources (e.g., networks, servers, storage, applications, and services) that can be rapidly provisioned and released with minimal management effort or service provider interaction. NIST 800-145
Community cloud - A system in which the cloud infrastructure is provisioned for exclusive use by a specific community of consumers from organizations that have shared concerns (e.g., mission, security requirements, policy and compliance considerations). It may be owned, managed and operated by one or more of the organizations in the community, a third party or some combination of them, and it may exist on or off premises. NIST 800-145 
De-encapsulation - The opposite process of encapsulation, in which bundles of data are unpacked or revealed.
Denial-of-Service (DoS) - The prevention of authorized access to resources or the delaying of time-critical operations. (Time-critical may be milliseconds or it may be hours, depending upon the service provided.) Source: NIST SP 800-27 Rev A
Domain Name Service (DNS) - This acronym can be applied to three interrelated elements: a service, a physical server and a network protocol.
Encapsulation - Enforcement of data hiding and code hiding during all phases of software development and operational use. Bundling together data and methods is the process of encapsulation; its opposite process may be called unpacking, revealing, or using other terms. Also used to refer to taking any set of data and packaging it or hiding it in another data structure, as is common in network protocols and encryption.
Encryption - The process and act of converting the message from its plaintext to ciphertext. Sometimes it is also referred to as enciphering. The two terms are sometimes used interchangeably in literature and have similar meanings.
File Transfer Protocol (FTP) - The internet protocol (and program) used to transfer files between hosts.
Fragment attack - In a fragment attack, an attacker fragments traffic in such a way that a system is unable to put data packets back together. 
Hardware - The physical parts of a computer and related devices.
Hybrid cloud - A combination of public cloud storage and private cloud storage where some critical data resides in the enterprise’s private cloud while other data is stored and accessible from a public cloud storage provider.
Infrastructure as a Service (IaaS) - The provider of the core computing, storage and network hardware and software that is the foundation upon which organizations can build and then deploy applications.  IaaS is popular in the data center where software and servers are purchased as a fully outsourced service and usually billed on usage and how much of the resource is used.
Internet Control Message Protocol (ICMP) - An IP network protocol standardized by the Internet Engineering Task Force (IETF) through RFC 792 to determine if a particular service or host is available.
Internet Protocol (IPv4) - Standard protocol for transmission of data from source to destinations in packet-switched communications networks and interconnected systems of such networks. CNSSI 4009-2015
Man-in-the-Middle - An attack where the adversary positions himself in between the user and the system so that he can intercept and alter data traveling between them. Source: NISTIR 7711
Microsegmentation - Part of a zero-trust strategy that breaks LANs into very small, highly localized zones using firewalls or similar technologies. At the limit, this places firewall at every connection point.
Oversized Packet Attack - Purposely sending a network packet that is larger than expected or larger than can be handled by the receiving system, causing the receiving system to fail unexpectedly. 
Packet - Representation of data at Layer 3 of the Open Systems Interconnection (OSI) model.
Payload - The primary action of a malicious code attack.
Payment Card Industry Data Security Standard (PCI DSS) - An information security standard administered by the Payment Card Industry Security Standards Council that applies to merchants and service providers who process credit or debit card transactions.
Platform as a Service (PaaS) - The web-authoring or application development middleware environment that allows applications to be built in the cloud before they’re deployed as SaaS assets.
Private cloud - The phrase used to describe a cloud computing platform that is implemented within the corporate firewall, under the control of the IT department. A private cloud is designed to offer the same features and benefits of cloud systems, but removes a number of objections to the cloud computing model, including control over enterprise and customer data, worries about security, and issues connected to regulatory compliance.
Protocols - A set of rules (formats and procedures) to implement and control some type of association (that is, communication) between systems. NIST SP 800-82 Rev. 2
Public cloud - The cloud infrastructure is provisioned for open use by the general public. It may be owned, managed, and operated by a business, academic, or government organization, or some combination of them. It exists on the premises of the cloud provider. NIST SP 800-145
Simple Mail Transport Protocol (SMTP) - The standard communication protocol for sending and receiving emails between senders and receivers.
Software - Computer programs and associated data that may be dynamically written or modified during execution. NIST SP 80-37 Rev. 2
Software as a Service (SaaS) - The cloud customer uses the cloud provider’s applications running within a cloud infrastructure. The applications are accessible from various client devices through either a thin client interface, such as a web browser or a program interface. The consumer does not manage or control the underlying cloud infrastructure including network, servers, operating systems, storage, or even individual application capabilities, with the possible exception of limited user-specific application configuration settings. Derived from NIST 800-145
Spoofing - Faking the sending address of a transmission to gain illegal entry into a secure system. CNSSI 4009-2015 
Transport Control Protocol/Internet Protocol (TCP/IP) Model - Internetworking protocol model created by the IETF, which specifies four layers of functionality: Link layer (physical communications), Internet Layer (network-to-network communication), Transport Layer (basic channels for connections and connectionless exchange of data between hosts), and Application Layer, where other protocols and user applications programs make use of network services.
Virtual Local Area Network (VLAN) - A logical group of workstations, servers, and network devices that appear to be on the same LAN despite their geographical distribution.
VPN - A virtual private network (VPN), built on top of existing networks, that can provide a secure communications mechanism for transmission between networks.
Wireless Area Network (WLAN) - A group of computers and devices that are located in the same vicinity, forming a network based on radio transmissions rather than wired connections. A Wi-Fi is network is a type of WLAN.
Zenmap - The graphical user interface (GUI) for the Nmap Security Scanner, an open-source application that scans networks to determine everything that is connected as well as other information.
Zero Trust - Removing the design belief that the network has any trusted space. Security is managed at each possible level, representing the most granular asset. Microsegmentation of workloads is a tool of the model. 
