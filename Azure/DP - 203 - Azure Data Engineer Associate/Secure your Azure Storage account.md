# Secure your Azure Storage account

Azure Storage Security features

- Protection at rest
    - Encryption using Storage Service Encryption (SSE)
        - 256-bit Advanced Encryption Standard (AES)
        - FIPS 140-2 Compliant
        - no additional charges, doesn't degrade performance and not disabled
    - For VM, Azure disk Encryption
        - BitLocker fow windows images, and uses dm-crypt dor Linux
    - Azure key Vault stores keys automatically
- Protection in transit
    - Transport-level security netween Azure and client
    - HTTPS - can be enforced
- Support browser cross-domain access
    - Crossm Origin resource sharing (CORS)
        - uses HTTP headers 
        - CORS support is optional flag 
- Control who can access data
    - Role Based access control
- Audit storage access
    - Storage Analytics service
    - logs operation in real time
    - search for specific requests
    - filter based on authentication mechanism, success of operation or resource accesssed
    
## Storage Account Keys

Azure Storage account can create authorized apps in Active Directory to control access to the data in blobs and queues. Can be used shared keys, it support blobs, queues, tables and files

- the client embeds the shared key in the HTTP Authorization Header of every request
- storage account validates the key
- shared keys = storage account keys
- regenerate keys periodically

Types of shared access signatures
- service level SAS
    - allows specific resources
    - retrieve a list of files or download a file
- account leve SAS
    - allow access to anything that a service level sas
    - additional resources and abilities
    - allow the ability to create file systems

Accounts that store user data two typical designs
- Clients uploads and downloads through a front-end proxy, which performs authentication
    - front end proxy service advantage of allowing validation of business rules
    - downside: if large volume of data or high-volume transactions- complicated or expensive to scale
- A lightweight service authenticates the client, as needed
    - next it generates a SAS
    - after receiving, the client can access storage account directly
    - SAs defines client permission and access interval
    - it reduces the need to route all data through a front-end proxy

## Control Network access to your storage account

- default
     - accept connections from client in any network

- go to storage account you want to secure
- select networking
- enabled from selected virtual network and ip adress
- can be enable from all networks

## Advanced Threat Protection for Azure Storage
- layer of protection allows you to adress threats without being a expert
- security alerts are triggered when anomalies in activity occur
    - integrated with MS Defender for Cloud
        - sent email for subscription admin with details and recommendantion
        - general purpose v2, block blob and blob storage
- Microsoft Defender for Storage
    - Blob storage, azure files and azure data lake storage gen2
    - all public clouds and us government clouds
    - azure portal
        - security + networking 
        - microsoft defender for cloud
        - enable
    
Anomalies
- Nature of anomaly
- storage account name
- event time
- storage type
- potential causes
- investigations teps
- remediation steps
- includes details possible causes and recommendations


## Azure Data lake Storage Security features
- RBAC
- Access control list (ACL) - POSIX compliant
    - only authorized users, groups ps service principals
- authentication through Azure Active Directory OAuth 2.0 bearer tokens
    - Federation with Azure AD Connect
    - MFA 
    - integrated with analytics services that use data
        - databricks, HDInsight, Azure Synapse analytics
        - and management tools like Azure Storage Explorer
    - authentication finishes
        - permissionsare applied at finest granularity
        - right level of authorization
- Encryption end-to-end
- Transport layer protections
