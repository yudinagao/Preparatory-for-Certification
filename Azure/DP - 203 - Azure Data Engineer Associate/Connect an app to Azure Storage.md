# Connect an app to Azure Storage

## Azure Storage Services
- Managed
    - MS handles maintenance and any critical problems for you
- Durable
    - Redundancy
    - Replication
- Secure
    - encryption
- Scalable

Data Types
- Blobs
    - Block blobs
        - text or binary up to 5TB
        - 50.000 blocks of 100 MB
        - read
        - larger than 100 MB must be updated as small blocks
        - these block consolidated or commited into the final blob.
    - Page Blobs
        - random access files up to 8TB
        - backing for the VHD for the VMs
        - provides random read/write access to 512 bytes pages
    - Append blobs
        - like block optimized for append
        - used for logging information
        - up to 195 GB
- Files
    - Highly available network file share
    - accessed using the server message block (SMB) protocol
    - multiples VMs can reand and write files
    - read using the REST interface or the storage client libraries
    - associate a unique URL to any file
- Queues
    - store and retrieve messages
    - mesasges up to 64KB
    - miliion of messages
    - can be processed asynchronously
    - can be used to loosely connect different parts of application together
- Table Storage

## Interact with the Azure Storage API

Use the REST API
- accessible using HTTP/HTTPS
- needs manual parsing
- requires creation of HTTP packets to work with each API
    - Use a Client Library
        - various languages (python, C#, JAva)

## Connect to your Azure Storage Account

- Security Access keys
    - two unique access keys
    - need a pair of keys to each storage account

- REST API endpoint
    - Blobs - https://[name].blob.core.windows.net/
    - Queues - https://[name].queue.core.windows.net
    - Table - https://[name].table.core.windows.net
    - Files - https://[name].file.core.windows.net
    - You can use a custom domain URL for the endpoint, if already have ir tied to Azure

- Simplest way
    - storage account connection string

- Security
    - allow keys to be rotated
        - can be done from azure ortal and Azure CLI/PowerShell
    - rotating a key invalidates the original key and revokes access to anyone 
        - update the connection string to reference the secondary access key
        - regenerate the primary key
        - update the connection string to the new primary key
        - regenerate the secondary key
    - SAS - Shared access signatures
        - support expiration
        - limited permission