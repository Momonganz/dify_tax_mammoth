[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Te ratonga takawaenga Intermediation service
============================================

Intermediation is the process of linking an account or customer record belonging to an individual or organisation to a client list of a business intermediary (like a tax agent, bookkeeper or payroll bureau) so the intermediary can act on their behalf.

About the intermediation service
--------------------------------

The intermediation service is a SOAP web service that enables intermediaries to:

*   link, delink or update the intermediary client list to their clients' accounts or customer master
*   retrieve clients and client lists that have already been established.

Intermediaries can use this service to create and manage links from a client list to a customer master or their accounts on any tax product.

[Intermediaries and others](/intermediaries-and-others)

For access to myIR File Upload and Gateway Services detailed technical documentation, register your organisation or login to Gateway Customer Support Portal using the links below.

Use the Getting started guide to find out how to access our sandbox (mock services) and test environments.

[Getting started guide](/digital-service-providers/guides-and-docs/getting-started)

Gateway services capability
---------------------------

The intermediation service provides the following capabilities through defined service operations on the gateway services:

| Service operation | Description |
| --- | --- |
| Link | Enables:*   linking of a business intermediary's client list to a client account<br>*   a business intermediary's client list to the client's customer master. |
| Delink | Enables:*   delinking of a business intermediary's client list to a client account<br>*   a business intermediary's client list from the client's customer master. |
| Update | Enables:*   updating of a business intermediary's ability to redirect mail or disbursements on a client account<br>*   switching of a client account between a business intermediary's client lists. |
| Retrieve client list | Enables retrieving of client lists belonging to a business intermediary as well as all of the clients in each list. This can be filtered by client account type or client list ID. |
| Retrieve client | Enables retrieving of the client attributes between a business intermediary and a linked client or client accounts. This can be filtered by a client’s account type. |

Intermediation service business use cases 
------------------------------------------

The following are examples of sequences of the gateway return service operations that could be used to achieve a specific business outcome.

#### Keys

*   Gateway service operations: RCL = Retrieve Client List, RC = Retrieve Client
*   The numbers for each use case are the order in which these operations should be called when using this services.

| Use case | Gateway service operation |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
| Link | Delink | Update | RCL | RC  |
| --- | --- | --- | --- | --- | --- |
| 1\. Retrieve complete list of clients and then request to link a new client to a client list. | 2   |     |     | 1   |     |
| 2\. Link an existing client’s customer master to a client list. | 1   |     |     |     |     |
| 3\. Retrieve a client’s details (such as client accounts they have access to, if mail or disbursements are redirected to them) and then update client details. |     |     | 2   |     | 1   |
| 4\. Remove a client from a client list. |     | 1   | 2   |     |     |
| 5\. View lists of clients that have been approved or are pending approval (authorised payroll bureaus only) |     |     |     | 1   |     |
| 6\. Move a client to another client list the intermediary manages. |     |     | 1   |     |     |

Supporting services
-------------------

[Identity and access service](/digital-service-providers/services-catalogue/access/identity-and-access)

[Software intermediation service](/digital-service-providers/services-catalogue/access/software-intermediation)

#### Tasks

*   [Getting started](/digital-service-providers/guides-and-docs/getting-started "Getting started")
    

#### Topics

*   [Working with us](/digital-service-providers/working-with-us "Working with us")
    
*   [Guides and docs for developers](/digital-service-providers/guides-and-docs "Guides and docs for developers")
    
*   [Availability of our services](/digital-service-providers/availability-of-our-services "Availability of our services")
    

#### Other Sites

*   [Log in to gateway customer support portal](https://gws.ird.govt.nz/gws)
    
*   [Register organisation for gateway services](https://gws.ird.govt.nz/gws?id=sn_user_registration&sys_id=c11dff9997b44a501ed6344ef053af51)