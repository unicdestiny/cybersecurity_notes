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

ECC/Elliptic curve crypto: done by putting two random points on a curve to use for the encryption.

SHA-256:it produces a 256-bit hash value

HMAC: does integrity checking and authentication

Diffie-hellman: algorithme used for key exchange

PKI/Public Key Infrastructure: infrastructure for generating and validating keys

CA/Certificate authority: signs the certificate to make sure it's valid

CSR/certificate request: ask for the information abouth the certificate.

CRL/Certificate Revocation List: check if the certificate is valid on this time.

OCSP: automatic protocol that checks if the certificate is valid.

TPM: hardware security module chip.

HSM: key storage hardware

FDE/full disk encryption: allows you to encrypt you disk so it's not readable when stolen.

SED/Self-encrypting drive

EFS/File encryption: used by windows to encrypt files

##Network Security:

TLS/Transport layer security: does encrypted communication by SSL

SSH: secure remote login running on port 22

VPN: private network tunnel over public internet

IPsec: encrypts network traffic inside an IP message

ESP/Encapsulating security payload:provides encryption+integrity+authenticatoin

AH/Authentication header: integrity+authentication

IDS/Intrusion detection system: detects intrusions that happen on the network

IPS/Intrustion prevention system: prevents intrustion from happening by detecting and acting on them. 

Firewall: A system that filters network traffic based on rules to allow or block access between devices

Firewall types:

1. Packet-filter firewall: filters traffic based on IP,port,protocol and works at network layer

2. Stateful firewall: tracks active connections(state). Allows only packets that belong to a valid section

3. NGFW: combines statefull firewall+deep inspection. Understands application can include IPS,Malware detection and user-based rules

4. WAF: protect web applications only works on HTTP/HTTPS level and block attacks like SQL injection,XSS, malcious HTTP requests

proxy: intermediary filter. 

1. Forward proxy: proxy between client and internet that forwards client request can hide the client

2.Reverse proxy: proxy in front of servers that handles incoming traffic and hides backend servers

3.Transparent proxy: proxy that intercepts traffic without the user knowing or configuring it

4. anonymous proxy: proxy that hides the user's IP address from webistes.

5. High-anonymity (elite)proxy: proxy that hides both the user's IP and the fact that a proxy is being used

##Security operations

SIEM: log correlation

SOAR: automated response

EDR/Endpoint detection

XDR/Extended detection

DLP/Data loss prevention

CASB/Cloud security broker

NAC/Network access control

SCAP/compliance automation

## Risk&Governance

RTO/recovery time objective: maximum acceptable time a system or service can be down after an outage before it must be restored

RPO/Recovery point objective: amount of data you can lose before you can't restore it

ALE/annual loss expectancy: expected yearly financial loss from a risk

SLE/ Single loss expectancy: loss from one security incident

ARO/ annual rate of occurence: how often a risk happens per year

EF: exposure factor

AV: Asset value

ALE= (AV*EF) *ARO

GDPR/General Data Protection Regulation: EU privacy

HIPAA/Health Insurance Portability and Accountability act: healthcare privacy

PCI DSS: payment security

SLA/Service level agreement: an agreement made on level of support a company provides for it's hardware.

MOU: agreement

NDA/Non Disclosure Agreement: has to do with the confidentiality of information

## Attacks

Phishing: credential theft

MITM/Man in the middle attack: interception of traffic between user and internet

DOS/Denial of service: overloads a system to make it unavailable

DDOS/Distributed Denail of Service: DoS attack launched from many devices at once

SQLi: Injecting malicious SQL to access or modify database data.

XSS/cross site scripting: injecting malicious scripts into websites to attack users browser

CSRF/Cross-site request forgery:  tricks a logged-in user into performing unwanted actions on a website

RAT/Remote access trojan: malware that gives attacker remote control of a system 

## Network/Security tools

Honeypot: fake system designed to attract attackers

Honeynet: network of honeypots used for monitoring attackers

Load balancer: distributes traffic across multiple servers

Bastion host: hardened system exposed to external network for secure access

jump server: controlled server used to access internal systems securely

## Malware types

worm: self-replicating malware that spread without user action

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

IaaS: infrastructure provided (VMs, storage, networks)

PaaS: platform for developers to deploy apps

SaaS: full application delivered over internet

Shared Responsibility Model:

Cloud provider secures infrastructure
Customer secures data + configuration

Cloud deployment models:

Public cloud: shared infrastructure

Private cloud: dedicated environment

Hybrid cloud: mix of both

## Incident response
1. Preparation
2. Detection
3. Containment
4. Eradication
5. Recovery
6. Lessons Learned

## Physical Security

CCTV: video monitoring system

Badge access: identity card-based entry control

Mantraps: controlled entry rooms preventing tailgating

Guards: human phyiscal security enforcement 

Locks: phyisical access control mechanism
