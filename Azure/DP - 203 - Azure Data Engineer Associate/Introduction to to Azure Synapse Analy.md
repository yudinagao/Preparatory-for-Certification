# Introduction to to Azure Synapse Analytics

SInlge cloud scale platform that supports multiple analytical technologies, enabling a consolidated and integrated experience for data engineer
- Descriptive Analytics 
    - "What is happening in mu business"
    - answered through creating a DW in which historical data is persisted in relational tables
    - multi dimensional modeling and reporting
- Diagnostic Analytics
    - "Why is this happening"
    - Exploring data that already exists in a DW
    - Typically, involves a wider search of your estate to  find more data about this type os analysis
- Predictive Analytics
    - "What is likely to happen in the future based on previous trends and patterns?"
- Prescriptive Analytics
    - Autonomous decision making based on real-time or near real-time analysis of data, using predictive analytics

## Azure Synapse
- Azure Synapse workspace
    - defines an instance of synapse
    - create in azure subscription using the portal or automated using cli, or azure resource manager
    - access to synapse studio, web based portal

    - One of core resources:
        - data lake ( linked service of Azure Data Lake Storage Gen2)
    - Includes built-in support for creating, running and managing pipelines
    - Support SQL based data querying and manipulation
        - built-in serverless pool optimized for using relational SQL semantics to query file-based data in the data lake
        - Custom dedicated SQL pools that host relational dw
        - uses a distributed query processing model to parallelize SQL operations
            - highly scalable solution
            - dedicated SQL pool to create relational DW
    - can create one or more Spark pools
        - use notebooks to combine codes and notes
    - Azure Synapse Data Explorer
        - data processing engine based on Azure Data Explorer service
        - Intuitive syntax named Kusto Query Language (KQL)
            - enable high performance, low latency os analysis
    - Can be integrated with other Azure Service
        - Azure Synapse Link
            - near real-time synchronization with Cosmos DB, Azure SQL, Dataverse
        - Microsoft Power BI
        - Microsoft Purview
        - Microsoft Machine Learning

## WHen to Use
- Large scale DW
- Advanced Analytics
- Data Exploration and Discovery
- Real Time Analytics
- Data Integration
- Integrated Analytics