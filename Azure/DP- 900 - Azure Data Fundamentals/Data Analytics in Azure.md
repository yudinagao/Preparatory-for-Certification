# Data Analytics in Azure

- Batch processing
    - Large volumes of data at a convenient time
    - Schedule to run
    - time delay between ingesting data and getting results
    - input data must be prepped before processing
- Stream processing
    - time critical operations
    - real-time response

| Feature    |  Batch   | Stream |
| ------     | -----    | ----   |
| Data scope | Can process all data in the dataset| Tipically only has access to most recent data received, or within a time window|
| Data size  | Large dasets efficiently |  Individual records or micro batches consisting of few seconds |
| Performance | Latency is tipically few hours | latency in order of seconds or milliseconds|
| Analysis | Complex analysis | simple response functions, aggreegates or calculations such as rolling averages|
## Combination of batch and streaming processing
- Data events are captured in real time
- data are ingested into a data store
- if real-time anlytics are not neeed, captured streaming data is written to data store to subsequent batch
- if is needed, stream processing tech is used to prepare for real time analysis or visualization, filtering or aggregating over temporal window
- The non-streaming is batched processed for analysis and the results persists in data store
- results of stream processing are  persisted in data store to support historical analysis
- Analytical and visualization tools are used to present and explore

!!! Lambda and Delta Architecture !!!

## General architecture for stream processing

- Events generate data
- Data captured 
- Data processed
- Data written to an output

### Real-time Analytics in Azure

- Azure Stream Analytics
    - PaaS
    - Define streaming jobs
    - Apply perpetual query
    - write to an output
    - Ingest Data from input 
    - Query
    - Can create a job or a Cluster

- Spark Structured Streaming
    - Open Sourced Library
    - complex streaming solutions
    - Azure Synapse Analytics, DataBricks or HDInsight
    - Spark Structured Streaming Library 
        - provides API for ingesting, processing and outputting
    - Dataframe - encapsulates a table

- Azure data Explorer
    - High performance
    - optimized for ingesting and querying batch or streaming data with a time-series element
    - Kusto Query Language (KQL)

#### Sources for streaming processing

- Azure Event Hubs
    - queues event data, event processed in order, exatcly once
- Azure IoT Hub
    - optimized for managing event data from IoT
- Azure Data Lake Store Gen2
    - highly scalable
- Apache Kafka
    - open source solution used with Apache Spark

#### Sinks for stream processing

- Azure Event Hub
- Azure Data Lake Store Gen2
- Azure SQL Database or Azure Synapse Analytics
- Microsoft Power BI



