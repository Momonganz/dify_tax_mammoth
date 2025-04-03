[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Ngā pitomutunga ratonga Service endpoints
=========================================

Digital service providers can connect to our gateway services through either cloud or desktop - they'll be directed to the appropriate endpoints.

Cloud-based connection endpoints
--------------------------------

A centralised cloud location can connect through mutual TLS certificates. These need to be exchanged before connection to each environment.

On the cloud endpoint we have the ability to throttle traffic from digital service providers whose heavy usage may cause issues for other digital service providers.

| Subject | Description |
| --- | --- |
| Purpose | Default endpoint to connect digital service providers to our gateway services |
| Client application type | Cloud |
| Constraints | Only for source locations with client side TLS certificates. |
| Mutual TLS | We trust the certificate the digital service provider associates with the TLS connection as the client for mutual TLS connections and use it to identify the digital service provider and the web service they are using. |
| Minimum TLS version | 1.2 |
| Port | 4046 |
| End-user authentication and authorisation | *   The Token Auth (OAuth 2.0) process is used to authenticate end-users using their myIR logon and password and grant 3rd party software consent to access their information.<br>*   Requires an online user to enter their myIR logon and password to grant the application access to their Inland Revenue information. |
| Organisational authentication and authorisation | The M2M mechanism uses a client signed JSON Web Token (JWT) to sign messages, which lets us identify the data owner (service provider or a customer of a service provider). |
| Firewalling in production | *   No IP address restrictions.<br>*   Access limited by certificate enrolment. |
| Firewalling in non-production environments | *   Endpoints are firewalled and IP address whitelisting needed.<br>*   Access limited by certificate enrolment. |

Desktop connection endpoints
----------------------------

A desktop server location must connect through one-way TLS.

No client side X509 certificates are required.

| Subject | Description |
| --- | --- |
| Purpose | Additional endpoint provided to facilitate connecting from desktops which might be:<br><br>*   high volumes of sources addresses<br>*   transient client IP addresses<br>*   not realistically associated with client side TLS certificates<br>*   not individually integrated to setup certificate trust. |
| Client application type | Desktop/native applications. For connecting from multiple decentralised clients. |
| Constraints | *   Less scalable.<br>*   Subject to tighter security controls.<br>*   Less able to be shielded from heavy usage of the service by others.<br>*   OAuth2 refresh tokens will not be offered. |
| Mutual TLS | Server side TLS only. |
| Minimum TLS version | 1.2 |
| Port | 443 (default https port) |
| End-user authentication and authorisation | *   The Token Auth (OAuth 2.0) process is used to authenticate end-users using their myIR logon and password and grant 4th party software consent to access their information.<br>*   Requires an online user to enter their myIR logon and password to grant the application access to their Inland Revenue information. |
| Firewalling in production | No IP address restrictions. |
| Firewalling in non-production environments | Firewalled - IP whitelisting needed for gateway service endpoints. |

Endpoint URLs
-------------

The endpoint URLs for the mock services (sandbox), test and production environments will be provided to digital service providers as part of the integration process.

Delegated permissions
---------------------

These services let a user retrieve only the data of customers that their credential (as represented by the OAuth token) has access to.

If an account or its data is targeted by the request parameters but the user does not have permission, an error will be returned. This access will depend on delegation permissions set up in myIR.

Timeouts
--------

Our gateway services typically have a 60 second timeout configured, although this may be adjusted after testing.

Supporting services
-------------------

[Identity and access service](/digital-service-providers/services-catalogue/access/identity-and-access)

#### Tasks

*   [Getting started](/digital-service-providers/guides-and-docs/getting-started "Getting started")
    

#### Topics

*   [Working with us](/digital-service-providers/working-with-us "Working with us")
    
*   [Services catalogue](/digital-service-providers/services-catalogue "Services catalogue")
    
*   [Guides and docs for developers](/digital-service-providers/guides-and-docs "Guides and docs for developers")
    

#### Other Sites

*   [Log in to gateway customer support portal](https://gws.ird.govt.nz/gws)
    
*   [Register organisation for gateway services](https://gws.ird.govt.nz/gws?id=sn_user_registration&sys_id=c11dff9997b44a501ed6344ef053af51)