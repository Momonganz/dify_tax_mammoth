Payroll software vendors or AIS employers who are using an in-house payroll system/ software can refer to the AIS file format/ specifications to ensure that their software can submit files that comply with IRAS’ requirements via API.

On this page:

## File format/ specifications for YA 2025 submission

Existing payroll software vendors or AIS employers who have already integrated the AIS-API to their in-house payroll system/ software can refer to the following Year of Assessment (YA) 2025 file format/ specifications. Changes for YA 2025 are highlighted in orange fonts.

Note: There will be no onboarding of new payroll software vendors to the AIS-API based for the YA 2025 submission. This is in anticipation of the upcoming major enhancements to the AIS-API that IRAS will be implementing to provide better support for employers in meeting their submission obligations. These changes are scheduled to come into effect from 3Q 2025, in preparation for the YA 2026 submission. If you are interested to integrate with IRAS’ AIS-API for YA2026’s AIS submission, kindly complete this [form](https://go.gov.sg/aisreginterest). We will contact you once the onboarding activities for the YA 2026 submission commences.

Expand all

[**AIS Application Programming Interface (API) Service Specifications**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#ais-application-programming-interface--api--service-specifications)

- The server/ software/ application must be able to meet the pre-requisites to:
1. Support the following protocols: HTTP/2, TLS 1.2/1.3, and

2. Trigger HTTP/GET and HTTP/POST requests.
- The server/ software/ application must have a Callback URL to redirect users to the payroll software after Corppass login and consent. The Callback URL must use Fully Qualified Domain Name (FDQN), and meet all of the following requirements:


1. Must be able to accept parameters,

2. Must not contain IP address, port number, Hash (#) or Wildcard (\*) characters, and

3. Must not be the same URL for Sandbox and Production environments

| Supporting AIS-API on API Marketplace | Supporting AIS-API on APEX |
| --- | --- |
| **Supporting AIS-API on API Marketplace** [API Services Interface Specifications for CorpPass Authentication](https://www.iras.gov.sg/docs/default-source/default-document-library/api-services-interface-specifications-for-corppass-authentication.pdf?sfvrsn=d33d6c5f_3 "API Services Interface Specifications for CorpPass Authentication") (PDF, 580KB) | **Supporting AIS-API on APEX** [CorpPass Authentication - OAuth on APEX](https://go.gov.sg/oauthcorppassapex) |
| **Supporting AIS-API on API Marketplace** [APl Service Interface Specifications for "Submission of Employment Income Records (Corppass)"](https://www.iras.gov.sg/docs/default-source/default-document-library/apl-service-interface-specifications-for-submission-of-employment-income-records-(corppass)-.pdf?sfvrsn=d191519d_23 "APl Service Interface Specifications for ") (PDF, 374KB) | **Supporting AIS-API on APEX** [API Service Interface Specifications for “Submission of Employment Income Records (APEX)”](https://www.iras.gov.sg/media/docs/default-source/uploadedfiles/pdf/iras-submission-of-employment-income-(apex)-api-services-interface-specification.pdf?sfvrsn=77208cc8_4 "API Service Interface Specifications for “Submission of Employment Income Records (APEX)”") (PDF, 363KB) |
| **Supporting AIS-API on API Marketplace** [AIS (Corppass) API Onboarding Guide](https://go.gov.sg/iras-ais-corppass-onboarding) (PDF, 1.1MB) | **Supporting AIS-API on APEX** [APEX AIS API Onboarding Guide](https://go.gov.sg/apex-oauth) |
| **Supporting AIS-API on API Marketplace** [API Sandbox Portal](https://apisandbox.iras.gov.sg/iras/devportal/sb/) | **Supporting AIS-API on APEX** [APEX](https://api.apex.gov.sg/) |
| **Supporting AIS-API on API Marketplace** [API Production Portal](https://apiservices.iras.gov.sg/iras/devportal/) | **Supporting AIS-API on APEX** [FAQ on AIS-API Migration to APEX and Upcoming Activities](https://go.gov.sg/ais-api-migration-faq) (PDF, 264KB) |

[**Additional file format specifications**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#additional-file-format-specifications)

Your payroll system must be able to support at least one of the formats (TXT and/or XML). If your payroll system supports the XML format only, you may refer to the “specifications of TXT files for all forms” document as a reference for the
business rules that apply to the corresponding fields of the XML format.

| Supporting Text file format (.txt) | Supporting Extensible Markup Language file format (.xml) |
| --- | --- |
| **Supporting Text file format (.txt)** [Specifications of TXT files for all forms](https://www.iras.gov.sg/docs/default-source/default-document-library/specifications-of-txt-files-for-all-forms.zip?sfvrsn=a468c634_32 "Specifications of TXT files for all forms") (ZIP, 1.08MB) | **Supporting Extensible Markup Language file format (.xml)** [XML schema for all forms](https://www.iras.gov.sg/media/docs/default-source/uploadedfiles/zip/xml-schema-for-all-forms.zip?sfvrsn=76535a15_2 "XML schema for all forms") (ZIP, 18KB) |
| **Supporting Text file format (.txt)** [Sample TXT for all forms](https://www.iras.gov.sg/docs/default-source/default-document-library/sample-txt.zip?sfvrsn=51826248_17 "Sample TXT for all forms") (ZIP, 2KB) | **Supporting Extensible Markup Language file format (.xml)** [Sample XML for all forms](https://www.iras.gov.sg/docs/default-source/default-document-library/sample-xml.zip?sfvrsn=46586b63_17 "Sample XML for all forms") (ZIP, 7KB) |
| **Supporting Text file format (.txt)** [Additional specifications for both TXT and XML file formats](https://www.iras.gov.sg/docs/default-source/default-document-library/things-to-note-for-both-txt-and-xml.pdf?sfvrsn=3cac4216_21 "Additional specifications for both TXT and XML file formats") (PDF, 376KB) | **Supporting Extensible Markup Language file format (.xml)** [Additional specifications for both TXT and XML file formats](https://www.iras.gov.sg/docs/default-source/default-document-library/things-to-note-for-both-txt-and-xml.pdf?sfvrsn=3cac4216_21 "Additional specifications for both TXT and XML file formats") (PDF, 376KB) |
| **Supporting Text file format (.txt)** [List of recommended controls](https://www.iras.gov.sg/media/docs/default-source/uploadedfiles/pdf/types-of-controls-for-payroll-software.pdf?sfvrsn=a11b0a41_25 "List of recommended controls") (PDF, 140KB) | **Supporting Extensible Markup Language file format (.xml)** [List of recommended controls](https://www.iras.gov.sg/media/docs/default-source/uploadedfiles/pdf/types-of-controls-for-payroll-software.pdf?sfvrsn=a11b0a41_25 "List of recommended controls") (PDF, 140KB) |
| **Supporting Text file format (.txt)** [Country/Region, Citizenship and Bank code](https://www.iras.gov.sg/media/docs/default-source/uploadedfiles/pdf/country-region-citizenship-bank-codes.pdf?sfvrsn=b5fbaae1_20 "Country/Region, Citizenship and Bank code") (PDF, 134KB) | **Supporting Extensible Markup Language file format (.xml)** [Country/Region, Citizenship and Bank code](https://www.iras.gov.sg/media/docs/default-source/uploadedfiles/pdf/country-region-citizenship-bank-codes.pdf?sfvrsn=b5fbaae1_20 "Country/Region, Citizenship and Bank code") (PDF, 134KB) |

## \[NEW!\] Technical specifications for AIS-API 2.0

IRAS will be making enhancements to the AIS-API (‘AIS-API 2.0') to streamline the AIS submission process. With effect from 3Q 2025, AIS submissions must be made via AIS-API 2.0. Payroll software vendors or AIS employers who are using an in-house payroll software and would like to support/ submit employment records through API can refer to the [technical specifications “Submission of Employment Income Records 2.0 (AIS-API 2.0)”](https://go.gov.sg/aisapi20) to prepare your software.

The AIS-API 2.0 will be available for subscription and testing on [APEX](https://api.apex.gov.sg/) from 2Q2025. Developers are encouraged to commence onboarding to APEX now to familiarise with the platform.

There are major changes introduced in AIS-API 2.0. Existing payroll software vendors and AIS employers can refer to a summary of the key changes below:

Expand all

[**1\. Submission format**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#1--submission-format)

AIS-API 2.0 will be in REST JSON format. Your payroll software no longer needs to support the TXT or XML file formats.


[**2\. Submission size**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#2--submission-size)

The allowable submission size per API call will be increased to 2000 employee records regardless of Form Types, up from 800 records.


[**3\. Amendment Submission**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#3--amendment-submission)

A new option for amendment submission will be introduced to simplify the submission of amendment data: the Revised indicator.

This allows your payroll software to generate amendment records with revised data to overwrite previous submissions of the affected record(s).

[**4\. Back years records**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#4--back-years-records)

Submission for back years records will be increased to 4 back years, up from the current 2 back years.


[**5\. IR8A and Appendices**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#5--ir8a-and-appendices)

Submission of corresponding Appendix 8A and/or Appendix 8B forms will be required to be made in the same API call as the main IR8A form.


[**6\. IR8A**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#6--ir8a)

All amount fields will only accept value in Number (9).

- If decimals exist for income fields, to round down the amount to the nearest dollar.
- If decimals exist for deduction fields, to round up the amount to the nearest dollar.

The following data items will not be required:

- Citizenship
- Formatted Address (Block/ House No., Street name, Level No., Unit No., Postal Code)
- Cessation Provision Indicator
- Compensation for loss of office Indicator
- Gratuity/ Notice Pay/ Ex-gratia payment/ Others indicator
- Period of Gross Commission payment
- Commission Payment Type
- Breakdown for Allowances items: Transport, Entertainment and Others
- Approval obtained from IRAS for loss of office compensation
- Approval date on compensation for loss of office
- Pension (combine ‘Pension’ with ‘Retirement benefits’)


[**7\. Appendix IR8S**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#7--appendix-ir8s)

Form IR8S will not be required.

Please note that interest on refund of employee’s CPF contribution remains taxable. Any refund claim amount must be submitted under the item ‘Allowances’ in the IR8A form.

[**8\. Appendix 8A**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#8--appendix-8a)

The maximum number of accommodation records, for residences provided by the employer, allowed per employee will be increased to 10.

All amount fields will only accept values in Decimal (7,2) . If the total Benefits-in-kind amount contains decimals, drop the decimals when populating into the corresponding field in IR8A.

[**9\. Appendix 8B**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#9--appendix-8b)

The maximum number of Employee Equity-Based Remuneration Scheme (EEBR) records allowed per employee will be increased to 30, up from 15.

Number of shares, Exercise price and OMV per share at exercise date will only accept values in Decimal (9,5).

All the Gross Amount of Gains fields will only accept values in Decimal (9,2).

If the Total Gains and Profits amount from Share Options for S10(1)(b) and S10(1)(g) contain decimals, drop the decimals when populating the amount into the corresponding field in IR8A.

The following data items will not be required:

- Open Market Value Per Share as at the Date of Grant of ESOP/ESOW Plan
- Gross amount qualifying for income tax exemption for stock option plans under ERIS
- Gross amount not qualifying for tax exemption
- Date of Incorporation for ERIS (for start-up only)

The calculation of the gross amount of gains from ESOP/ESOW Plan will also be adjusted correspondingly.

To ensure that your payroll system meets all the requirements, please always refer to the Technical Specifications for Submission of Employment Income 2.0 (AIS-API 2.0) for the complete list of data items and validation rules.

For enquiries on the Technical File Format/ Specifications, email us at [data\_mgmt@iras.gov.sg](http://mailto:data_mgmt@iras.gov.sg/).

## FAQs

Expand all

[**Will there be changes to the technical file format when IRAS makes changes to the Form IR8A and/ or appendices?**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#will-there-be-changes-to-the-technical-file-format-when-iras-makes-changes-to-the-form-ir8a-and--or-appendices-)

Tax changes and new government initiatives may result in changes to the technical file format/ specifications. We will publish the changes on our website by Aug every year and inform all AIS payroll software vendors via email.

[**Are there any requirements for API integration?**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#are-there-any-requirements-for-api-integration-)

Yes, our API endpoints have to be triggered from a Server-to-Server connection. Your server/ software/ application must be able to:

1.  Support the following protocols: HTTP/2, TLS 1.2/1.3, and
2.  Trigger HTTP/GET and HTTP/POST requests.

A Callback URL is also required to redirect users to the payroll software after Corppass login and consent. The Callback URL must use Fully Qualified Domain Name (FDQN), and meet all of the following requirements:

1.  Must be able to accept parameters,
2.  Must not contain IP address, port number, Hash (#) or Wildcard (\*) characters, and
3.  Must not be the same URL for sandbox and production environments.

[**There are differences between the hardcopy forms and the requirements stated in the file format. Which template should I follow to customise the printouts from my software?**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#there-are-differences-between-the-hardcopy-forms-and-the-requirements-stated-in-the-file-format--which-template-should-i-follow-to-customise-the-printouts-from-my-software-)

Vendors should mimic the fields in the official copy of the income tax forms (https://go.gov.sg/iras-formir8a) to customise the printouts. The payroll software should be
able to capture these fields’ input based on the file format specifications, and generate the printout accordingly.

For clients who are in the Auto-Inclusion Scheme (AIS), the following statement must be displayed at the top header of the form(s):

_“This statement can only be issued by an employer in the Auto-Inclusion Scheme (AIS) and is for your retention. The information in this statement will be automatically included in your income tax return, so you need not declare them in your tax form. You can check if your employer is in the AIS at IRAS websi_ _te, https://go.gov.sg/iras-ais-search.”_

[**Why doesn't IRAS allow "overwriting" of previous submission when submitting amendment files?**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#why-doesn-t-iras-allow--overwriting--of-previous-submission-when-submitting-amendment-files-)

There are instances where the same company has more than one payroll system administrated by different departments or HR personnel as the nature of income is different. For such cases, the amount given in two different files should be added and not overwritten.

To avoid confusion to the filing of employment income details, changes to the amounts must be given as the difference.

[**Must the files be encrypted as a security feature?**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/technical-file-format-specifications#must-the-files-be-encrypted-as-a-security-feature-)

No. IRAS’ applications use the Secure Socket Layers (SSL) technology, which is the industry standard protocol for secure, web-based communications and transactions.  SSL creates a secure communication channel between the server and the consumer’s browser. SSL provides message privacy by encrypting all information exchanged between the web server and the consumer’s browser.

[Digital Services**Auto Inclusion Scheme (AIS) for Employment Income**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income)[Digital Services**Submit employment income records**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/submit-employment-income-records)[Digital Services**How to support AIS submission as a vendor**](https://www.iras.gov.sg/taxes/individual-income-tax/employers/auto-inclusion-scheme-(ais)-for-employment-income/how-to-support-ais-submission-as-a-vendor)