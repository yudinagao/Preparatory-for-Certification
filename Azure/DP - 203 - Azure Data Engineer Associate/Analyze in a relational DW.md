# Analyze in a relational DW

Dimension tables
- two key values
    - surrogate key
        - specific DW and uniquely identifies each row
        - incrementing integer number
    - alternate key
        - natural or business key
            - identifies specific instance of an entity
    
    - may be populated from multiple sources, risk of duplicating business key
    - simple numeric key generally perform better in queries that join a lot of tables
    - atributes may change over time, used to support historic report

Fact Tables
