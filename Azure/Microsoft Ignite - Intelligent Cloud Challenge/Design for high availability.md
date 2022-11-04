# Design for high availability

- Resilient to component Failure
- No Significant downtime

## Cost x Complexity
### Targe SLA - 
    - Automation - Self Healing and Self Diagnosing
    - Mean time between Failures x Mean time to Recover
    - Agreement from customers

### Identify Dependencies
    - Availability requirements
    - Downtime acceptable
    - Potential downtime cost youur business
    - How much should you invest
    - Backup requirements
    - Replication Requirements
    - Monitoring Requirements
    - Specific latency requirements

### Identify critical system flows

- Over or underutilized 
- Adjust to better needs and cost goals
- Certain paths have high expectations
- Identify Less critical componentes
    - Cost redcution

# Azure Front Door

- Content Delivery Network
    - fast, reliable, secure
    - optimizes access times to content
    - load balacing
    - site acceleration

- Primary and Secondary regions
    - Front Door - requires to primary region if fails secondary
    - Geo-Replication

# Azure Traffic Manager

- DNS-base traffic load balancer
- Public endpoints - high availability and quick responsiveness
- Distribute trafiic optimally to services acrros the globe
- Only at Domain level

    - User Petitions DNS server
    - DNS server queries Traffic Manager for required record
    - Result returns to Traffic Managaer
    - Client connects do endpoint

# Recommend a high availability solution for compute

- Azure Availability Zones
- Highly available container solution
    - Azure Kubernets Service (AKS)
        - Managed Kubernets Cluster
- Consider multiple region availability
- Azure Storage replication options
    - infrastructre based asynchronous replication
    - Application based asynchronous replication

# Recommend a high availability solution for relational Data Storage

- General purpose
    - Application and Control Ring
    - Remote Storage
- Business Critical
    - SSD
- Hyoerscale
    - databases pages without having to access the data file directly
    - paired pages servers
    - 100 TB
    - CAn have 0 to 4 replicas to read

- Databases service tiers for availability
    - Availability Zones
    - Azure SQL SLA
    - Geo-replication

# Recommend a high availability solution for non-relational Data Storage

## Azure storage redundancy

- Data replication in the primary region
- Data is replicated in secondary region that's geographically distant
- Apps require read to replicated data if primary is down

## Locally Redundant Storage (LRS)

- Copies Synchronous three times within physical location in the primary region
- least expensive
- not recommended for high availability and durability
- server rack and drive failures
- if data is easily reconstructed
- application restricts replication data within same country or region

## Zone-Redundant Storage (ZRS)

- Copies Synchronous three Azure availability zones
- High availability primary and replication secondary
- Geo-redudant Storage and  Geo-Zone-Redudant Storage

## Data Lake Storage Redundancy

- high level of IOPS

