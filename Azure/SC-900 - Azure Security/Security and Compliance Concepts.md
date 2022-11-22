# Security and Compliance Concepts

## Shared Resposibility Model

IaaS:Shared
Paas: Application and Data
SaaS: Customer

- Customer:
    - Information and Data
    - Devices (mobiles and PCs)
    - Accounts and Identities
- Provider:
    - Physical hosts, network, datacenter
- Shared:
    - Operations Systems,
    - Network Controls
    - Applications
    - Identity and Directory Infrastructure

## Defense in Detpth:

### Layer of defense;

    1 - Physical: Limiting access to datacenters
    2 - Identity and access: Multifactor Authentication, or condidtion based 
    3 - Perimeter: Distributed Denial of Service (DDoS)
    4- Network: segmentation and network acess control, limiting communication between services
    5 - Compute: securing access to VM - closing ports
    6 - Application: ensure applications are secure and free of vulnerabilities
    7 - Data: Controls to manage access to business and customer data - encryption

### CIA - Confidentiality, Integrity and Availability

- Confidentiality: keeps confidential sensitive data - encryption
- Integrity: Keeping data or messages correct - confidence that data hasn't been tampered with or altered
- Availability: Data available for those who need, when they need it

## Zero Trust model

- Assumes evertything is opoen and unstrusted network, even resources behind firewalls
- Verify explicity
- Least privileged access
- assume Breach

### Foundational Pillars:
- Identities
- Devices
- Applications
- Data
- Infrasctruture
- Network

## Encryption and Hashing

### Symmetric Encryption
One key to encrypt and decrypt the data
### Asymmetric:
Public key and Private key

Encryption at rest
Encryption in transit
Encryption for data in use

### Hashing

Algorithm convert text to unique fixed-lenght value called hash

## Compliance Concepts

### Data Residency
    - Govern the physical location where data can be stored and how and when it can be transferred, processed or accessed 

### Data Sovereignty
    - Personal data, is subject to Laws and regulations of country

### Data Privacy
    - Providing notice and being tranparent about collection, processing, use and sharing of personal data
