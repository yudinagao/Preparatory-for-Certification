# Identity Governance in Azure AD

 - GOvern the identity lifecycle
    - No Access -> Join -> Move -> Leave
    - Premium offers integration with HR systems
 - Govern access lifeCycle
    - Users require different levels of access 
    - Dynamic groups
    - creates attribute-based rules 
 - Secure privileged access to administration
    - monitoring privileged key part
    - Azure AD Privileged Identity Management - (PIM)
    - Premium P2

 ### Key Questions
 - Which users should have access to which resources?
 - What are those users doing with that access?
 - Are there effective organizational controls for managing access?
 - Can auditors verify that the controls are working?

 ## Entitlement management and access reviews

Identity governance
   - Delegate creation of access package to non-admin
   - delegated access package manager defines policies that includes rules
      - request access
      - aprove their access
      - when access expires
   - Manage external users
   - Azure AD Premium P2

## Azure AD Access Reviews

Efficiently manage group membership, access to enterprise applications and role assignment
- Access review created
   - each user reviews theis own access
   - one or more users review everyone's access
   - track progress
- Premium P2

## Azure AD terms of use

Users read relevant disclaimers for legal or compliance requirements
   - Before access sensitive data
   - on a recurring schedule, to remind of regulations
   - based on users attributes, applicable to certain roles
   - presenting terms for users

## Privileged Identity Management (PIM)

Manage, control and monitor access to important resources. Mitigates the risks of excessive, unnecessary or misused access permissions. Premium P2

- Just in time, providing privileged acess only when needed
- Time-bound - assigning start and end dates
- Approval based
- Visible 
- Auditable - full access history

## Azure Identity Protection

- Automate the detection and remediation of identity-based riks
- Investigate risks using data in the portal
- Export risk detection data to third party tools for further analysis

Risks three tiers: Low, medium and high
   - Anonymous IP Adress
   - Atypical travel
   - Malware linked IP Adress
   - Unfamiliar sign in propertis
   - Password spray
   - Azre AD Threat intelligence
   - Leaked Credentials
   - 