[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

API wāhinoho Address API
========================

The address API enables the creating, updating and deleting of the address of a customer or an account. It is 1 of 8 APIs that, together, make up the customer services suite.

[How customer services work](/digital-service-providers/services-catalogue/customer-and-account/customer-services-suite/how-customer-services-work)
 

How the address API works
-------------------------

The address API requires the customer or account API to be integrated.

The address API enables the addresses held at either the customer level or the customer account level to be added, updated and deleted. It requires either:

*   the customer ID or account ID for adding an address to a customer or account
*   an address ID for the update or deletion of an address from a customer or account.

The customer ID or account ID is available through a call to the customer API or account API, respectively. The address ID is available through a call to either the customer API or the account API.

The address API can only be used by:

*   the customer the data is associated to
*   a user with delegated access
*   an intermediary who’s linked to the customer
*   government agencies with a memorandum of understanding that allows them access to customer account level data.

The address API enables the above users to update Inland Revenue’s customer or account data from their native systems, and to avoid the use of manually facilitated channels.

For access to myIR File Upload and Gateway Services detailed technical documentation, register your organisation or login to Gateway Customer Support Portal via the links below.

Use the Getting started guide to find out how to access our sandbox (mock services) and test environments.

[Getting started guide](/digital-service-providers/guides-and-docs/getting-started)

### Gateway service capability for the address API

The address API provides the following capabilities through defined API operations and API paths.

| API operation | API path | Description |
| --- | --- | --- |
| POST | /address | Adds an address of a given type (physical or postal) to either the identified:<br><br>*   customer<br>*   account. |
| PUT | /address | Updates the provided details to the identified address for either the:<br><br>*   customer<br>*   account. |
| DELETE | /address | Deletes the details of the identified address for either the:<br><br>*   customer<br>*   account. |

Address API business use cases
------------------------------

The following are examples of how to use the address API to achieve specific business outcomes. The sequence of operations, the order in which they should be called, is indicated in the column of each operation.

| Number | Use case | POST /address | PUT /address | DELETE /address | Dependencies |
| --- | --- | --- | --- | --- | --- |
| 1   | Add a postal address to a customer. | 1   |     |     | Customer does not already have a postal address. |
| 2   | Update an existing postal address for a customer. |     | 1   |     | Address ID for update has been obtained from the customer API. |
| 3   | Update an existing postal address for a customer account. |     | 1   |     | Address ID for update has been obtained from the account API. |
| 4   | Remove an existing postal address for a customer. |     |     | 1   | Address ID for removal has been obtained from the customer API. |
| 5   | Remove an existing postal address for a customer account. |     |     | 1   | Address ID for removal has been obtained from the account API. |

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