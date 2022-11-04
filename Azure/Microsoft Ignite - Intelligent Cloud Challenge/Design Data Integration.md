# Design Data Integration

## Azure Data FActory

- Orchestrate data movement
- Transform data at scale
- Connect and collect
- Transform and enrich
- Continuos Integration and delivery (CI/CD) and delivery
- Monitor

## Azure Data Lake

- Data Storage
- Data Access
- Data Costs
- Data Performance
- Data Security
- Data Redundancy
- Data Scalability
- Data Analysis

### How it works

- Ingesting Data
    - Ad-hoc data
    - Relational data
    - Streaming Data
- Accessing Data
    - Storage Explorer
- Setting Access Control
    - Azure RBAC
    - ACL

# Azure DataBricks

- Big Data and ML platform
- Databricks SQL
- DataBricks Data Science & Engineering
- DataBricks ML

# Azure Synapse Analytics

- Synapse SQL Pool
- Synapse Spark Pool
- Synapse Pipelines
- Synapse Link
- Synapse Studio

- Variety of data sources
- Need to implement ML solutions using Apache Spark
- Descriptive
- Diagnostic
- Predictive
- Prescriptive

# Azure Data Factory X Azure Synapse Analytics

|Criteria 	|Azure Data Factory 	|Azure Synapse Analytics|
|----       |----                   |-----                  |
|Data sharing 	|Can be shared across different data factories 	|No sharing of data|
|Solution templates 	|Provided with Azure Data Factory template gallery 	|Provided with Synapse Workspace Knowledge center|
|Integration Runtime cross region support 	|Support Cross region data flows 	|Does not support cross region data flows|
|Monitoring 	|Integrated with Azure Monitor 	|Diagnostic logs in Azure Monitor|
|Monitoring of Spark Jobs for Data Flow 	|Not supported 	|Supported by the Synapse Spark pools|

# Design a strategy for hot, warm and cool data path

|Requirement 	|Description|
|-----          |-----      |
|When data requirements are known to change frequently
When processing or displaying data in real time| 	Use Hot data path|
When data is rarely used. The data might be stored for compliance or legal reasons
Used for data that is consumed for long term analytics and batch processing 	|Use Cold data path|
When you need to store or display a recent subset of data
Used for data that is consumed for small analytical and batch processing 	|Use Warm data path|

# Azure Stream Analytics

- Route Data to Storage and Analytics (Power BI)
- Data to ML to train
- Fully managed
- Low cost
- Run in cloud or in Intelligent Edge
- Perfomance
- Security