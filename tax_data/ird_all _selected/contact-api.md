[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

API whakapā Contact API
=======================

The contact API enables the creating, updating and deleting of the contact details of a customer or an account. It is 1 of 8 APIs that, together, make up the customer services suite.

[How customer services work](/digital-service-providers/services-catalogue/customer-and-account/customer-services-suite/how-customer-services-work)

How the contact API works
-------------------------

The contact API requires the customer or account API to be integrated.

The contact API enables the contact details held at either the customer level or the customer account level to be added, updated and deleted. It requires either:

*   the customer ID or account ID for the addition of a contact or phone number to a customer or account
*   a contact ID for the update or deletion of a contact from a customer or account
*   a phone ID for the update or deletion of a phone number from a customer or account.

The account ID is available through a call to the account API. The contact ID and phone ID are available through a call to either the customer API or the account API.

The contact API can only be used by:

*   the customer the data is associated to
*   a user with delegated access
*   an intermediary who’s linked to the customer
*   government agencies with a memorandum of understanding that allows them access to customer account level data.

The contact API enables the above users to update Inland Revenue’s customer or account data from their native systems, and to avoid the use of manually facilitated channels.

For access to myIR File Upload and Gateway Services detailed technical documentation, register your organisation or login to Gateway Customer Support Portal using the links below.

Use the Getting started guide to find out how to access our sandbox (mock services) and test environments.

[Getting started guide](/digital-service-providers/guides-and-docs/getting-started)

### Gateway service capability for the contact API

The contact API provides the following capabilities through defined API operations and API paths.

| API operation | API path | Description |
| --- | --- | --- |
| POST | /contact | Adds a contact to either the identified:<br><br>*   customer<br>*   account. |
| PUT | /contact | Updates the name of an identified contact for either the:<br><br>*   customer<br>*   account. |
| DELETE | /contact | Deletes a contact for either the:<br><br>*   customer<br>*   account. |
| POST | /phone | Adds a phone number to the contact details of either the identified:<br><br>*   customer<br>*   account. |
| PUT | /phone | Updates the phone number of an identified contact for either the:<br><br>*   customer<br>*   account. |
| DELETE | /phone | Deletes the phone number of an identified contact for either the:<br><br>*   customer<br>*   account. |

Contact API business use cases
------------------------------

The following are examples of how to use the contact API to achieve specific business outcomes. The sequence of operations, the order in which they should be called, is indicated in the column of each operation.

The use cases for adding, updating and deleting contacts works the same way for both primary and secondary contacts.

| Number | Use case | POST /contact | PUT /contact | DELETE /contact | Dependencies |
| --- | --- | --- | --- | --- | --- |
| 1   | Add a contact to a customer. | 1   |     |     | Customer does not already have either a primary or secondary contact. |
| 2   | Add a primary contact to a customer account. | 1   |     |     | Customer does not already have either a primary or secondary contact. |
| 3   | Update the name of an existing contact for a customer. |     | 1   |     | Contact ID for update has been obtained from the customer API. |
| 4   | Update the name of an existing contact for a customer account. |     | 1   |     | Contact ID for update has been obtained from the account API. |
| 5   | Remove an existing contact for a customer. |     |     | 1   | Contact ID for removal has been obtained from the customer API. |
| 6   | Remove an existing contact for a customer account. |     |     | 1   | Contact ID for removal has been obtained from the account API. |

The use cases for adding, updating and deleting phone numbers of contacts works the same way for both primary and secondary contacts.

| Number | Use case | POST /phone | PUT /phone | DELETE /phone | Dependencies |
| --- | --- | --- | --- | --- | --- |
| 1   | Add a phone number to an existing contact for a customer. | 1   |     |     | Contact ID has been obtained from the customer API. |
| 2   | Add a phone number to an existing contact for a customer account. | 1   |     |     | Contact ID has been obtained from the account API. |
| 3   | Update an existing phone number on a contact for a customer. |     | 1   |     | Phone ID for update has been obtained from the customer API. |
| 4   | Update an existing phone number on a contact for a customer account. |     | 1   |     | Phone ID for update has been obtained from the account API. |
| 5   | Remove a phone number from a contact for a customer. |     |     | 1   | Phone ID for removal has been obtained from the customer API. |
| 6   | Remove a phone number from a contact for a customer account. |     |     | 1   | Phone ID for removal has been obtained from the account API. |

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