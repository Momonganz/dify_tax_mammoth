[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Te tuakiri me te āhei Identity and access
=========================================

Identity management and privacy concerns are important to us. Our gateway services are accessed over the internet, and access is controlled through security applied with authentication and authorisation mechanisms to keep our systems and customer information safe.

### Our services are restricted

Digital service providers wanting to integrate with us need to go through an approval process. 

Identity and access services 
-----------------------------

We provide 3 types of identity and access services to use with gateway services:

*   OAuth authentication
*   Machine-to-Machine authentication (M2M)
*   SH authentication.

For access to myIR File Upload and Gateway Services detailed technical documentation, register your organisation or login to Gateway Customer Support Portal using the links below.

### OAuth authentication

This authentication service is a token auth implementation using OAuth 2.0 for both cloud and native (desktop) client applications. 

### Machine-to-Machine (M2M) authentication

This authentication service utilises a client signed JSON Web Token (JWT) and is only available for service providers integrating through cloud service.

The service is available to use from **April 2020 (R4 Release)** for certain API services only. 

### SSH authentication

This authentication service is only available for service providers integrating to secure FTP file transfer services. 

How identity and access works
-----------------------------

We provide mechanisms for authentication and authorisation for both the end user and organisation entity types. Our security protocols include transport layer encryption, digital certificates, and access tokens.

The end user authentication and authorisation mechanism is token authorisation (OAuth 2.0). Both cloud or native (desktop) application options are enforced for client applications and authenticate end users using their myIR user ID and password to grant the application access to their Inland Revenue information.

The organisational authentication and authorisation mechanisms include:

*   Machine 2 Machine (M2M)
*   SSH Keys.

The M2M mechanism uses a client signed JSON Web Token (JWT) to sign messages, which lets us identify the service provider or a customer of a service provider.

Secure FTP file transfer services require a service provider to supply their public PGP key for file encryption. We supply our public SSH key in order to gain access to the service provider FTP server.

Find out more about security measures:

[Security measures for gateway services](/digital-service-providers/guides-and-docs/gws-architecture/security-measures)

Security protocols
------------------

The following security protocols apply when using our gateway services:

| Aspect | Standard/ protocol | Version |
| --- | --- | --- |
| Transport layer encryption | TLS | 1.2 |
| Digital certificates for mutual authentication | X.509 | RFC 5280 profile |
| Access tokens | OAuth | 2.0 |

Transport level security
------------------------

At a network level, access to our services is restricted to approved providers. This includes access to our test environments.

For integration through a cloud end point:

*   A TLS mutual authentication using the TLS 1.2 specification is applied across all gateway services in PROD and QUAL environments. This is not applicable for desktop client applications.
*   In the mock services environment, TLS mutual authentication is not used but IP address white listing is applied.

TLS connection requirements:

| Cloud providers | Desktop providers |
| --- | --- |
| Incoming connections are identified using client side X509 certificates. | Desktop providers must connect through one-way TLS. |
| The client side X509 certificates must be from a certificate of authority and cannot be self-signed. | No client side X509 certificates required. |

### Supporting guides and documents

Learn about the architecture of our gateway services and how we authorise identity and access to our application types.

[API architecture of gateway services](/digital-service-providers/guides-and-docs/gws-architecture)

  

Learn how to manage myIR logins for authorised representatives of an organisation so that access tokens can be generated for gateway services.

[Managing myIR logons and gateway services access tokens](/digital-service-providers/guides-and-docs/managing-myir-logons-for-gateway-services)

  

Use the Getting started guide to find out how to access our sandbox (mock services) and test environments.

[Getting started guide](/digital-service-providers/guides-and-docs/getting-started)

#### Tasks

*   [Manage access tokens for gateway services](/digital-service-providers/guides-and-docs/manage-access-tokens-for-gateway-services "Manage access tokens for gateway services")
    

#### Topics

*   [Managing myIR logons for gateway services](/digital-service-providers/guides-and-docs/managing-myir-logons-for-gateway-services "Managing myIR logons for gateway services")
    
*   [Security measures for gateway services](/digital-service-providers/guides-and-docs/gws-architecture/security-measures "Security measures for gateway services")
    

#### Other Sites

*   [Log in to gateway customer support portal](https://gws.ird.govt.nz/gws)
    
*   [Register organisation for gateway services](https://gws.ird.govt.nz/gws?id=sn_user_registration&sys_id=c11dff9997b44a501ed6344ef053af51)