# Introduction to DataVerse

Cloud based solution
- support interconnected application and process in a secure and compliant manner
- Designed to be you central data repository for business data
    - Field Service
    - Marketing
    - Customer Service
    - Sales
- Security
    - Azure Active Directory
    - Conditional access
    - Multi Factor Authentication
    - Authorization down to the row and column level
    - audit capabilities
- Logic
    - Business logic at data level
- Data
    - Control to shape your data
    - Discover, model, validate and report
- Storage
    - Azure Cloud
- Integration
    - API, webhooks, eventing and data export

- Dataverse database - single instance of M Dataverse
    - Tables
- Scalability
- Common Data Model vs Microsoft Dataverse
    - CDM - logical design - set of open-sourced, standardized, extensible data tables and relationships 
    - Open Data Initiative  

## Identify tables and columns in DataVerse

Types of Table:
- Standard
    - out-of-box tables
    - account, business unit, contact, task and user tables
    - can be customized
- Managed
    - not customizable
    - imported as part of managed solution
- Custom
    - unmanaged tables

## Understand Relationships

One to many x Many to many:
- parent child relationship
- unique column = key

## Environments
- Store, manage and share
- provision one dataverse database within that environment
- created under Azure AD tenant
    - only accessed by users of that tenant
    - bound to geographi location

## Business Rules

- apply and maintain business logic at data layer
    - set, clear column values
    - validate data and show error messages
    - show or hidr columns - model driven apps
    - enable or disable columns - model driven
    - create business recommendations based on BI

## Administer

Microsoft Power Platform admin Center
- Environments
- Data POlicies
    - restricts which data connectors and monitor these connections
    - limit flow in and out daverse tables
- Data Integration
    - create or add pre defines connections
    - dataverse and SQL server
