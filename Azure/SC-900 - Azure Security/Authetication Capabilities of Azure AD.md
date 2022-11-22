# Authetication Capabilities of Azure AD

## Authentication Methods in Azure AD

- Passwords
- Phone
    - SMS based authentication
    - Voice call Verification
- OATH
    - Open Authentication -specify how time based, one-time password codes are generated
        - Software OATH
        - Hardware OATH
- Passwordless
    - Biometrics
        - WIndows Hello for Businnss
            - Two factor authentication
            - PIN and biometrics
        - FIDO2
            - Fast Identity Oline
            - USB devices, BLuetooth or Near FIled Communication (NFC)
- Microsoft Authenticator APP
    - Passwordless
    - download phone app

## Multi-Factor Authentication (MFA) in Azure AD

- SOmething you know
- SOmething you gave
- SOmenthing you are

- Securitiy Defaults
    - Enforcing Azure AD MFA registration to all users
    - Forcing administrators to use MFA
    - Requiring all Users to complete  MFA when needed

## Self-service Password Reset (SSPR) in Azure AD

- Password chnage
- Password Reset
- ACcount unlock

- To use SSPR: 
    - Assigned and Azure AD license
    - Enabled SSPR by admin
    - Registered, with authentication  methods they want to use

## Password Protection and Management Capabilities of Azure AD

- reduces Risks of users setting weak passwords
- Global banned password list
- Custom Banned passwords list
    - Feature of Premium P1 and P2
- 