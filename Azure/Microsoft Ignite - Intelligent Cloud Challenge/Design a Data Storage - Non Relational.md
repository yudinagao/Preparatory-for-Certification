# Design a Data Storage - Non Relational

## Azure Storage Account

- Groups all storage Services
- Location
- Replication
- Subscription Owner
- Compliance Requirements
- Storage Costs
- Administrative OverHead
- Data Sensitivity
- Data Isolation


## Azure Blob Storage7

- Storage Availability
- Latency
- Cost requirements
- Immutability

## Azure Files

- Data Access Method
    - Direct Mount
    - with Azre File Sync
- Performance
    - Latency
    - IOPS
    - Bandwitdh
|Comparison 	|Azure Blob Storage 	|Azure Files 	|Azure NetApp Files|
|Description 	|Azure Blob Storage is best suited for large scale read-heavy sequential access workloads where data is ingested once and modified later. |Blob Storage offers the lowest total cost of ownership, if there's little or no maintenance. 	|Azure Files is a highly available service best suited for random access workloads. For NFS shares, Azure Files provides full POSIX file system support and can easily be used from container platforms like Azure Container Instance (ACI) and Azure Kubernetes Service (AKS) with the built-in CSI driver, in addition to VM-based platforms. 	Azure NetApp Files is a fully managed file service in the cloud, powered by NetApp, with advanced management capabilities.| NetApp Files is suited for workloads that require random access and provides broad protocol support and data protection capabilities.|
|Use cases 	|Large scale analytical data, Throughput sensitive high-performance computing, Backup and archive, Autonomous driving, Media rendering, or Genomic sequencing 	|Shared files, Databases, Home directories, Traditional applications, ERP, CMS, NAS migrations that don't require advanced management, Custom applications that require scale-out file storage 	|On-premises enterprise NAS migration that requires rich management capabilities, Latency sensitive workloads like SAP HANA, Latency-sensitive or IOPS intensive high performance compute, Workloads that require simultaneous multi-protocol access|
|Performance (per volume) 	|Up to 20,000 IOPS, Up to 100 GiB/s throughput 	|Up to 100,000 IOPS, Up to 80 Gib/s throughput 	|Up to 460,000 IOPS, Up to 36 Gib/s throughput|

## Azure Managed Disks

- Choose Disk Size, Type and Provision
- Encryption
    - Azure Disk Encryption - encrypts the Vm
    - Server-Side Encryption - physical disks on the data center
    - Encryption as Host - encrypted at rest and flows encrypted to the storage service

## Azure Queue Storage

# Design for Storage Security

- Azure security baseline for Azure Storage
- Shared Access Signature
- Firewall policies and rules
- Virtual network endipoints
- Secure Transfer
- Encryption keys - Microsoft-managed or Customer-managed
