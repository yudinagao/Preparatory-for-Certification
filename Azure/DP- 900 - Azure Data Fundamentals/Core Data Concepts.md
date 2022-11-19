# Core Data Concepts

## Explore Core Data Concepts

### Data Formats:
    - Structured Data
    - Semi Structured
    - Unstructured Data

### File Storage
    - Delimited Text Files (CSV, TSV)
    - JavaScript Object Notation (JSON)
    - Extensible MarkupL Language (XML)
    - Binary Large Object (BLOB)
    - Optimized Files Formats: 
        - Avro - Row-based format - header stored in JSON, data in Binary - compressing data and miniminz storage
        - Parquet - Column-based Format - metadata to describe each chunk - specialized in processing and storing
        - ORC - Optimized Row Columnar format - Apache Hive - data stripes

### DataBases
    - Relational:
        - Store and query Sctructured Data 
        - Normalization - elimination duplicate Data
    - Non-Relational:
        - Don't apply relational schema
        - Key-Value - Unique keys to associated value
        - Document - Specific key-value where value is a JSON
        - Column Family - store tabular - rows and columns - divide columns into groups , each family holds a set of columns that are logically related together
        - Graph - entities as nodes with links to define relationships
    
### Transactional Data Processing
#### OLTP - Online Transactional Processing
    - OPtimized for read and wirte
    - CRUD Operations
    - ACID:
        - Atomicity - transaction - single unit - succeeds or fails completely
        - Consistency - One valid state to another
        - Isolation - Concurrent transaction cannot interfere with one another, and must result in consistent database state
        - Durability - transaction committed, it will remain committed.
### Analytical Processing
    - Uses Read-Only - historical data and business metrics
    - Data files stored central data lake
    - ETL
        - Schema Fact tables and Dimension tables
    - Data aggregated and loaded into OLAP ( Online Analytical Processing) model or cube.
    - Data stored, can be queried

    - Data lakes - large scale data analytical processing
    - Data WareHouses - store data relational schema
        - optimized for read operations
        - may require denormalization for OLTP
    - OLAP - optimized for analytical workloads, drill up/down at multiple hierarchical levels,
    
