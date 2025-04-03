[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Te ratonga moni whiwhi Income service
=====================================

The income service enables digital service providers to retrieve a customer’s income profile data reported to Inland Revenue. 

How the income service works
----------------------------

The income service enables access to a customer's income and tax data from all known income sources for a specific date range. It returns income data that consists of the income source, date income was recognised, income type, amount, and any deductions from that income.

Income data is accessible by an intermediary who's linked to the customer’s income tax account or the customer to whom the income belongs.

When integrated through our gateway services it can be used to match investment and income data to what we have recorded.

Software developer kit (SDK)
----------------------------

View and download the income service software developer kit to help you integrate:

*   test scenarios
*   test data
*   sample request and response messages
*   the Open API YAML file
*   the build pack that provides the data definitions for the request and response messages.

[Income service software developer kit (SDK) on GitHub](https://github.com/InlandRevenue/Gateway_Services-Customer-and-Account/tree/master/Service%20-%20Income)

  

Use the Getting started guide to find out how to access our sandbox (mock services) and test environments.

[Getting started guide](/digital-service-providers/guides-and-docs/getting-started)

Gateway services capabilities for the income service
----------------------------------------------------

The gateway service used for the income service is the income API. It provides the following capabilities through defined service operations:

| Service operation | Description |
| --- | --- |
| Post | Retrieves income information from Inland Revenue.  <br>Requires an IRD number, a 'from' date, and an optional 'to' date. |

The income service business use case
------------------------------------

The following is an example of a business use case on the income service that could be used to achieve a specific business outcome.

| Number | Use case | API Call: Post |
| --- | --- | --- |
| 1   | As an intermediary, request income information for a customer and receive this information, then match the income data to what you've recorded for the customer. | 1   |

Supporting services
-------------------

[Identity and access services](/digital-service-providers/services-catalogue/access/identity-and-access)

[Accounting income method (AIM)](/digital-service-providers/services-catalogue/returns-and-information/accounting-income-method)

[Income tax](/digital-service-providers/services-catalogue/returns-and-information/income-tax)

[Investment income reporting](/digital-service-providers/services-catalogue/returns-and-information/investment-income-reporting)

[Payday filing](/digital-service-providers/services-catalogue/returns-and-information/payday-filing)

#### Tasks

*   [Getting started](/digital-service-providers/guides-and-docs/getting-started "Getting started")
    

#### Topics

*   [Identity and access](/digital-service-providers/services-catalogue/access/identity-and-access "Identity and access")
    
*   [Returns and information](/digital-service-providers/services-catalogue/returns-and-information "Returns and information")
    
*   [Managing myIR logons for gateway services](/digital-service-providers/guides-and-docs/managing-myir-logons-for-gateway-services "Managing myIR logons for gateway services")
    

#### Other Sites

*   [Log in to gateway customer support portal](https://gws.ird.govt.nz/gws)
    
*   [Register organisation for gateway services](https://gws.ird.govt.nz/gws?id=sn_user_registration&sys_id=c11dff9997b44a501ed6344ef053af51)