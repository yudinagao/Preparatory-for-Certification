# Services and Identity Types of Azure and

Azure Active Directory
    - Cloud-based identity and access management services
    - Internal resources
    - External resources

- Simplifies how organizations manage authorization and access
- Provides a single identity system. 
- Control access to corporate apps and resources.
- Multi-factor authentication
- Single Sign ON

## Azure AD editions

- Azure AD Free - administer users and create groups, sync with on premises, basic reports, configure self-service password change for cloud users, and sing sign across azure.
- Office 365 Apps - free version + self-service password reset for cloud users, and device write back
- Azure AD Premium P1 - Free version + Office 365 and advanced administration, dynamic groups, self-service management groups, Microsoft Identity Manager with cloud write back.
- Azure AD Premium 2 - Premium p1 + Azure AD Identity Protection, also Privileged Identity Management
- Pay as you go services: Azure AD B2C

## Azure AD identity Types

- User
    - representation of something that's managed by Azure AD. You can create a group to give access permissions to all users.
    - Azure B2B - Guest Users. 

- Service Principal 
    - identity for application 

- Managed Identity
    - System assigned:
        - managed identity directly on a service instance.
    - User assigned
        - Standalone resource

|Property	|System-assigned managed identity	|User-assigned managed identity|
| ----  |   ------  | ----- |
|Creation	|Created as part of an Azure resource, such as an Azure virtual machine or Azure App Service.	|Created as a standalone Azure resource|
|Lifecycle	|Shared lifecycle with the Azure resource. When the parent resource is deleted, the managed identity is also deleted.	|Independent life cycle. Must be explicitly deleted.|
|Sharing across Azure resources	|Cannot be shared. Associated with a single Azure resource.	|Can be shared. A user-assigned managed identity can be associated with more than one Azure resource.|
|Common use cases	|Workloads that are contained within a single Azure resource. Workloads for which you need independent identities, such as an application that runs on a single virtual machine.	|Workloads that run on multiple resources and which can share a single identity. Workloads that need preauthorization to a secure resource as part of a provisioning flow. Workloads where resources are recycled frequently, but permissions should stay consistent. For example, a workload where multiple virtual machines need to access the same resource.|

- Device
    - Azure AD registered Devices
        - Bring Your own Device
    - Azure AD Joined
        - Device owned by organization
    - Hybrid Azure AD joined Services

## Types of External Identities

### B2B

Share applications and services with guest users. Self service sign up. SSO

### B2C

Customer Identity Access Management (CIAM)
Sign in with prefered social, enterprise and local account identities
Features of Premium P1 e P2

## Hybrid Identity

On-premises and on cloud
- AZure AD Password hash synchronization
    - same credentials - Azure AD manages
    - password validation on cloud
- Azure AD Pass-Through authentication
    - password validation on premises
- Federation authentication
    - single sign on via smart cards or certificates. 
    - sign in multi factor on premises
    - third party authentication solution