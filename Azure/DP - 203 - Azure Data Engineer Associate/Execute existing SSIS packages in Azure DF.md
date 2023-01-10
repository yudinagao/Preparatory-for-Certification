# Execute existing SSIS packages in Azure DF

SSIS is a platform for building complex ETL solutions
- Component within a SQL Server
- used to develop data integration pipelines for on premises dw solutions
- is primarily a control flow engine that manages execution of workflows
    - workflows are help in packages, which can be executed on demand or on a schedule
    - task workflow is referred as control flow of the package
        - can include a specific task to manage data flow operations
- Data flows tasks by using a data flow engine that encapsulates the data flow in a pipeline
- each step in the dat flow task operates in sequence on a rowset of data
- a SSIS solution usually consists of one or more SSIS projects, each containing one or more SSIS packages

## SSIS Projects
- unit of deployment for SSIS solutions
- define project levl parameters to enable users to specify run time settings
- project level connections managers that reference data sources and destinations
- then can deploy project to a SSIS catalog and
- configure project level parameter values and connections as appropriate for execution environments

## SSIS PAckages
- define workflow of tasks to be executed
- package control flow can include on or more data flow tasks
    - each encapsulates its own data flow pipeline
    - packages can include package level parameter so that dynamic value can be passed to the package at run time

## Integration Runtime

- location of your Azure SSIS IR should be same location as the database
- during the provisioning of the azure SSIS Integration Runtime 
    - the node size - number of cores and number of nodes in the cluster
    - existing instance o azure SQl database to host the SSIS Catalog Database (SSISDB) and the service tier for the database
    - maximum parallel executions per node

## Set-up Azure SSIS Integration Runtime