# How to build a model-driven app

Model-driven app design is a component-focused aproach to app dev.
- Does not require code
- much of layout is determined

Three design phases:
- Model your business data
    - uses metadata-driven architecture
    - customize apps withou code
    - determine what data the app will need
    - how it relates to other data
- Define you business processes
    - defining and enforcing consistent business process
    - helps ensure app users can focus on their work
- Build the app

## Builing blocks of model-driven apps

- Data
    - Tables
    - Columns
    - Relationship
    - Choice columns
- User interface
    - App
        - Components
        - Properties
        - Client type
        - URL
    - Site map  
        - specifies the navigation in you app
    - Form
    - View
- Logic
    - Business process flow
        - walk users through standard business process
        - repeability
    - Workflow
        - automate business process without user interface
    - Actions
        - manually invoke behaviors
    - Business rule
        - apply rules or recommendation logic to a form to set filed requirements
        - Hide or show, validate data
    - Flows
        - Power Automate cloud based service
        - workflows between apps and services, 
        - get notificaitons, sync files, collect data
- Visualization
    - Chart
    - DashBoard
    - Embedded Microsoft Power BI

## Design of model-driven apps

- Specify for each table
    - Forms
    - Views
- Add new content to an application
    - Table based form and view
    - Dashboard
    - Custom
- Testing the application

Data Model
- What type of data will your solution be storing or collecting?
- How will this data relate or coincide with the other data you're working with?
    - Data types

Understand the needs of the user

Business Rules
- behaviors at data layer
    - setting conditions fow when a field is required, 
    - setting a default value,
    - showing or hiding a field based on a criteria

Business process flows
- guide users through using your app
- provide visuals on next steps based on the status of the data

Dashboards

## Creating a model-driven app
- add account tablw to your app
- add forms and views to your app
- add contact page to you app
- save and publish your app

## Control Security and share model-driven apps

Role-based security to share

- Create or set up a security role
    - predefined roles
    - expand existing predefined roles 
    - create a custom security role

Predefined roles:
- Environment Maker
    - create new resources to environment
    - apps, connections, custom API, gateways and flows
    - can't access data
- system administrator
    - full permission to customize and administer the environment
    - creating, changing and assigning security roles
    - view all data
- system customizer
    - full permission to customize environment
    - can only view rows for tables that they create
- Microsoft Datavers User
    - can run the app
    - perform commom tasks fot the rows they own
- Delegate
    - code run as or impersonate another user

