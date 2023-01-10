# Peta-byte scale ingestion with Azure Data Factory

Ingestion using copy activity
- code-free data ingestion
- 100 native connectors
- simple to create
- not able to deal with sophisticated transformations or business logic

Ingestion using compute resources
- Spark pools - Azure synapse Analytics
- complex calculations
- generate new data for further pipeline

Ingestion using SSIS packages
- lift and shift existing SSIS workload
- deploy and manage exiting SSIS packages

## DF Connectors

File formats
- AVRO
- Binary
- Delimited text format
- JSON
- ORC
- Parquet

## Data Ingestion Security Considerations

Networks

- Virtual Networks secure communication between Azure services or with servers 
- configure a Network Security Groups (NSG) to restrict  access
- using Azure SSIS IR 
    - gives option to join a virtual network
    - azure creates network resources, like NSG automatically created by ADF

- Use services to detect and prevent intrusions
    - can deny communication with know IP adress by enabling DDoS protection
    - Azure Security center Integrated Threat Intelligence
        - deny with known malicious or unused Internet Ip Adress
    - Azure Firewall can be used to control network access
    - payload inspection is required
        - you can redirect traffic to a firewall appliance via Azure Express Route force tunneling

- SImplify management of security rules using network service tags
    - groups together ip adresses prefixes from a given Azure service
    - using tags, create rules in NSG

Identity and access control

- Adminstrative accounts
    - should be dedicated
    - monitored and managed on a regular basis to ensure not compromised
    - higher security environments
        - dedicated machines for administrative access

- Active Diretory to matk use of SSO
    - register service principals wihtin Azure AD
        - token management

Data Protection

- Use RBAC to control access to the resources
    - Sensitive data
        - maintaining a list of the data stores that contain sensitive information
        - isolate systems that store and process
        - monitor and block unauthorized transfer
        - encrypt any sensitive information that goes in transit
        - encrypt any sensitive information in rest

Logging and monitoring

- Configure central security log management
    - Azure Monitor
        - centralize ths storage of ingestion logs
        - query them using logic analytics
        - set up strategy to store the logs long term

- Monitor and log the configuration and network packet traffic of VN, subnets and NICS
    - enbale NSG flow logs
    - send logs into an Azure Storage account for traffic auditing
    - send logs to Log Analytics workspace and use traffic analytics to provide insights

- Enable audit logging
    - configure diagnostic logs to track
    - retained for 45 days
    - save the diagnostic logs

- Enable alerts on activities
- Follow standard logging and monitoring standard within organization
    - audit logging
    - security logs
    - anti-malware logging
    - log retetion policies
    