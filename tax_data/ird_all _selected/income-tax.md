[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Te tāke moni whiwhi mō ngā kaiwhakarato ratonga matihiko Income tax for digital service providers
=================================================================================================

Everyone in New Zealand needs to pay tax on income they earn, whether they’re an individual, business, or organisation. 

Income tax returns
------------------

Most salary and wage earners will automatically receive an income tax assessment and will not need to submit a return, but any individual who does not receive an automatic assessment, and all businesses and organisations, must submit an annual income tax return unless they have an exemption.

Income tax information is submitted to us on one of these return types:

*   IR3 - Individual income tax return - resident
*   IR3NR - Individual income tax return – non-resident
*   IR4 - Companies income tax return
*   IR6 - Trust or estate income tax return
*   IR7 - Partnership or look-through companies income tax return
*   IR8 - Māori authority income tax return
*   IR9 - Clubs and societies income tax return
*   IR44 - Registered superannuation fund income tax return
*   IR1215 - Income tax return and disclosure - as agent

When submitting an income tax return the filer is also able to provide additional forms (attachments) that apply to the individual’s or organisation’s situation.

For access to myIR File Upload and Gateway Services detailed technical documentation, register your organisation or login to Gateway Customer Support Portal using the links below.

Filing income tax returns through our gateway services
------------------------------------------------------

The income tax gateway service can be used to:

*   submit new or amended income tax returns and supplementary forms
*   request income tax information held by us for a customer
*   query the processing status of a previously filed income tax return
*   request a copy of a previously filed income tax return
*   request the due date of the next expected income tax return.

All income tax returns and supplementary forms are supported by the income tax gateway service.

Gateway service capability for income tax
-----------------------------------------

The gateway service used for income tax is the return service. It provides the following capabilities through defined service operations:

| Service operation | Description |
| --- | --- |
| Prepop | Provides information in pre-populated fields. |
| File | Submits new or amended income tax returns. |
| RetrieveStatus | Provides the status of a previously filed income tax return. |
| RetrieveReturn | Provides a copy of previously filed income tax return. |
| RetrieveFilingObligation | Provides the due date of the next expected income tax return. |

Income tax business use cases
-----------------------------

The following are examples of sequences of the gateway return service operations that could be used to achieve a specific business outcome.

#### Keys

*   Gateway service operations: RS = Retrieve Status, RR = Retrieve Return, RFO = Retrieve Filing Obligation
*   The numbers for each use case are the order in which these operations should be called when using this service.

| Use case | Gateway service operation |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
| File | Prepop | RS  | RR  | RFO |
| --- | --- | --- | --- | --- | --- |
| 1\. Submit a new income tax return | 2   | 1   |     |     |     |
| 2\. Retrieve the status of a previously submitted return and next filing obligation |     |     | 1   |     | 2   |
| 3\. Retrieve previously submitted income tax return |     |     |     | 1   |     |
| 4\. Amend and submit an income tax return | 2   |     |     | 1   |     |

Automatic assessment (auto-calc) business use cases
---------------------------------------------------

We'll calculate assessments automatically for individuals if we have all their income information for the tax year. We'll recalculate those assessments if the income information is later updated. The income tax gateway service can be used to view and manage automatically calculated assessments.

[Income tax assessments (auto-calc)](/income-tax/income-tax-for-individuals/what-happens-at-the-end-of-the-tax-year/income-tax-assessments)

  

The following are examples of sequences of the gateway return service operations that could be used to achieve a specific business outcome.

#### Keys

*   Gateway service operations: RS = Retrieve Status, RR = Retrieve Return, RFO = Retrieve Filing Obligation
*   The numbers for each use case are the order in which these operations should be called when using this service.

| Use case | Gateway service operation |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
| File | Prepop | RS  | RR  | RFO |
| --- | --- | --- | --- | --- | --- |
| 1\. Retrieve auto-calculated return |     |     | 2   | 1   |     |
| 2\. Confirm auto-calculated return | 3   |     | 2   | 1   |     |
| 3\. Amend and submit reportable income | 2   | 1   |     |     |     |
| 4\. Submit other income | 2   | 1   |     |     |     |

#### Tasks

*   [Getting started](/digital-service-providers/guides-and-docs/getting-started "Getting started")
    

#### Topics

*   [Income tax for businesses and organisations](/income-tax/income-tax-for-businesses-and-organisations "Income tax for businesses and organisations")
    
*   [Income tax for individuals](/income-tax/income-tax-for-individuals "Income tax for individuals")
    

#### Other Sites

*   [Log in to gateway customer support portal](https://gws.ird.govt.nz/gws)
    
*   [Register organisation for gateway services](https://gws.ird.govt.nz/gws?id=sn_user_registration&sys_id=c11dff9997b44a501ed6344ef053af51)