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

# Chapter 1 Glossary

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
   
# Chapter 2 Glossary
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

