[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

API ingoa Name API
==================

The name API enables the creating, updating and deleting of the customer's names. It is 1 of 8 APIs that, together, make up the customer services suite.

[How customer services work](/digital-service-providers/services-catalogue/customer-and-account/customer-services-suite/how-customer-services-work)
 

How the name API works
----------------------

The name API requires the customer API to be integrated.

The name API enables the preferred name and trading name of a customer to be added, updated and deleted. It requires either:

*   the customer ID for the addition of a name
*   a name ID for the update or deletion of a name.

The name ID is available through a call to the customer API. The name API does not allow any access to the legal name of a customer.

The name API can only be used by:

*   the customer the data is associated to
*   a user with delegated access
*   an intermediary who’s linked to the customer.

The name API enables the above users to update Inland Revenue’s customer data from their native systems, and to avoid the use of manually facilitated channels.

For access to myIR File Upload and Gateway Services detailed technical documentation, register your organisation or login to Gateway Customer Support Portal using the links below.

Use the Getting started guide to find out how to access our sandbox (mock services) and test environments.

[Getting started guide](/digital-service-providers/guides-and-docs/getting-started)

Gateway service capability for the name API
-------------------------------------------

The name API provides the following capabilities through defined API operations and API paths.

| API operation | API path | Description |
| --- | --- | --- |
| POST | /name | Adds a name of a given type (preferred or trading) to the customer data set. |
| PUT | /name | Updates the details of an existing name in the customer data set. |
| DELETE | /name | Deletes a given name from the customer data set. |

Name API business use cases
---------------------------

The following are examples of how to use the name API to achieve specific business outcomes. The sequence of operations, the order in which they should be called, is indicated in the column of each operation.

| Number | Use case | POST /name | PUT /name | DELETE /name | Dependencies |
| --- | --- | --- | --- | --- | --- |
| 1   | Add a preferred name to a customer. | 1   |     |     | Customer does not already have a preferred name. |
| 2   | Update an existing preferred name for a customer. |     | 1   |     | Name ID for update has been obtained from the customer API. |
| 3   | Remove an existing preferred name for a customer. |     |     | 1   | Name ID for removal has been obtained from the customer API. |

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