# Perform code-free transformation at scale with DF

## Azure DF transformation methods

Tranforming using Mapping Data Flow
- resulting data flows that are created are subsequently executed on scaled out apache spark cluster
- monitor the execution of transformations - progress or errors

Tranforming data using compute resources
- On demand HDInsight
- AzureBatch
- Azure Machine Learning Studio Machine
- Azure Machine Learning
- Azure Data Lake Anaytics
- Azure SQL, SQL Data WareHouse, Sql Server
- Azure Databricks
- Azure Function

Transforming data using SSIS packages

## DF Transformation Types
- Schema Modifier Transformations
    - modification to a sink destination
    - create new columns
- Row modifier transformations
    - impact how the rows are presented in the destination
    - sort
- Multiple Inputs/Output tranformations
    - Generate new data pipelines or merge pipelines into one
    - union

Mapping Data Flows
- Aggregate
    - SUM, MIN, MAX, COUNT
    - Group by
- Alter Row
    - Insert, delete, update, and upsert policies in rows
    - one to many conditions 
        - specified in order of priority
    - DDL and DML
- Conditional split
    - Multiple input/output
    - route rows of data to different streams based on matching conditions
- Derived Column   
    - generate new cloumns or modify existing fields using data flows expression languages
- Exists
    - check whether data existir in aother source or stream
- Filter
    - filter row based on condition
- Flatten
    - take array values inside hierarchical structures such as JSON
    - unroll them into individual rows
- Join
    - combine data
- Lookup
    - enables you to reference data from another source
- new-branch
    - apply multiple sets of operations and transformation against same data stream
- Pivot
    - aggregation where one or more grouping columns has distinct row values transformed into individual columns
- Select
    - Alias columns and stream names, and drop or reorder columns
- Sort
- Source
- Surrogate key
    - add an increment non-business arbitrary key value
- Union
    - combine multiple data vertically
- Unpivot
- Window

Data Flow Expression Builder
- coded 