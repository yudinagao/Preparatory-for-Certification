# Access Management Capabilities of Azure AD

## Conditional Access in Azure AD
- extra layer of security
- implemented through policies
- signals user, location, device and application

### Conditional Access Signals

 - User or group membership - policies can be targetered to all users, specific group of users, directory rules or external users
 - Named location information
 - Device
 - Application
 - Real-time sign in risk detection
 - Cloud apps or actions
 - User risks

 ### Access Control

 - Block Access
 - Grant Access
 - Requires one or more conditions
    - Requires MFA
    - Require device marked as compliant
    - Require   hybrid Azure AD joined device
    - Require approved client app
    - Require app protection policy
    - Require password change

- Control user access based on session controls

## Benefits of Azure AD roles and role-based access Control

- Built-in Roles:
    - Global Administrator
    - User Administrator
    - Billing Administrator
- Custom Roles
    - Preset List
    - Require Premium P1 or P2
- Only grant the access the user needs
- Categories of Azure AD Roles
    - Azure AD specific roles
    - service specific roles - manage features within the service
    - Cross-service roles

### Difference between Azure AD RBAC and Azure RBAC

 - Azure AD RBAC - Azure AD roles controls access to Azure AD resources such as users, groups or applications
 - Azure RBAC - Azure roles control access to Azure Resources such as Vms, Storage