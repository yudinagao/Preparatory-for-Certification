# Azure Data Factory

Cloud-based ETL and data integration
Build ETL

- Connect and collect
    - Type:
        - Structured
        - Semi structured
        - Unstructured
    - Read data from source data store
    - tasks:
        - Serialization/ Deserialization
        - Compression/ Decompression
        - Column Mapping
        - ...
    - Write data to the sink
- Transform and enrich
    - Data transformation graphs that run on Spark
- CI/CD
    - Azure DevOPs
    - GitHub
- Monitoring
    - Azure Monitor
    - API
    - PowerShell
    - Azure Monitor logs
    - Health panels in Azure Portal

Key Components:
- Pipelines
    - manage activities as a set
- Activities
    - data movemnt
    - data transformation
    - control activities
- Datasets
    - inputs or outputs
- Linked Services
    - Connect to a external resource
    - data store or compute resource
- Data Flows
    - no need for code
- Integration Runtime
    - Bridges between activity and linked services

- Set triggers and schedule
- Associate a pipeline with a trigger or manually
- Connect to linked services
- Monitor all