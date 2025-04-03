[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Te ratonga tuhinga Document service
===================================

The document service enables the transmission of electronic documents between a customer, partner or intermediary and Inland Revenue. 

How the document service works
------------------------------

When integrated through our gateway services, the document service can be used to:

*   send us electronic documents
*   view previously submitted electronic documents
*   receive electronic documents that we've sent 
*   remove electronic documents submitted by mistake.

Documents used in this service can include:

*   mail we've generated for communicating with customers
*   documents we've requested from a customer
*   documents a customer voluntarily provides us.

We provide documents in PDF format, while documents provided to us can be in many different file formats including PDF, DOC, DOCX, XLSX, TXT, JPG, JPEG, PNG, TIF and ODS.

Please note, the ‘MailType’ is included in the response payload for all letters issued by our new system.

Letters issued under our old system are not available in the Document service API.

The list linked below provides all the current mail type codes and the title of each letter item to assist with identifying what each letter is about.

This reference list only contains letters that publish electronically as these are the only ones available in myIR or in the Document service. There is still a small volume of letters that will always print as paper for various reasons.

In general, letters from our new system are formatted as 2 letters followed by 4 numbers. Older letters issued out of our old system have a different format which is a mix of letters and numbers.

For access to myIR File Upload and Gateway Services detailed technical documentation, register your organisation or login to Gateway Customer Support Portal using the links below.

Use the Getting started guide to find out how to access our sandbox (mock services) and test environments.

[Getting started guide](/digital-service-providers/guides-and-docs/getting-started)

Gateway service capability for the document service
---------------------------------------------------

The document service provides the following capabilities through defined service operations:

| Service operation | Description |
| --- | --- |
| Create | Enables documents to be sent to us electronically. |
| Read | Retrieves a specific identified document (or list of documents) from us. |
| Update | Marks a mistakenly-sent document to be reversed. |

Document service business use cases
-----------------------------------

The following are examples of use cases of the document service operations that could be used to achieve a specific business outcome. The numbers for each use case are the order in which these operations should be called when using this service.

| Number | Use case | Create | Read | Update |
| --- | --- | --- | --- | --- |
| 1   | Submit documents to Inland Revenue in response to a request for information | 1   |     |     |
| 2   | Submit documents to Inland Revenue to provide supporting information for a return | 1   |     |     |
| 3   | View a list of previously submitted electronic documents |     | 1   |     |
| 4   | View a submitted electronic document |     | 1   |     |
| 5   | Remove a document submitted by mistake |     |     | 1   |

Supporting services
-------------------

[Identity and access services](/digital-service-providers/services-catalogue/access/identity-and-access)

[Notifications service](/digital-service-providers/services-catalogue/communication/notifications)

#### Tasks

*   [Getting started](/digital-service-providers/guides-and-docs/getting-started "Getting started")
    

#### Topics

*   [Access](/digital-service-providers/services-catalogue/access "Access")
    
*   [Returns and information](/digital-service-providers/services-catalogue/returns-and-information "Returns and information")
    
*   [Customer and account](/digital-service-providers/services-catalogue/customer-and-account "Customer and account")
    

#### Other Sites

*   [Log in to gateway customer support portal](https://gws.ird.govt.nz/gws)
    
*   [Register organisation for gateway services](https://gws.ird.govt.nz/gws?id=sn_user_registration&sys_id=c11dff9997b44a501ed6344ef053af51)