[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

API pūkete pēke Bank API
========================

The bank API enables the creating and deleting of the refund bank account for an identified customer’s account. It is 1 of 8 APIs that, together, make up the customer services suite.

[How customer services work](/digital-service-providers/services-catalogue/customer-and-account/customer-services-suite/how-customer-services-work)
 

How the bank API works
----------------------

The bank API requires the account API to be integrated.

The bank API enables the refund bank account held at the customer account level to be added and deleted. It requires the account ID for the addition or deletion of a refund bank account. The account ID is available through a call to the account API.

Note that the add function is effectively an update function if a refund bank account already exists on the customer account. It replaces the existing refund bank account with the added refund bank account in this scenario.

The bank API can only be used by:

*   the customer the data is associated to
*   a user with delegated access
*   an intermediary who’s linked to the customer
*   government agencies with a memorandum of understanding that allows them access to customer account level data.

The bank API enables the above users to update Inland Revenue’s customer account data from their native systems, and to avoid the use of manually facilitated channels.

For access to myIR File Upload and Gateway Services detailed technical documentation, register your organisation or login to Gateway Customer Support Portal using the links below.

Use the Getting started guide to find out how to access our sandbox (mock services) and test environments.

[Getting started guide](/digital-service-providers/guides-and-docs/getting-started)

### Gateway service capability for the bank API

The bank API provides the following capabilities through defined API operations and API paths.

| API operation | API path | Description |
| --- | --- | --- |
| POST | /bank | This operation either:<br><br>*   adds a refund bank account to the identified customer account if there is not already a refund bank account on the customer account<br>*   replaces an existing refund bank account on the identified customer account. |
| DELETE | /bank | Deletes the refund bank account from the identified customer account. |

Bank API business use cases
---------------------------

The following are examples of how to use the bank API to achieve specific business outcomes. The sequence of operations, the order in which they should be called, is indicated in the column of each operation.

| Number | Use case | POST /bank | DELETE /bank | Dependencies |
| --- | --- | --- | --- | --- |
| 1   | Add the refund bank account to an identified customer account. | 1   |     | Customer account ID has been obtained from the account API. |
| 2   | Update the refund bank account to an identified customer account. | 1   |     | Customer account ID has been obtained from the account API. |
| 3   | Remove the existing refund bank account from an identified customer account. |     | 1   | Customer account ID has been obtained from the account API. |

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