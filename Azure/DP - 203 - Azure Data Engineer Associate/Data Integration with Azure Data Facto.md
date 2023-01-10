# Data Integration with Azure Data Factory

ADF - cloud-based data integration service that orchestrates the movement and transformation of data between various data stores and compute resources
- 100 eterprise connectors

## Extract

- Defines data Source:
    - identify resource group, subscription, identity information such as key or secret
- Define the data
    - define the data using database query, a set of files, Azure blob storage name 

## Transform

- Splitting, combining, deriving, adding, removing or pivoting columns
- map field between data source and destination
- aggregate or merge data

## Load

- Destinantion
    - JSON, file or blob
    - built-in azure functions
- start the job:
    -  test the ETL job in a job or test environment, then migrate to prodcution
- monitor 
    - set up a proactive and reactive  monitoring system

## Integration Runtimes
- is referenced by linked service or activity
- provides compute environment where activity either is run or gets dispatched from
- compute infra used by DF
    - Data flow
    - data movement
    - activity dispatch
    - SSIS package execution - SQL Server Integration Services

Types:
- Azure
- Self-Hosted
- Azure-SSIS

Copy activity
- between two cloud data stores: when both source and sink are using Azure IR
- copying between cloud data source and a data source in private network
    - if either are slef hosted, IR is executed in self-hosted
- copying between data sources in private networks
    - both soruce and sink must point to the same instance of integration runtime
