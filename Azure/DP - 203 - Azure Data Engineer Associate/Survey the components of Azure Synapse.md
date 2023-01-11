# Survey the components of Azure Synapse

- Create an Azure Synapse ANalytics workspace
    - creates several resources
        - Azure Data Lake Storage Gen2
            - primary storage and container to store worskpace data
    - Workspace stores data in Apache Spark tables
        - stores Spark application logs - /synapse/workspacename
    - endpoints created that can be used to connect to SQL on demand services and Azure Synapse Analytics Workspace itself

    - Enables you to create pools, either SQL or Spark Pools
        - seamlessly mixed and matched 
        - do this through Azure Synapse shared metadata, - different engines to share dbs and tables
        - Enables Modern DW workload pattern and giver workspace SQL engines access to db
            - SQL engine create own object not shared with other engines
    
    - Central location where u can view information about these resources
With a serverless SQL on demand endpoint available,a nd an Azure Data lake Storage Gen2 account,
    - realize value form product by uploading to the data lake 
    - uses serverless sql to prepare and explore data

## Azure Synapse Analytics SQL

- implement dw solution or perform data virtualization
     - dw -> cetral repository of data in relational tables
        - data is retrieved, cleansed and transformed
        - data stored in permanent talbe
    - data virtualization allow u to interact with data without the need to understand how data is formatted, structured or type
        - explore data without technical specifications
        - enables ad hoc data preparation scenarios
- Synapse SQl offer both dedicated and serveless model
    - dedicated model - sql pools
        - collection of analytic resources provisioned when using ir
        - predicatable performance and cost
    - serverless 
        - unplanned ad hoc workloads
        - data exploration
        - prep data for virtualization

## Apache Spark in Azure Synapse Analytics
Spark pools in Azure Synapse Analytics offer a fully managed Spark service
- Speed and effiiency
    - 2 minutos for less than 60 nodes
    - 5 minutes for more than 60 nodes
    - shutdown, by default, 5 minutes after last job executed
- Easy creation
- Esay use
    - custom noteboo
- Scalability
    - Auto-scale enabled
        - pools scale by adding or removing nodes as needed
        - spark can shut down without loss daat, data stored in Azure Storage or Data lake
- Support for Azure Data Lake Storage gen2
    - as well as blob storage
    - primary case - process big data that cannot be handled with synapse sql
    - can be integrated with databricks
    - 200 anaconda libraries

## Orchestrate data integration with Synapse
Synapse pipelines cloud based ETL and data integration 
- create and schedule data driven workflows
- build ETL ou ELT
- integrates SQL pool, spark pools
- can be integrated with power bi

## Hybrid transactional analytical processing with Azure Synapse Link

- enables business to perform analytics over a db system that is seen to provide transactional capabilities without impacting in performance
- enables transactional and analytical to support near realtime analysis of operational data
- enable link 
    - all transactions data is stored in a fully isolated column