### Authentication Quiz

__Question 1 How is authentication different from authorization?__

Authentication is verifying an identity; authorization is verifying access to a resource.

They're the same thing.

_Authentication is verifying access to a resource; authorization is verifying an identity._

Authentication is identifying a resource; authorization is verifying access to an identity.

Correct
Right on! Authentication is proving that an entity is who they claim to be, while authorization is determining whether or not that entity is permitted to access resources.

__Question 2 What are some characteristics of a strong password? Check all that apply.__

Is used across accounts and systems

_Includes numbers and special characters_

_Is at least eight characters long_

Contains dictionary words

Correct
You got it! A strong password should contain a mix of character types and cases, and should be relatively long -- at least eight characters, but preferably more.

__Question 3 In a multi-factor authentication scheme, a password can be thought of as:__

something you have.

something you use.

_something you know._

something you are. 

Correct
Since a password is something you memorize, it's something you know when talking about multi-factor authentication schemes.

__Question 4 What are some drawbacks to using biometrics for authentication? Check all that apply.__

Biometrics are easy to share.

_There are potential privacy concerns._

Biometric authentication is much slower than alternatives.

_Biometric authentication is difficult or impossible to change if compromised._

Correct
That's exactly right! If a biometric characteristic, like your fingerprints, is compromised, your option for changing your "password" is to use a different finger. This makes "password" changes limited. Other biometrics, like iris scans, can't be changed if compromised. If biometric authentication material isn't handled securely, then identifying information about the individual can leak or be stolen.

__Question 5 In what way are U2F tokens more secure than OTP generators?__

They're password-protected.

They can't be cloned.

They're cheaper.

_They're resistant to phishing attacks._

Correct
Right on! Authentication is proving that an entity is who they claim to be, while authorization is determining whether or not that entity is permitted to access resources.

__Question 6 What elements of a certificate are inspected when a certificate is verified? Check all that apply.__

_"Not valid before" date_

Certificate key size

__"Not valid after" date__

Trust of the signatory CA

Correct
Yep! To verify a certificate, the period of validity must be checked, along with the signature of the signing certificate authority, to ensure that it's a trusted one.

__Question 7 What is a CRL?__

_Certificate Revocation List_

Certificate Recording Language

Caramel Raspberry Lemon

Certified Recursive Listener

Correct
Good job! CRL stands for "Certificate Revocation List." It's a list published by a CA, which contains certificates issued by the CA that are explicitly revoked, or made invalid.

__Question 8 What are the names of similar entities that a Directory server organizes entities into?__

Groups

Clusters

Trees

__Organizational Units__

Correct
Awesome! Directory servers have organizational units, or OUs, that are used to group similar entities.

__Question 9 True or false: The Network Access Server handles the actual authentication in a RADIUS scheme.__

True

_False_

Correct
Nice work! The Network Access Server only relays the authentication messages between the RADIUS server and the client; it doesn't make an authentication evaluation itself.

__Question 10 True or false: Clients authenticate directly against the RADIUS server.__

True

_False_

__Question 11 What does a Kerberos authentication server issue to a client that successfully authenticates?__


_A ticket-granting ticket_

An encryption key

A digital certificate

A master password

Correct
Exactly! Once authenticated, a Kerberos client receives a ticket-granting ticket from the authentication server. This TGT can then be presented to the ticket-granting service in order to be granted access to a resource.

__Question 12 What advantages does single sign-on offer? Check all that apply.__

It enforces multifactor authentication.

_It reduces time spent authenticating._

_It reduces the total number of credentials._

It provides encrypted authentication.

Correct
You nailed it! SSO allows one set of credentials to be used to access various services across sites. This reduces the total number of credentials that might be otherwise needed. SSO authentication also issues an authentication token after a user authenticates using username and password. This token then automatically authenticates the user until the token expires. So, users don't need to reauthenticate multiple times throughout a work day.

__Question 13 What does OpenID provide?__

Digital signatures

_Authentication delegation_

Certificate signing

Cryptographic hashing

Correct
Yep! OpenID allows authentication to be delegated to a third-party authentication service.
