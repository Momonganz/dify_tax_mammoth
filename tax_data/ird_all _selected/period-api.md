[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

API mō te wā Period API
=======================

The period API provides information about 1 or more periods for an identified customer account. It is 1 of 8 APIs that, together, make up the customer services suite.

[How customer services work](/digital-service-providers/services-catalogue/customer-and-account/customer-services-suite/how-customer-services-work)
 

How the period API works
------------------------

When integrated through our gateway services, the period API provides information about a customer’s account periods. The period service accepts an account ID and account type, and an optional date range. It returns information about each period of the specified account or, if a date range is specified, it returns information about periods within that date range only. This information includes:

*   period start and end dates
*   the account or product type
*   filing frequency
*   whether a notice of assessment has been issued
*   whether a return has been filed or is still expected
*   the value of any default assessment.

An extended attribute list is returned for income tax accounts, which includes:

*   a balance date
*   extension of time details
*   provisional tax details
*   imputation or Māori Authority credit amounts.

The period API can only be used by:

*   the customer the account is associated to
*   a user with delegated access to the customer’s account
*   an intermediary who’s linked to the customer’s account
*   government agencies with a memorandum of understanding that allows them access to customer account level data.

Some customers may split their individual account access across delegated users. This means a user may not be able to see all accounts for a specific customer.

The period API enables the above users to query Inland Revenue’s period data from their native systems, and to avoid the use of manually facilitated channels.

For access to myIR File Upload and Gateway Services detailed technical documentation, register your organisation or login to Gateway Customer Support Portal using the links below.

Use the Getting started guide to find out how to access our sandbox (mock services) and test environments.

[Getting started guide](/digital-service-providers/guides-and-docs/getting-started)

Gateway service capability for the period API
---------------------------------------------

The period API provides the following capabilities through defined API operations and API paths.

| API operation | API path | Description |
| --- | --- | --- |
| POST | /list | Returns the information of periods for an identified customer account. |

Period API business use cases
-----------------------------

The following are examples of how to use the period API to achieve specific business outcomes. The sequence of operations, the order in which they should be called, is indicated in the column of each operation.

| Number | Use case | POST /list | Parameters |
| --- | --- | --- | --- |
| 1   | Retrieve details for all periods for a given customer account that I am authorised to access. | 1   | *   Account ID<br>*   Account type |
| 2   | Retrieve details for a single period for a given customer account that I am authorised to access. | 1   | *   Account ID<br>*   Account type<br>*   'From' date (where date is within required start period)<br>*   'To' date (where date is within required end period) |
| 3   | Retrieve account data for a range of periods for a given customer account that I am authorised to access. | 1   | *   Account ID<br>*   Account type<br>*   'From' date (where date is within required start period)<br>*   'To' date (where date is within required end period) |

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