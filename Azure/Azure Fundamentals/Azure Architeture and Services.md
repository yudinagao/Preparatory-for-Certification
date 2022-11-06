# Azure Architeture and Services

## Azure Account

Azure Account -> Subscriptions -> Resources Groups -> Resources

## Azure Physical Architeture

- Regions 
    - geographical area
    - Regions Pairs
    - Sovereign Regions
- Availability Zones - phisically separate within an Azure Region

## Azure Management Architeture

### Azure Resources and Resources Groups

- Resource - VMs, VN, Databases
- Resource Groups

### Azure Subscription 

- Unit of management, billing and scale
- Organize resources
- Billing Boundary
- Access Control Boundary
- Environment
- Organizational structure
- Azure Management Group
    - Create a hierarchy that applies a policy
    - Providdes User Access to multiple subscriptions

## Azure Identity, Access and Security

### Azure Identity

- Azure Active Directory Services
    - Authentication
    - Single sign-on
    - Application management
    - Device Management
- Azure Active Directory Domain Services
    - Domain
    - group Policy
    - lightweight directory access protocol (LDAP)
    - Kerberos/ NTLM authentication
    - Defines a unique Namespace

### Azure Authentication Methods

- Single Sign On
- Multi Factor Authentication
- Passwordless Authentication
    - Microsoft Hello for Business
    - Microsoft Authenticator App
    - FIDO2 security keys

#### Azure External Identities

- B2B Collaboration
- Azure AD B2C
- Azure Conditional Access

### Azure Role-based Access Control

- Management Group
- Single Subscription
- Resource Group
- Single Resource

### Zero Trust Model

- Assumes Worst Case Scenario
- Verify Explicity
- Use least Privilege Access
- Assume Breach
Instead of assuming that a device is safe because it’s within the corporate network, it requires everyone to authenticate. Then grants access based on authentication rather than location.

### Defense in Depth

- Physical layer
- Identity and Access
    - Control Access and change control
    - Single Sign on
    - Audit Events and Changes
- Perimeter
    - Use DDoS protection
    - Use Perimeter Firewalls
- Network
    - Limit Communication between resources
    - Deny by Default
    - Restrict inboud internet access and limit outbund access
- Compute
    - Secure Access to VM
    - Implement endpoint protection
- Application
    - Ensure applications are safe and free of vulnerabilities
    - Storage Sensitive application servies
    - Make security a design requeriment.
- Data
    - Database
    - Disk inside VM
    - Storage as PaaS   
    - Manage thoihjt    

## Microsoft Defender For Cloud

- 

