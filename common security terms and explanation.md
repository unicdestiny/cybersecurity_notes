## Security Fundamentals

CIA triad:
- confidentiality: prevents unauthorized access to data
- integrity: Ensure systems and data are acccessible when needed
- Availability: Ensure systems and data are accessible when needed

AAA
- Authentication: Verify identity
- Authorization: Determine permissions
- Accounting: log and track actions

Zero trust
- Security model based on "never trust,always verify"
- Every user, device, and connection must be continuously validated

Least Privilege: Users receive only the minimum permissions necessary to perfom their job.

Seperation of duties: Critical tasks are split among multiple people to reduce fraud and mistakes. 

Defense in depth: multiple layers of security controls protect systems and data

Salting: Random data added to a password before hashing to prevent rainbow table attacks

authentication factors:
- something you know: passowrd, PIN
- something you have: smart card,token,phone
- something you are: fingerprint, face scan
- somewhere you are: GPS location, network location
- something you do : typing pattern, signature dynamics

## Identity & Access Control

MFA/Multi-factor authentication: uses two or more verification factors (e.g., password + SMS code or authentication app)

SSO/Single Sign-On: allows users to access multiple applications within a system using one set of credentials

RBAC/Role-Based access Control: access permissions are assigned based on user roles (e.g., managers can access management tools)

ABAC/Attribute-Based access Control: access is granted based on attributes such as location, device type, or IP address

DAC/Discretionary access control: owner of resource decides who gets access to it (e.g. read+ write+execute rights on files)

MAC/Mandatory access control: rights about files and resources are given by file system

LDAP/Lightweight Directory Access protocol: protocol for accessing and managing directory services (like Active Directory)

RADIUS: A network protocol used for centralized authentication, authorization, and accounting (AAA) of users accessing a network.

TACACS+: A Cisco-developed AAA protocol used for centralized authentication, authorization, and accounting, mainly for managing administrative access to network devices.

FIDO2: A passwordless authentication standard that uses public key cryptography to allow secure login using devices or biometrics instead of passwords.

PIV/Personal Identity Verification: A U.S. federal goverment smart card standard used for secure identification and authentication of employees and contractors

CAC/Common access cards: a smart card used by the U.S. department of defense to provide secure identification, authentication, and access to systems and facilities.

## Identity&Access Control

Kerbos: ticket-based authentication system used in AD

OAuth: authorization framework using access tokens

OpenID connect: identity layer on top of OAuth(user login)

Federation: allows user to access multiple systems using one identity acroos organizations

## Cryptography

AES/advanced encryption standart: symmetric encryption using the same secret key for encryption and decryption

RSA: asymmetric encryption using a public key to encrypt and a private key to decrypt. In case of digital signature private key signs and public key verifies.

ECC/Elliptic curve crypto: An asymmetric cryptography method based on elliptic curve mathematics. Provide similare security to RSA with much smaller key sizes.

SHA-256:it produces a 256-bit hash value

HMAC: does integrity checking and authentication

Diffie-hellman: algorithme used for key exchange

PKI/Public Key Infrastructure: infrastructure for generating and validating keys

CA/Certificate authority: signs the certificate to make sure it's valid

CSR/certificate request: A request sent to a CA containing the public key and identifying information needed to issue a certificate.

CRL/Certificate Revocation List: A list of revoked certificates published by a CA.

OCSP: automatic protocol that checks if the certificate is valid.

TPM/Trusted Platform Module: a hardware chip that securely stores cryptographic keys and supports secure boot and disk encryption. TPM is similar to but not the same as an HSM.

HSM: dedicated hardware used to generate, store, and protect cryptographic keys.

FDE/full disk encryption: allows you to encrypt you disk so it's not readable when stolen.

SED/Self-encrypting drive

EFS/File encryption: used by windows to encrypt files

##Network Security:

TLS/Transport layer security: Is the modern replacement for SSL and provides encrypted communications. 

SSH: secure remote login running on port 22

VPN: private network tunnel over public internet

IPsec: Suite of protocols used to secure IP communications through authentication,integrity, and encryption

ESP/Encapsulating security payload:provides encryption+integrity+authentication

AH/Authentication header: integrity+authentication and no encryption

IDS/Intrusion detection system: detects intrusions that happen on the network

IPS/Intrustion prevention system: prevents intrustion from happening by detecting and acting on them. 

Firewall: A system that filters network traffic based on rules to allow or block access between devices

Firewall types:

1. Packet-filter firewall: filters traffic based on IP,port,protocol and works at layers 3 and 4 (Network and Transport)

2. Stateless firewall: filters each packet independently based on rules such as source IP, destination IP, port, and protocol. Doesn't track connection state or session information. Faster and uses fewer resources than a stateful firewall, but provides less security.

3. Stateful firewall: tracks active connections(state). Allows only packets that belong to a valid session

4. NGFW: combines stateful firewall+deep inspection. Understands application can include IPS,Malware detection and user-based rules

5. WAF: protect web applications only works on HTTP/HTTPS level and block attacks like SQL injection,XSS, malcious HTTP requests

proxy: intermediary filter. 

1. Forward proxy: proxy between client and internet that forwards client request can hide the client

2.Reverse proxy: proxy in front of servers that handles incoming traffic and hides backend servers

3.Transparent proxy: proxy that intercepts traffic without the user knowing or configuring it

4. anonymous proxy: proxy that hides the user's IP address from webistes.

5. High-anonymity (elite)proxy: proxy that hides both the user's IP and the fact that a proxy is being used

##Security operations

SIEM: log correlation

SOAR: automated response

EDR/Endpoint detection and Response

XDR/Extended detection and Response: correlates data across endpoints,networks,cloud,email,etc.

DLP/Data loss prevention

CASB/Cloud security broker

NAC/Network access control

SCAP/Security Content Automation Protocol

## Risk&Governance

RTO/recovery time objective: maximum acceptable time a system or service can be down after an outage before it must be restored

RPO/Recovery point objective: amount of data you can lose before you can't restore it

ALE/annual loss expectancy: expected yearly financial loss from a risk

SLE/ Single loss expectancy: loss from one security incident

ARO/ annual rate of occurence: how often a risk happens per year

ALE=(AVE X EF) X ARO

where:

- AV=Asset Value
- EF= Exposure Factor
- SLE= AV * EF
- ALE= SLE * ARO


GDPR/General Data Protection Regulation: EU privacy

HIPAA/Health Insurance Portability and Accountability act: healthcare privacy

PCI DSS: payment security

SLA/Service level agreement: Defines agreed service levels such as uptime, response time, and support expectations

MOU/Memorandum of understanding: documents intent and responsibilities between parties

NDA/Non Disclosure Agreement: has to do with the confidentiality of information

## Attacks

Phishing: credential theft

MITM/Man in the middle attack: intercepts and potentially modifies communciations between two parties.

DOS/Denial of service: overloads a system to make it unavailable

DDOS/Distributed Denail of Service: DoS attack launched from many devices at once

SQLi: Injecting malicious SQL to access or modify database data.

XSS/cross site scripting: Injects malicious scrips that execute in victims browsers

CSRF/Cross-site request forgery:  tricks a logged-in user into performing unwanted actions on a website

RAT/Remote access trojan: malware that gives attacker remote control of a system 

## Network/Security tools

Honeypot: fake system designed to attract attackers

Honeynet: network of honeypots used for monitoring attackers

Load balancer: distributes traffic across multiple servers

Bastion host: hardened system exposed to external network for secure access

jump server: controlled server used to access internal systems securely

## Malware types

worm: self-replicating and spreads without user interaction

rootkit: hides malicious activity and maintains deep system access

spyware: secretly collects user data

keylogger: records keystrokes

logic bomb: triggers malicious action when a condition is met

## Attack types

Zero-day exploit: attack using unknown/unpatched vulnerability

Privilege escalation: gaining higher access rights than allowed

DNS poisoning: redirecting traffic by corrupting DNS results

ARP spoofing: redirecting local network traffic by fake MAC-IP mapping

Password spraying: trying common passwords across many accounts

## Cloud Security

IaaS: infrastructure provided (VMs, storage, networks). Customer responsibility OS,applications,data

PaaS: platform for developers to deploy apps. Customer responsibility applications,data.

SaaS: full application delivered over internet. Mostly data and user access.

Shared Responsibility Model:

Cloud provider secures infrastructure
Customer secures data + configuration

Cloud deployment models:

Public cloud: shared infrastructure

Private cloud: dedicated environment

Hybrid cloud: mix of both

## Incident response
1. Preparation
2. Detection/Identifaction
3. Containment
4. Eradication
5. Recovery
6. Lessons Learned

## Physical Security

CCTV: video monitoring system

Badge access: identity card-based entry control

Mantraps: controlled entry rooms preventing tailgating

Tailgating: unauthorized person follows an authorized person into a secured area

Piggybacking: Similar to tailgating, but the authorized person knowingly allows access.

Biometrics: Fingerprint, iris scan, facial recognition.

Motion Detection: Sensors that detect movement in restricted areas.

Security Lighting: Improves surveillance and deters intruders.

Faraday Cage: Blocks electromagnetic signals to prevent wireless interception.

Visitor Logs: Records visitor access for accountability.
Guards: human phyiscal security enforcement 

Locks: phyisical access control mechanism
