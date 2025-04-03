[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Te pūrongo haumitanga moni whiwhi mā ngā ratonga tomokanga Investment income reporting through gateway services
===============================================================================================================

Investment income reporting through gateway services lets organisations securely file investment income information to us through defined service operations. Use this service to file investment income information or amend a previously filed return.

Investment income reporting through the gateway services is available for the following withholding tax product types:

*   Approved issuer levy (AIL)
*   Dividend withholding tax (DWT)
*   Interest pay as you earn (IPS)
*   Non-resident withholding tax (NRT)
*   Resident withholding tax (RWT)
*   Portfolio investment entities (PIE) attributed income. 

Gateway services capability for investment income reporting
-----------------------------------------------------------

The gateway service used for investment income reporting is the Return service. It provides the following capabilities through defined service operations:

| Service operation | Description |
| --- | --- |
| Prepop | Not applicable for investment income reporting. |
| File | Enables payers to submit investment income information for a specific reporting period and if required submit amendments to previously filed investment income information. |
| RetrieveStatus | Provides the processing status of previously filed investment investment income information for a specific reporting period. |
| RetrieveReturn | Provides a copy of previously filed investment income information for a specific reporting period. |
| RetrieveFilingObligation | Not applicable for investment income reporting. |
| Retrieve list | Not applicable for investment income reporting. |

For access to myIR File Upload and Gateway Services detailed technical documentation, register your organisation or login to Gateway Customer Support Portal using the links below.

Investment income reporting business use cases
----------------------------------------------

The following use cases are examples of sequences of the gateway service operations that can be used to achieve a specific business outcome when providing investment income information.

The numbers for each use case are the order in which these operations should be called when using this service.

| Number | Use cases | File | Retrieve status | Retrieve return |
| --- | --- | --- | --- | --- |
| 1   | File a single IIR return for a month period and subsequently optionally retrieve return status. | 1   | 2\* |     |
| 2   | File multiple IIR returns for a month period and subsequently optionally retrieve return status. | 1   | 2\* |     |
| 3   | Amend one or more line items in an IIR return as a single filer. | 1   |     |     |
| 4   | Amend one or more line items in an IIR return as a multi-filer. | 1   |     |     |
| 5   | Replace all data in an IIR return (Reverse Replace) - file an amended single IIR return the same period for all transactions. | 1   |     |     |
| 6   | Intermediary files an IIR return on behalf of a payer for a specific period and optionally retrieve return status. | 1   | 2\* |     |
| 7   | Retrieve IIR return as a single filer for the specific period. |     |     | 1   |
| 8   | Retrieve IIR return as a multi-filer for a specific period. |     | 1\* | 2   |

Note: \* indicates optional process steps 

PIE business use cases
----------------------

The following use cases are examples of sequences of the gateway service operations that can be used to achieve a specific business outcome when providing PIE investment income information.

The numbers for each use case are the order in which these operations should be called when using this service.

| Number | Use cases | File | Retrieve status | Retrieve return |
| --- | --- | --- | --- | --- |
| 1   | File a periodic PIE return (IR852) using a gateway interface. | 1   |     |     |
| 2   | File investor certificate PIE returns (IR854) using a gateway interface. | 1   |     |     |
| 3   | File an annual reconciliation PIE return (IR853) using a gateway interface. | 1   |     |     |
| 4   | Amend a periodic PIE return (IR852) using a gateway interface. | 1   | 2\* |     |
| 5   | Amend an investor certificate PIE return (IR854) using a gateway interface | 1   | 2\* |     |
| 6   | Amend an annual reconciliation PIE return (IR853) using a gateway interface. | 1   | 2\* |     |
| 7   | Retrieve the status of a PIE return using a gateway interface. |     | 1   |     |
| 8   | Retrieve a previously filed PIE return using a gateway interface. |     | 1   | 2   |

Note: \* indicates optional process steps 

Download detailed use cases and process flows for an investment income reporting tax type:

[GWS business use cases AIL 2018 (PDF 947KB) Download guide](/-/media/project/ir/home/documents/digital-service-providers/gateway-services-business-use-cases/gws-business-use-cases-ail.pdf?modified=20201001004956&modified=20201001004956)

[GWS business use cases DWT 2018 (PDF 949KB) Download guide](/-/media/project/ir/home/documents/digital-service-providers/gateway-services-business-use-cases/gws-business-use-cases-dwt.pdf?modified=20201001004941&modified=20201001004941)

[GSW business use cases IPS 2018 (PDF 945KB) Download guide](/-/media/project/ir/home/documents/digital-service-providers/gateway-services-business-use-cases/gsw-business-use-cases-ips.pdf?modified=20201001004917&modified=20201001004917)

[GWS business use cases NRT 2018 (PDF 943KB) Download guide](/-/media/project/ir/home/documents/digital-service-providers/gateway-services-business-use-cases/gws-business-use-cases-nrt.pdf?modified=20201001004908&modified=20201001004908)

[GWS business use cases RWT 2018 (PDF 949KB) Download guide](/-/media/project/ir/home/documents/digital-service-providers/gateway-services-business-use-cases/gws-business-use-cases-rwt.pdf?modified=20201001014349&modified=20201001014349)

[GWS business use cases PIE 2020 (PDF 477KB) Download guide](/-/media/project/ir/home/documents/digital-service-providers/gateway-services-business-use-cases/gws-business-use-cases-pie.pdf?modified=20201001014729&modified=20201001014729)

##### Please choose a Content Collection

#### Tasks

*   [Getting started](/digital-service-providers/guides-and-docs/getting-started "Getting started")
    

#### Topics

*   [Access](/digital-service-providers/services-catalogue/access "Access")
    
*   [Guides and docs for developers](/digital-service-providers/guides-and-docs "Guides and docs for developers")
    

#### Other Sites

*   [Log in to gateway customer support portal](https://gws.ird.govt.nz/gws)
    
*   [Register organisation for gateway services](https://gws.ird.govt.nz/gws?id=sn_user_registration&sys_id=c11dff9997b44a501ed6344ef053af51)