# Understand the Security Concepts of Information Assurance (D1.1)

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

# Module 2: Understand the Risk Management Process (D1.2.1, D1.2.2)

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

[risk_treatment](https://i.imgur.com/qabuAXx.png)

- __Risk AVOIDANCE is the decision to cease the risky activity to remove the likelihood that an event will occure__ to attempt to eliminate the risk entirely. This could include ceasing operation for some or all of the activities of the organization that are exposed to a particular risk. Organization leadership may choose risk avoidance when the potential impact of a given risk is too high or if the likelihood of the risk being realized is simply too great.
- __Risk ACCEPTANCE is taking no action, ignoring the risks, and continuing risky activity.__ Management may opt for conducting the business function that is associated with the risk without any further action on the part of the organization, either because the impact or likelihood of occurrence is negligible, or because the benefit is more than enough to offset that risk.
- __Risk MITIGATION is taking actions to prevent or reduce the impact of an event.__ Mitigation can involve remediation measures, or controls, such as security controls, establishing policies, procedures, and standards to minimize adverse risk. Risk cannot always be mitigated, but mitigations such as safety measures should always be in place.
- __Risk TRANSFERENCE is passing the risk to third party__ who will accept the financial impact of the harm resulting from a risk being realized in exchange for payment.__ Typically, this is an insurance policy.

### D1, L1.2.2 Quiz

[risk_terms](https://i.imgur.com/Q2NQQpB.png)

When a company chooses to ignore a risk and proceed with a risky activity, which treatment is being applied by default? (D1, L1.2.2)
- [ ] Mitigation
- [ ] Avoidance
- [x] Acceptance
- [ ] Transference
