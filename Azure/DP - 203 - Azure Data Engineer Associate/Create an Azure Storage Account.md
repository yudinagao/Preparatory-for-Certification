# Create an Azure Account

## Decide how many storage accounts you need

- Storage 
    - Azure Blobs
    - Azure Files
    - Azure Queues
    - Azure Tables

- Storage account
    - groups a set of Azure storage services together
    - any change in the group apply to all services
    - storage account is an Azure resource and is a part of resource group
    - azure sql and azure cosmos db are independent azure resources and cannot be included in a storage account

- Storage account settings
    - Subscription
    - Location
    - Performance:
        - Standard
            - BLob, File, Queue, Table - Magnetic hard disks
        - Premium
            - more services than standard
                - store as block blob, append
                - create and store premium file share
                - SSD for storage
    - Replication
        - Stategy to make copies
        - at minimum - 3 copies within datacenter - locally redundant storage(LRS)
        - can upgrade t geo-redundant storage(GRS)
    - Access Tier
        - How quickly you are able to access your blobs
    - Secure transfer required
        - security feature that determines the supported protocols for access
        - enables HTTPS and disable HTTP
    - Virtual networks
        - security feature allows inbound access requests only from VN you specify
    
## How many storage accounts do you need

Storage account represents a collection of settings like replication, location and subscription owner
- data diversity
    - increased diversity means increased number of storage accounts
- cost sensitivity
    - by itself has no cost
    - settings influence the cost
        - geo redundant costs more than locally redudant
        - premium and hot tier increase cost of blobs
- tolerance for management overhead
    - typical strategy is to start with analysis of your data
    - create partitions that share the same characteristics 
        - location
        - billing
        - replication strategy
    - create one storage account for each partition

## Choose your account settigns

- Name
    - globally unique
    - only lowercase letters and digits
    - 3 to 24 char
- Deployment model
    - two deplyment models
        - Resource Manager 
            - current model that uses Azure Resource Manager API
        - Classic
            - legacy offering that uses the Azure Service Management API
    - difference between the two
        - Azure Manager adds the concepts of resource group 
        - not available in the classic model
- Account kind
    - Storage V@2
    - Storage V1
        - lower cost than v2
    - Blob Storage

## Account Creation tool

- Azure Portal
    - provides GUI with explanations
- Azure CLI
    - write scripts
- Azure PowerShell
    - write scripts
- management client libraries
    - incorporate the creation into a client app

## Step by step creation

- sign in
- select storage account
- on the command bar - create
    - subscriptiom
    - resource group
    - instance details
    - storage account name
    - Region
    - Performance
    - Redundancy
- Advanced settings
    - security
        - require secure transfer for REST API opertaions
            - controls if HTTP can be used
        - enable blob public access
        - enable storage account key access
        - Default to Azure Directory Authoriztion in the Azure Portal
        - Minimum TLS version
        - Permitted scope for copy operations
    - Data Lake Storage Gen2
        - Enable hierarchicalnamespace
            - only for big-data applications
    - Blob Storage
        - Enable SFTP
        - Enable network file system v3
        - Allow cross-tenant replication
        - Access tier
    - Azure Files
        - Enable large files share
- Networking
    - Network connectivity
        - Connectivity method
            - public internet access 
    - Network Routing
        - Routing preference
            - microsoft global network optimized for low-latency path selection
- Data Protection
    - Recovery
        - Enable point in time restore for containers
        - Enable soft delete for blobs
        - Enable soft delete for containers
    - Tracking
        - Enable versioning for blobs
        - Enable blob change feed
    - Access Control    
        - Enable version-level immutability support
- Encryption
- Tags
    - associate key value pair with the account for your categorization
- review + create to validate

