# Relational Data Concepts

# Normalization
- Schema design process that minimizes data duplication and enforces data integrity
    - Separate  each entity into its own table
    - separate each discrete attribute into its own column
    - Uniquely identify each entity instace using a primary key
    - Use foreign key columns to link related entities

## Explore SQL
### DDL Statements - Data Definition
- CREATE
- ALTER
- DROP
- RENAME

### DCL Statements - Data Control
- GRANT
- DENY
- REVOKE

### DML Statements - Data Manipulation
- SELECT
- INSERT
- UPDATE
- DELETE
- JOIN

## Database Object

### View
- Virtual table based on the result of a SELECT query

### Stored Procedure
- Defines SQL statements that can be run on command.
- Encapsule programmatic logic 

### Index
- Helps you search data in a table
- Creates a tree-based structure to optimize query
- Consume storage space
- May slow down insert, update and delete operations.
