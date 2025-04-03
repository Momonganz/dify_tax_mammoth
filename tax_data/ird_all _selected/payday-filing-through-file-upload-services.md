[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Te tāpaetanga rā utu mā ngā ratonga tukuatu kōnae Payday filing through file upload services
============================================================================================

When payday filing through the myIR file upload service, employers must upload to us from their software:

*   employee information each pay cycle
*   details for new and departing employees. 

For more details on how to file
-------------------------------

[File employment information with file upload](/employing-staff/payday-filing/filing-employment-information-electronically/file-employment-information-in-myir-with-return-file-upload)

Payday filing business use cases  
----------------------------------

The following are examples of sequences of the myIR file upload service operations that could be used to achieve a specific business outcome.

#### Keys

*   Employee details:  Dep = Departing
*   The numbers for each use case are the order in which these operations should be called when using these services.

| Use case | Employee details |     |     | Employment information |     |
| --- | --- | --- | --- | --- | --- |
| New | Amend | Dep | File | Amend |
| --- | --- | --- | --- | --- | --- |
| 1\. First time employee - file employee details (including KiwiSaver enrolment), file employment information | 1   |     |     | 2   |     |
| 2\. New employee (existing KiwiSaver member) - file employee details, file employment information | 1   |     |     | 2   |     |
| 3\. Existing employee - file employment information on payday or within 2 days of payday | 1   |     |     | 2   |     |
| 4\. Existing employee - (opt out of KiwiSaver) file employee details, file employment information |     | 1   |     | 2   |     |
| 5\. Existing employee - amend previously filed employment information |     |     |     |     | 1   |
| 6\. Departing employee - file employee details, file employment information |     |     | 1   | 2   |     |

[Payday filing - myIR file upload business use cases 2019 (PDF 237KB) Download guide](/-/media/project/ir/home/documents/digital-service-providers/software-providers/payday-filing/payday-filing-myir-file-upload-services/payday-filing-myir-file-upload-business-use-cases.pdf?modified=20241106035654&modified=20241106035654)

[Payday Filing File Upload Specification 2025 V1.00 (PDF 951KB) Download document](/-/media/project/ir/home/documents/digital-service-providers/payday-filing-file-upload-specification-2025.pdf?modified=20241106034028&modified=20241106034028)

[Payday Software Developers Casebook July 2024\_2025 V1.2 (PDF 3MB) Download document](/-/media/project/ir/home/documents/digital-service-providers/payday-software-developers-casebook-july-2024.pdf?modified=20241106034037&modified=20241106034037)

Please note that access to technical documentation will be available only through the Gateway Customer Support Portal from 1 July 2025. Please register your organisation or login to Gateway Customer Support Portal for continuing access to technical documentation using the links below. 

Find out more about the calculations and business rules that support payday filing.

[Payroll calculations and business rules](/digital-service-providers/services-catalogue/returns-and-information/payday-filing/payroll-calculations-and-business-rules)

Express file transfer service
-----------------------------

The express file transfer service in myIR provides a place to drop all payday related files. This includes all versions of EI and ED.  The service allows zip files to be uploaded as long as all the files in the zip are employer related that meet our specifications.

The following employer files are supported:

*   File transfer Payday schedules: Upload multiple payday employment information schedules.
*   File transfer Payday amendments: Upload amendments to multiple payday employment information schedules.
*   File transfer employee details: Upload new and departing employee details.
*   Upload KiwiSaver file: Upload a KiwiSaver file to enrol multiple employees in KiwiSaver at the same time.
*   Upload compressed zip file: For this account upload one or more Non-payday or KiwiSaver files.
*   File transfer employer schedules: File transfer employer monthly schedules for multiple filing periods (IR348).
*   File transfer EMS amendments: Upload amendments to multiple employer monthly schedules (IR348).
*   File transfer employer deductions: Upload multiple employer deductions forms (IR345).

There is no test a file service for express file transfer. Individual files can be tested using the appropriate individual test a file service. The express file transfer service evaluates the files in the zip using the same validation as the individual test a file services, which can be found in the file specifications.

### For more details on how to file

[File employment information with express file transfer](/employing-staff/payday-filing/filing-employment-information-electronically/upload-employment-information-in-myir-with-express-file-transfer)

Multi-Payment Option (MPO)
--------------------------

The Multi-Payment Option (MPO) account at Inland Revenue allows tax preparers to submit a single payment that must be posted against multiple customers’ accounts.

The detailed specifications for MPO filing.

[Multi Payment Option File Upload Specification 2020 (PDF 197KB) Download guide](/-/media/project/ir/home/documents/digital-service-providers/file-upload-spec-mpo/multi-payment-option-file-upload-specification.pdf?modified=20240822021256&modified=20240822021256)

  

Testing and support for file upload services
--------------------------------------------

We provide support for development and testing of the payday filing myIR file upload services.

Please register your organisation in our gateway customer support portal to access support and to keep up to date with the latest release. Once registered you can request access to our Test a file services.

[Register your organisation for gateway services](https://gws.ird.govt.nz/gws?id=sn_user_registration&sys_id=c11dff9997b44a501ed6344ef053af51)

Alternatively, if you do not need support you can submit files to us to validate their compatibility with our payday filing specification. 

Select a file type to test:

#### Release 2021 tax year onwards

[Employee details (CSV format)](https://myir.ird.govt.nz/tools/?LINK=TSTEMP2)

[Employee details (Excel format)](https://myir.ird.govt.nz/tools/?LINK=TSTLNK)

[Employment information (CSV format)](https://myir.ird.govt.nz/tools/?LINK=PSOEI2TEST)

[Employment information amendment (CSV format)](https://myir.ird.govt.nz/tools/?LINK=PSOEIATEST2)

  

#### Release 2020 tax year 

[Employment information amendment (CSV format) R 2020](https://myir.ird.govt.nz/tools/?LINK=PSOEIATEST)

  

#### Payroll amendments - Pre-release 2020 tax year

[Multi-payment option (MPO) for schedular payments](https://myir.ird.govt.nz/tools/?LINK=MPOTEST)
 

[Employer deduction schedule (EDS) for payroll intermediaries](https://myir.ird.govt.nz/tools/?LINK=PSOEPSTEST)

[Amend employer schedules](https://myir.ird.govt.nz/tools/?LINK=PSOEASTEST)

[Payroll intermediary subsidy claim form (SCF)](https://myir.ird.govt.nz/tools/?LINK=PRSSCFTEST)

#### Tasks

*   [Getting started](/digital-service-providers/guides-and-docs/getting-started "Getting started")
    

#### Other Sites

*   [Log in to gateway customer support portal](https://gws.ird.govt.nz/gws)
    
*   [Register organisation for gateway services](https://gws.ird.govt.nz/gws?id=sn_user_registration&sys_id=c11dff9997b44a501ed6344ef053af51)