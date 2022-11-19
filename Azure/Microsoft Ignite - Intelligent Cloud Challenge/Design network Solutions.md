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

- Communication of Azure Resources
- Communictaion between VN
- Communication to the internet
- Communication with on-premises networks

Do any organizational security requirements exist for isolating traffic into separate virtual networks? 
Do any organizational requirements exist for isolating virtual networks into separate subscriptions or regions?
How many network interfaces and private IP addresses do you require in a virtual network?

### Network Segmentation

- Subscription - high level construct - Communictaion between in different subscription needs to be explicity provissioned
- Virtual Networks - Communictaion between in different VN needs to be explicity provissioned
- Network Security Groups - access control mechanics for controlling traffic between resources within a VN. Also control external Networks - granular level by creating a perimeter for a subnet
- Application Secrity Groups - Groups a set of VMs under an applicatiaon tag
- Azure Firewall - native filter traffic between cloud resourcers, internet and on premises

#### Pattern 1 - Single Virtual Network

Subnet1 - database workloads
Subnet2 - web workloads. 
NSGs - Subnet1 talk only Subnet2
     - Subnet2 -> Internet

Although we used NSGs to illustrate how subnet traffic can be governed, you can also enforce this segmentation by using a Network Virtualized Appliance from Azure Marketplace or Azure Firewall.

#### Pattern 2 - Multiple virtual networks with peering in between them

 Group applications - separate virtual networks or in multiple Azure regions. 
 explicitly peer a virtual network

 #### Pattern 3: Multiple virtual networks in a hub & spoke model

 Choose a VN as a hub within a region - communication achieved by peering
 Traffic passes through the HUB - it serves as a gateway
 Scalability

 ### Virtual network NAT gateway

Virtual Network NAT (network address translation) simplifies outbound-only Internet connectivity for virtual networks 
- You need on-demand outbound to internet connectivity without pre-allocation
- You need one or more static public IP addresses for scale
- You need configurable idle timeout
- You need TCP reset for unrecognized connections

### Routing

 - System routes
 - Subnet default routes
 - Routes from other virtual networks
 - BGP routes
 - Service endpoint routes
 - User Defined Routes (UDR)

## Design for application delivery services

### Content Delivery Network - CDN

- Point of presence close to large clusters of users
- Reduce latency
- Custom domains, file compression, caching and geo-filtering

### Azure Front Door

- Define, Manage and monitor global routing - web traffic 
- Optimize for best performance and instant global failover for high availability
- requests are send to the lowest latency back ends
- you have primary and secondary backends
- Distribute traffic using weight coefficients
- Ensure request from a user get sent to the same back end (affinity)
- HTTPS based and you need WAF and or CDN

### Traffic Manageer

DNS -based traffic load balancer
Distribute traffic aoptimizing - high availability and response time
    - priority
    - weighted
    - performance
    - geographic
    - multi-value
    - subnet

- need of increase application availability
- need of improve application performance
- need to combine hybrid applications
- need to dirtibute traffic for complex deployments

### Load Balancer

- High Performance 
- Low Latency layer 4 load-balancing for all UDP and TCP protocols
- Manages inbound and outbound connections
- Define rules to map inbound connections to back end pool
- 