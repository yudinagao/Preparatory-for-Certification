# Azure Storage for non-Relational data

## Azure Blob Storage

- Store unstructured data as binary large objects (BLob)
- Store Blob in containers - group together
- Organize blobs in hierarchy of virtual folders

| Type        |   Description           | Space      | Best case use |
|   ----      | -----        | -----      | ---      |
|Block Blobs  |set of blocks, block is the smallest amount that can be read or written as an individual unit | Each block vary size, up to 100 MB, contains up to 50.000 blocks, maximum size of 4.7TB | Store Discrete, Large Binary Objects that change infrenquetly|
| Page Blobs  | Collection of fixed size 512 byte-pages | Can hold up to 8 TB| Optimized for support random read nad write operations, you can fetch and store data for a singe page; Azure uses it to implement virtual disk storage for VMs|
| Append Blob | Block blob optimed for append operations | Each block up to 4 MB, maximum size of and append blob is just over 195 GB| You can only add block at the end, can't update or delete existing blocks|


| Tier | Use cases | Storage Costs|
| ---- | ---       | ---          |
| Hot Tier | For blobs that are accessed frequently | Stored on high-performance media|
| Cool Tier | For data that are accessed in frenquently | Lower Performance, Common for new blobs to be accessed frequently initially but less so  as time passes|
| Archive Tier | Intended for historical data, required only rarely | lowest storage cost but increased latency - Need to change the tier, the blob will be re hydrated |

You can create lifecycle management  policies for blobs in a storage account. Can automatically move blob to Hot or Cool or Archive Tier. Policy is based on number of days since last modifications. Can delete outdated Blobs.

## Azure DataLake Storage Gen2

Separate service for hierarchical data storage for analytical lakes

- Scalability of blob storage and cost-control of storage tiers,
- Hierarchical system capabilities  and compatility with major analytics systems of Azure Data lake Store
- System like Hadoop in Azure HDInsight, Azure Databricks and Synapse Analytics can be hosted in 

## Azure Files

Enables you to store a file on a computer and grant access to that file to other computers

- Up to 100 TB, maximum size of a file is 1 TB, but you can set quotas to limit
- supports 2000 concurrent connections
- Standard tier - Hard disk based hardware
- Premium tier - SSD
- Support netwroking sharing protocols:
    - Server Message blocks (SMB) - 
    - Network File System (NFS) - needs to create a VN and use a premium tier 

## Azure Tables

- NoSQL storage - key-value pair
- data is stored denormalized
- timestamp column records date and time of modification
- no foregin keys, relationships, stored procedures, views
- Partitioning - groups related rows 

## Azure Cosmos DB

- SUpports multiple API - query data using API 
- Uses indezes and partitioning to fast read
- can enable multi-region writes
- Cosmos DB automatically allocates space in a container for your partitions, each partition up to 10 GB

- IoT and telematics,
- Retail and Marketing
- Gaming
- Web and mobile applications

### Cosmos DB API

- Azure Cosmos DB for NoSQL - Document data model
- Azure Cosmos DB for MongoDB - Data Stored in Binary JSON
    - MongoDB Query Language (MQL) - object oriented syntax
- Azure Cosmos DB for PostGreSQL
- Azure Cosmos DB for Table
- Azure Cosmos DB for Apache Cassandra - Column family data model
- Azure Cosmos DB for Apache Gremlin - Graph data model
