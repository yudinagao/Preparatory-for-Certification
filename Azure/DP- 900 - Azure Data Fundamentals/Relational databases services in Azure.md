# Relational databases services in Azure

## SQL Server on Azure VM
 - VM in Azure with SQL Server
 - IaaS
 - Great option for lift-and-shift
 - Create Rapid Development and test scenarios
 - Scale Up/Down

 ## Azure SQL Managed Instance
 - PaaS
 - provides near 100% compatibility with on-premises SQL Server Instances
 - Automated management, backups and other maintenance tasks
 - If your systema uses features like linked servers, Service Broker or Database Mail
 - Supports Azure Active Directory

 ## Azure SQL Database
 - Fully Managed, highly scalable PaaS database service
 - PaaS
 - Single Database:
 - Elastic Pools - Share same resources
 
 ## Azure SQL Edge
 - Optimized for IoT

# Comparison between Services
|  |	SQL Server on Azure VMs 	|Azure SQL Managed Instance 	|Azure SQL Database|
|--| ----                          |           -----               | -----            |
|Type of cloud service 	|IaaS 	|PaaS 	|PaaS
|SQL Server compatibility 	|Fully compatible with on-premises physical and virtualized installations. Applications and databases can easily be "lift and shift" migrated without change. 	|Near-100% compatibility with SQL Server. Most on-premises databases can be migrated with minimal code changes by using the Azure Database Migration service 	|Supports most core database-level capabilities of SQL Server. Some features depended on by an on-premises application may not be available.|
|Architecture 	|SQL Server instances are installed in a virtual machine. Each instance can support multiple databases. 	|Each managed instance can support multiple databases. Additionally, instance pools can be used to share resources efficiently across smaller instances. 	|You can provision a single database in a dedicated, managed (logical) server; or you can use an elastic pool to share resources across multiple databases and take advantage of on-demand scalability.|
|Availability 	|99.99% 	|99.99% 	|99.995%|
|Management 	|You must manage all aspects of the server, including operating system and SQL Server updates, configuration, backups, and other maintenance tasks. 	|Fully automated updates, backups, and recovery. 	|Fully automated updates, backups, and recovery.|
|Use cases 	|Use this option when you need to migrate or extend an on-premises SQL Server solution and retain full control over all aspects of server and database configuration. 	|Use this option for most cloud migration scenarios, particularly when you need minimal changes to existing applications. 	|Use this option for new cloud solutions, or to migrate applications that have minimal instance-level dependencies.|
 