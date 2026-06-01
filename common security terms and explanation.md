## Identity & Access Control

MFA/Multi-factor authentication: uses two or more verification factors (e.g., password + SMS code or authentication app)

SSO/Single Sign-On: allows users to access multiple applications within a system using one set of credentials

RBAC/Role-Based access Control: access permissions are assigned based on user roles (e.g., managers can access management tools)

ABAC/Attribute-Based access Control: access is granted based on attributes such as location, device type, or IP address

DAC/Discretionary access control: owner of resource decides who gets access to it (e.g. read+ write+execute rights on files)

MAC/Mandatory access control: rights about files and resources are given by file system

LDAP/Lightweight Directory Access protocol:

  Definition: A protocol used to access and manage directory information (users,groups,permissions)
  
  How it works:
   
    1) Client connects to an LDAP server
    
    2) The clients performs a bind operation(authentication attempt)
    
    3) The server checks credentials against the directory database
    
    4) If valid, the client is authenticated
    
    5) The client can then query or modify direcotry entries
  
  Tree-based structure called DIT/Directory information tree:
    dc=company,dc=com
     
     ├── ou=users
     
     │    ├── cn=John Doe
     
     │    └── cn=Alice Smith
     
     ├── ou=groups
     
     └── ou=devices
  
  Key components:
    
    DN/Distinguished name: full path to an entry
    
    CN/common name: user or object name
    
    OU/Organization unit: groups like users,admins, devices
    
    DC/Domain component: domain structure
  
  Types of bind:
    
    simple bind: username+ password
    
    SASL bind more secure authentication framework
  
  Flow:
    1) client sends bind request
    2) server verifies credentials
    3) server returns success or failure
  
  Ports:
  
  | Protocol                          | Port | Description           |
  
  | --------------------------------- | ---- | --------------------- |
  
  | LDAP (unencrypted)                | 389  | Standard LDAP traffic |
  
  | LDAPS (LDAP over SSL/TLS)         | 636  | Encrypted secure LDAP |
  
  | Global Catalog (Active Directory) | 3268 | Search across domains |
  
  | Global Catalog (SSL)              | 3269 | Secure global catalog |

  LDAP vs LDAPS:
  
    LDAP: plain text communication(port 389)
    
    LDAPS: encrypted using TLS from the start(port 636)

Radius: authentication system
TACACS+: admin authentication
FIDO2: passwordless authentication
PIV/CAC: smart card authentication
