# Design a data storage solution for relational data

## Azure SQL Database

- Paas
- High Scalable - up to 100 TB
- Pricing
- Serverless option
- Elastics Databases Pools - All databases share the same compute and storage resources

## Azure SQL Managed Instance

- Lift-and-Shift migration
- SQL Server Agent
- Common Language Runtime
- Database Mail
- Distributed Transactions
- ML Services
- Define Maximum CPU Cores and Storage

## SQL Server on Azure Virtual Machines

To Consider:
- Server Access 
- Automated Management
- Azure Hybrid Benefit

| Compare 	| SQL Database 	| SQL Managed Instance 	| SQL Server on Azure Virtual Machines |
| ---- 	| ---- 	| ----	| ---- |
| Scenarios 	| Best for modern cloud applications, hyperscale or serverless configurations 	| Best for most lift-and-shift migrations to the cloud, instance-scoped features 	| Best for fast migrations, and applications that require OS-level access|
| Features | Single database
- Hyperscale storage (for databases up to 100 TB)
- Serverless compute
- Fully managed service

Elastic pool
- Resource sharing between multiple databases for price optimization
- Simplified performance management for multiple databases
- Fully managed service |

Single instance
- SQL Server surface area (vast majority)
- Native virtual networks
- Fully managed service

Instance pool
- Pre-provision compute resources for migration
- Cost-efficient migration
- Host smaller instances (2vCore)
- Fully managed service |
Azure Virtual Machines
- SQL Server access
- OS-level server access
- Expansive version support for SQL Server
- Expansive OS version support
- File stream, Microsoft Distributed Transaction Coordinator (DTC), and Simple Recovery model
- SQL Server Integration Services (SSIS), SQL Server Reporting Services (SSRS), and SQL Server Analysis Services (SSAS)| 

# Recommend a solution for database Scalability

## Dynamic Scalability

- Choose DTUs or vCore - define maximm amount of resources
- Elastic databases pools
- Implement vertical or horizontal scaling
- Apply horizontal scaling by using sharding to partition data

# Recommend a solution for database availability

- general Purpose
- Business Critical
- HyperScale

# Design security for data at rest, data in motion, and data in use

|Data state 	|Encryption method 	|Encryption level|
|----------     |-----              |-----           |
|Data at rest 	|Transparent data encryption (TDE) 	|Always encrypted|
|Data in motion |Secure Socket Layers and Transport Layer Security (SSL/TLS) 	|Always encrypted|
|Data in process|Dynamic data masking 	|Specific data is unencrypted, Remaining data is encrypted|

# Design for Azure SQL Edge

- Containereized Linux Application
- IoT
Consider:
- Network connectivity
- Slow or intermittent broadband connection
- Data Security and privacy concerns
- Synchronization and connectivity to back end systems
- Code and skill familiarity

# Design for Azure Cosmos DB and Table Storage

## Azure Cosmos DB

- Fast response time at any scale
Consider
- Latency
- Throughput
- Global Distribuition
- Indexing
- Query
- Consistency
- Pricing
- SLA