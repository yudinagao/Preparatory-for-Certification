# Design Modern DW using Synapse

Modern Data Warehouse brings together all data at any scale easily, meaninng, you get insights through analytical dashboards, operational reports or advanced analytics for all users.
- increased volumes of data
- new varieties of data
- data velocities

- Architecture
    - Data Ingestion and Preparation
        - data lake so store their data in different types in a Data lake Store Gen2
        - ingest data
            - code -free 100 data integrations with DF
            - SSIS packages
            - customers can seamlessly author, monitor and manage their big data 
        - Data preparation option - Azure Databricks
    - Making the data ready for consumption by analytical tools
        - DW using dedicated SQL pool - Azure Synapse ANalytics
        - leverages Massively Parallel Processing engine
    - Providing access to data, in a shaped format so ir can be easily consumed by data visualization tool
        - POwer BI 
            - enourmous set of data sources, queired live or used to mdeol
    
- Data Storage for a modern DW
    - source within a staging area = landing zone
        - neutral storage area between source systems and DW
    - Reduce Contencio on source system
        - must minimize the resource usage
        - grabbing data at source and DUMPING into staging area
    - Deal with ingestion of source systems on different schedules
    - join data together from different source systems
        - freedom to perform any work you need without impact source and DW
        - create additional tables to aid the process of join -> mapping tables
        - create a separate table that contains metadata that maps the data in a column from one source system with another column from another source system that represents the same business entity
    - Rerun failed dw loads from a staging area
        - dw loads may not be all successfull
        - handle scenarios where a rerun may be necessary during busy hours, and needs to occur without disrupting the source systema again
        - holding onto the staging area

# File formats of ingesting raw data in batch

Three types of data loading velocities as one of three latencies
- Batch
- Interactive query
- Real-time/near real time
    - Synapse connect to IoT Hub or Event Hub as input source, and outputting files do ADLS Gen2 storage account.
        - options - set the serialization, JSOn, encoding like UTF-8, minimum number of rows per file
    - can land the streaming data to dedicated sql pool
        - can use stream analytics
When working with small files, can affect negatively performance
    - larger size files for better performances

## Prepare and transform data with Synapse

- natively perform data transformation with synapse using data flows task
- add source data 
    - if u want only one file from a folder with multpiple files
        - need to create another dataset or use parameterization
        - not import schema from data lake, u can import schema
