# Security Capabilities in Azure

## Distributed Denial of Service

- Volumetric attack - vaolume-based attacks that flood the network overwhelming the available bandwidth. Legitimate traffic can't get through. bits per second
- Protocol Attacks - render a target inaccessible by exhausting server resources with false protocol request that exploit weakness in layer 3 (network) and layer 4 (transport) protocols - packets per second
- Resource (application) layer attacks - though web application packets - disrupt transmission data between hosts


## Azure DDoS Protection

Help protect your applications and servers by analyzing network traffic and discard anything that looks like DDoS attack.
- Default - enables every property in Azure, always on traffic monitoring and real time mitigation of commom network attacks - global net
- Protection Standard - enhanced DDoS mitigation, Protection is simple to enable on any new or existing VN - inclued logging, alerting and telemetry

## Azure Firewall

Cloud-based network security service that protecs your Azure VN
- Built-in High availability and availability zones
- network and application level filtering
- Oubound snat and inbound Dnat - translate the private IP
- multiple public ip addresses
- Threat intelligence
- Integration with Azure Monitor

## Web Application Firewall

Provides centralized protection, security management simple, improves response time to a security threat and aloows patching a know vulnerability in one place. Gives application admin better assurance of protection

## Network Segmentation in Azure

Ability to group related assets that are a part of workload operations, Isolation of resources
Governance policies
Secure interactions between perimeters

## Azure Network security Groups

Filter network traffic to and from azure resources in a Azure VNet. A NSG define how the traffic is filtered

### Inbound and Outbound security Rules

- Rule Properties:
    - Name
    - Priority
    - Source or destination
    - Protocol
    - Direction
    - Port Range
    - Action

- AllowVNetInBound
    - Lowest Priority - processed first
    - from any VNet on any port to any VNet any protocol
- AllowAzureLoadBalancerInBOund
    - From any Azure Load Balancer to any port to any IP adress any protocol
- DenyAllInBound - deny al trafiic

### Difference between Azure Firewall and NSG
Firewall complements NSG 
Firewall across and centralized network
NSG within VNet

## Azure Bastion and JIT Access

Azure Bastion lets you connect to a VM using yu=our browser and the Azure portal.
- PaaS
- Provides secure and seamless RDP and SSH connectivy to your VM from the Azure Portal, using Transport Layer Security (TLS)
- VM don't need a public IP address, agent or special client software
- Don't need to manage a NSG
- Protection against port scanning

Just-in-Time Access
- allows lock down of the inbound traffic to your VMs
- select which port to be blocked
- JIT requires Microsoft Defender for Servers to be enabled on the subscription

## Azure encrypts data

- Azure Storage Service
    - protects data at rest by automatically encrypting before persisting it to Azure managed disks.
- Azure Disk Encryption
    - encrypts windows and Linux IaaS VM disks
    - usues industry-standard BitLocker feature of windows and the dm-crypt feature of linux
- Transparent Data encryption (TDE)
    - protects Azure SQL Database and Azure Data Warehouse
    - real time encryption and decryption of the database, associated backups and transaction logs files at rest

## Azure Key Vault

- Secrets Managements
    - tighly control access to tokens, passwords, certificates, API keys and other secrets
- Key Management
- Certificate Management
- Store secrets backed by hardware security modules (HSMs)
    - protected by software or by FIPS 140-2 level 2 validated HSMs