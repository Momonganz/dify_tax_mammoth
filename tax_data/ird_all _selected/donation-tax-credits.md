[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Ngā hua tāke takoha mō ngā kaiwhakarato ratonga matihiko Donation tax credits for digital service providers
===========================================================================================================

An individual who donates to an approved donee organisation can claim a tax credit for a gift of money of $5 or more. Testamentary gifts, that is, those given, bequeathed, done or appointed by will and gifts by way of a full or partial debt forgiveness are excluded. Donation tax credits are limited by the individual’s taxable income so can usually only be processed after the end of the tax year. 

Claiming donation tax credits
-----------------------------

Donation tax credits are processed:

*   automatically each pay day for donations made through payroll giving
*   automatically any time after the associated tax year is complete for donations recorded in myIR
*   on submission of the IR526 tax credit claim form.

Tax credits can only be claimed for receipted donations and if the individual has met their filing obligation for the period. Individuals submitting a claim must provide receipts before their claim can be processed, but tax agents, bookkeepers and other representatives need only provide receipts if requested.

For access to myIR File Upload and Gateway Services detailed technical documentation, register your organisation or login to Gateway Customer Support Portal using the links below.

Filing donation tax credit claims through our gateway services
--------------------------------------------------------------

The donation tax credit gateway service can be used to:

*   submit a new or amended donation tax credit claim form
*   query the processing status of a previously filed donation tax credit claim form
*   request a copy of a previously filed donation tax credit claim form.

Gateway service capability for donation tax credits
---------------------------------------------------

The gateway service used for donation tax credit is the return service. It provides the following capabilities through defined service operations:

| Service operation | Description |
| --- | --- |
| Prepop | Not available for donation tax credits. |
| File | Submits new or amended donation tax credit claim forms. |
| RetrieveStatus | Provides the status of previously filed donation tax credit claim forms. |
| RetrieveReturn | Provides a copy of previously filed donation tax credit claim forms. |
| RetrieveFilingObligation | Not available for donation tax credits. |

Donation tax credit business use cases
--------------------------------------

The following are examples of sequences of the gateway return service operations that could be used to achieve a specific business outcome.

#### Keys

*   Gateway service operations: RS = Retrieve Status, RR = Retrieve Return, RFO = Retrieve Filing Obligation
*   The numbers for each use case are the order in which these operations should be called when using this services.

| Use case | Gateway service operation |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
| File | Prepop | RS  | RR  | RFO |
| --- | --- | --- | --- | --- | --- |
| 1\. Submit a new donation tax credit claim form | 1   |     |     |     |     |
| 2\. Retrieve the status of a previously submitted donation tax credit claim form |     |     | 1   |     |     |
| 3\. Retrieve a previously submitted donation tax credit claim form |     |     |     | 1   |     |
| 4\. Amend and submit a donation tax credit claim form | 2   |     |     | 1   |     |

#### Tasks

*   [Getting started](/digital-service-providers/guides-and-docs/getting-started "Getting started")
    

#### Topics

*   [Guides and docs for developers](/digital-service-providers/guides-and-docs "Guides and docs for developers")
    
*   [Availability of our services](/digital-service-providers/availability-of-our-services "Availability of our services")
    

#### Other Sites

*   [Log in to gateway customer support portal](https://gws.ird.govt.nz/gws)
    
*   [Register organisation for gateway services](https://gws.ird.govt.nz/gws?id=sn_user_registration&sys_id=c11dff9997b44a501ed6344ef053af51)