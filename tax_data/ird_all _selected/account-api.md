[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

API pūkete Account API
======================

The account API provides either a list of accounts for an identified customer or information about a single customer account. It is 1 of 8 APIs that, together, make up the customer services suite.

[How customer services work](/digital-service-providers/services-catalogue/customer-and-account/customer-services-suite/how-customer-services-work)

An account represents a tax type (for example, income tax) or a product (for example, KiwiSaver). 

How the account API works
-------------------------

When integrated through our gateway services, the account API provides general information about customer accounts. The account API accepts either a customer ID or an account ID. When a customer ID is provided, the account API will return a list of account IDs associated with the customer. When an account ID is provided, the account API returns information about that identified account including:

*   account status
*   account type (tax or product name)
*   filing details
*   start and stop dates
*   physical address
*   postal address
*   primary contact details (contact and phone)
*   secondary contact details (contact and phone)
*   refund bank account.

The account API can only be used by:

*   the customer the account is associated to
*   a user with delegated access to the customer’s account
*   an intermediary who’s linked to the customer’s account
*   government agencies with a memorandum of understanding that allows them access to customer account level data.

Some customers may split their individual account access across delegated users. This means a user may not be able to see all accounts for a specific customer. 

The account API enables the above users to query Inland Revenue’s customer account data from their native systems, and to avoid the use of manually facilitated channels.

For access to myIR File Upload and Gateway Services detailed technical documentation, register your organisation or login to Gateway Customer Support Portal using the links below.

Use the Getting started guide to find out how to access our sandbox (mock services) and test environments.

[Getting started guide](/digital-service-providers/guides-and-docs/getting-started)

Gateway service capability for the account API
----------------------------------------------

The account API provides the following capabilities through defined API operations and API paths.

| API operation | API path | Description |
| --- | --- | --- |
| POST | /list | Returns a list of accounts for an identified customer. |
| POST | /account | Returns the information of an identified customer account. |

Account API business use cases
------------------------------

The following are examples of how to use the account API to achieve specific business outcomes. The sequence of operations, the order in which they should be called, is indicated in the column of each operation.

| Number | Use case | POST /list | POST /account |
| --- | --- | --- | --- |
| 1   | Retrieve a list of accounts for an identified customer that I am authorised to access. | 1   |     |
| 2   | Retrieve account data for an account that I am authorised to access but do not have the account ID. | 1   | 2   |
| 3   | Retrieve account data for an account that I am authorised to access and already have the account ID. |     | 1   |

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