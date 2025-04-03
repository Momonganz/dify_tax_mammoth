[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

API Kiritaki Customer API
=========================

The customer API provides general information about a customer. It is 1 of 8 APIs that, together, make up the customer services suite.

[How customer services work](/digital-service-providers/services-catalogue/customer-and-account/customer-services-suite/how-customer-services-work)
 

How the customer API works
--------------------------

When integrated through our gateway services, the customer API provides general information about an identified customer. The customer API accepts a customer ID (IRD number or other customer identifier) and returns high-level information for that customer including:

*   names (preferred name and trading name)
*   physical address
*   postal address
*   primary contact details (contact and phone)
*   secondary contact details (contact and phone)
*   start and stop dates
*   entity classification (for example, individual salary and wages, or non-individual limited partnership).

The customer API can only be used by:

*   the customer the data is associated to
*   a user with delegated access
*   an intermediary who’s linked to the customer.

The customer API enables the above users to query Inland Revenue’s customer data from their native systems, and to avoid the use of manually facilitated channels.

For access to myIR File Upload and Gateway Services detailed technical documentation, register your organisation or login to Gateway Customer Support Portal using the links below.

Use the Getting started guide to find out how to access our sandbox (mock services) and test environments.

[Getting started guide](/digital-service-providers/guides-and-docs/getting-started)

Gateway service capability for the customer API
-----------------------------------------------

The customer API provides the following capabilities through defined API operations and API paths.

| API operation | API path | Description |
| --- | --- | --- |
| POST | /customer | Returns the information of an identified customer. |

Customer API business use cases
-------------------------------

The following are examples of how to use the customer API to achieve specific business outcomes. All assume the user is authorised to access the customer's data. The sequence of operations, the order in which they should be called, is indicated in the column of each operation.

| Number | Use case | POST /customer |
| --- | --- | --- |
| 1   | Retrieve the customer addresses held by Inland Revenue. | 1   |
| 2   | Retrieve the customer contact details held by Inland Revenue. | 1   |
| 3   | Check the last time customer address, name or contact details held by Inland Revenue were updated. | 1   |

Supporting services
-------------------

[Identity and access services](/digital-service-providers/services-catalogue/access/identity-and-access)

[Returns and information](/digital-service-providers/services-catalogue/returns-and-information)

[Income Tax](/digital-service-providers/services-catalogue/returns-and-information/income-tax)

[Notifications](/digital-service-providers/services-catalogue/communication/notifications)

#### Tasks

*   [Getting started](/digital-service-providers/guides-and-docs/getting-started "Getting started")
    

#### Topics

*   [Identity and access](/digital-service-providers/services-catalogue/access/identity-and-access "Identity and access")
    
*   [Returns and information](/digital-service-providers/services-catalogue/returns-and-information "Returns and information")
    
*   [Managing myIR logons for gateway services](/digital-service-providers/guides-and-docs/managing-myir-logons-for-gateway-services "Managing myIR logons for gateway services")
    

#### Other Sites

*   [Log in to gateway customer support portal](https://gws.ird.govt.nz/gws)
    
*   [Register organisation for gateway services](https://gws.ird.govt.nz/gws?id=sn_user_registration&sys_id=c11dff9997b44a501ed6344ef053af51)