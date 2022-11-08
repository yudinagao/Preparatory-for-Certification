# Network Architeture based on workload requirements

## Requirements

Naming - Unique within the scope
Regions 
    - lowest latency
    - data residency, sovereignty, compliance and resiliency
Subscription
    - Segmentation
        - Virtual Networks
            - Isolating traffic
            - limit of network interfaces
            - Public and private address
        - Subnets
            - Unique address range
            - limit access to resources
            - network security group
Security
    - Traffic Filtering
        - Network security group
        - Security rules
    - Traffic Routing
        - Traffic between subnets to flow through an NVA
        - Forcing internet traffic for inspection and logging - Force Tunneling

## Best Practice - 

Plan IP Addressing
    - Virtual network address shouldn't overlap with on-premises
Implement a hub and spoke network topology
    - isolates workloads while sharing services
    - HUb is an Azure Virtual Network that acts as a central point of connectivity
    - Spoke are virtual networks that connects to hub by using peering
Design Subnets
    - Multiple subnets whithin each virtual network
    - Default traffic between all subnets

## On-premises connectivity to Azure Virtual Network

### VPN connection

VPN gateway - encrypted traffic between as Azure Virtual Network and and on-premises.
- Traffic is likely to be light or trade slightly latency for flexibility and processing power of the cloud
- SImple to configure
- Higher badnwidth up to 10 Gbps
- Requires an on-premises VPN device

### ExpressRoute connection

Uses private, dedicated connection through a third-party connectivty provider.
Suitable for hybrid applications running large-scale, mission critical workloads high degrre scalability
- Higher badnwidth up to 10 Gbps
- Support Dynamic scaling of bandwidth
- may allow direct access to national cloud
- May be complex to set up
- requires high bandwidth router on premises

### ExpressRoute with VPN failover

Combines the previous two
Need of higher bandwidth than ExpressRoute and highly available network connectivity
- High availability if ExpressRoute Fails
- Complex to configure
- Require redundant hardware VPN appliances and redundant Azure VPN Gateway

### Hub-spoke network topology

- Customer managed or Microsoft managed
- Use of WAN to replace hubs as managed service
    - optimized and automated branch connectivity
- Less operational overhead
- Cost Saving
- Improved Security
- Separation of Concerns
- Central control and access to shared devices

## Azure Network connectivity services

- 