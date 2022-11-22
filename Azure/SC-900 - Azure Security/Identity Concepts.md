# Identity Concepts

## Authentication x Autorization

- Authentication - proving that a person is who they say they are
- Autorization - Allowed access

## Identity as primary security perimeter

Identity: is the set of things that defines or characterizes someone or something. 

- Administration
    - Creation and management/ governance of identities for users, devices and services. How and under whats circumstances the characteristics of identities can be changed
- Authentication
    - How much of an IT system needs to know about and identity to have sufficient proof that they are who they say they are. Challenging a party for legitimate credentials
- Autorization - processing incoming identity data to determine the leve of access 
- Auditing - tracking who does what, when, where and how. In-depth reporting , alerts and governance of identities

## Role of Identity Provider

The client communicates with the identity provider by giving an identity that can be authenticated. When the identity (which can be a user or an application) has been verified, the identity provider issues a security token that the client sends to the server. The server validates the security token through its trust relationship with the identity provider. 

## Single Sign-ON

Users logs in once - and credential is used to access multiple applications or resources. WHen you set-up SSO between multiple identity providers, Called Federation.

## Concepts of directory Services and Active Directory

Active Directory - set of directory services
Active Directory Domain Services (AD DS)
    - Store information about members of domain, devices and users. Verifies their credentials, defines their access levels.
    - Manages multiple infra components  and systems using a single identity per user. 
    - Doesn't support mobile or modern authentication.
Azure Active Directory provides  Identity as a Service (IDaaS)

## Concepts of Federation

Enables access of services across Organizational or domain boundaries  - trust relationships between the respective domain identity provider. Not bi directional