\[IN CONFIDENCE RELEASE EXTERNAL\] Inland Revenue Business Transformation Programme Data Conversion, Data Cleansing & Data Enrichment Approach Release 3 Prepared by: Data Lead – Business Data Stream Date: 6 July 2018 Page 2 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] About this Document This document explains the overall data conversion, data cleansing and data enrichment approach that will be taken for the conversion of data for Release 3 as approved by the Data Owners Forum. Document Control File Name and Path Contact Person Status Final Version 1.0 BT UiD 10825 Document Signoff Formal Review Area Name Signature Date Responsible person – work stream 1 Responsible person – work stream 2 Responsible people – work stream 3 Responsible person – work stream 4 Accountable Person The following people have supported the development of this document: The following people and groups have been consulted: Data Owners Forum The following people and groups have been informed of the development and completion of this document. Data Owners Forum Design Authority Transformation Executive Working Group Page 3 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] Contents 1 Executive Summary .............................................................................................. 5 2 Data Cleansing Approach ...................................................................................... 7 2.1 Introduction ..................................................................................................... 7 2.2 Roles and Responsibilities ................................................................................... 7 2.2.1 Business Data Stream Team roles .............................................................. 7 2.2.2 Business Data Stream Team Responsibilities ............................................... 7 2.2.2.1 Work stream 1 - Everyday BAU data cleansing carried out by CCSI and CCSB . 7 2.2.2.2 Work stream 2 – Known R3 data issues - data cleansing work carried out by CCSI, CCSB & IT&C .................................................................................. 8 2.2.2.3 Work stream 3 – Converted data cleansing activity ...................................... 8 2.2.2.4 Work stream 4 – Data Enrichment ............................................................. 9 2.2.3 Business Transformation Managers .......................................................... 10 2.2.4 Data Stewards ....................................................................................... 10 2.2.5 Business Stakeholders ............................................................................ 10 2.2.6 Data Owners Forum ............................................................................... 10 2.3 Data Cleansing Approach ................................................................................. 12 2.4 Process for Data Cleansing / Remediation for work stream 3 ................................ 12 2.5 Data Cleansing Guiding Principles ...................................................................... 13 2.6 Lessons Learned from Release 2 ....................................................................... 13 3 Data Conversion Methodology and Approach ...................................................... 14 3.1 Work stream 3 – Converted data cleansing activity .............................................. 14 3.2 Inventory Data Resources ................................................................................ 14 3.2.1 Creating the Inventory ........................................................................... 15 3.2.2 Review the Inventory for Integrity and Quality .......................................... 15 3.3 Data Purification ............................................................................................. 15 3.4 Detailed Conversion Plan .................................................................................. 16 3.4.1 Approach to Historic Data ....................................................................... 16 3.4.2 Types of Data to be converted ................................................................. 16 3.4.3 Establish a System of Record .................................................................. 16 3.4.4 Live vs. FIRST Reference ........................................................................ 16 3.4.5 Approach to Selection Criteria ................................................................. 17 3.4.5.1 Impact on Daily Operations ..................................................................... 17 3.4.5.2 Impact on Planned System Processes ....................................................... 17 3.4.5.3 Impact on Data Purification ..................................................................... 17 3.4.5.4 Impact on Cutover Timeline .................................................................... 17 3.4.6 Automatic vs. Manual Processes .............................................................. 17 3.4.7 Approach to Work in Progress.................................................................. 18 Page 4 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] 3.5 Conversion Process.......................................................................................... 18 3.5.1 Extract Data from FIRST Applications ....................................................... 18 3.5.2 Translation of Extracted Data from FIRST Applications ................................ 19 3.5.2.1 Mapping and Reformatting vs. Transforming Data ...................................... 19 3.5.2.2 Avoid Production Copies ......................................................................... 19 3.5.2.3 Reduce Risk by Reducing the Toolset ........................................................ 19 3.5.2.4 Leverage IR Expertise ............................................................................ 19 3.5.3 Loading Data into START ........................................................................ 19 3.5.3.1 Validate Transformed Data ...................................................................... 19 3.5.3.2 Customer is the logical Unit of Work ......................................................... 19 3.5.3.3 Use Standard Business Objects ................................................................ 19 3.5.3.4 Suspending Some Core Functionality ........................................................ 20 3.5.4 Reconciliation ........................................................................................ 20 3.5.4.1 FIRST Report ......................................................................................... 20 3.5.5 User Verification .................................................................................... 20 3.5.6 Mock Conversion Runs ............................................................................ 20 3. 5.7 Business Function Definitions .................................................................. 21 3.6 System Cutover .............................................................................................. 21 3.6.1 Cut-off for Processing Items in FIRST Systems .......................................... 21 3.6.2 FIRST Enters a Read-Only State .............................................................. 22 3.6.3 Final Conversion Process ......................................................................... 22 3.6.3.1 Suspend Maintenance ............................................................................. 22 3.6.4 Going live ............................................................................................. 22 4 Data Enrichment Approach ................................................................................. 22 5 Reporting ............................................................................................................ 23 Appendix A – Business Data Stream Team – The 4 Work streams ................................... 23 Appendix B – High Level Data Cleansing Plan/Timeline .................................................. 25 Appendix G – Definitions ........................................................................................... 26 Page 5 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] 1 Executive Summary The primary goal of the data conversion and cleansing approach is to deliver the data conversion and necessary data cleansing activities required to successfully deliver Release 3 and enable the realisation of benefits from the Business Transformation Programme. Three main issues are top of mind. They are: size – R3 is substantially larger than R1 or 2; complexity – this is significantly higher; and timeframe – ensure data is in an acceptable condition to enable a clean conversion from FIRST to START in April 2019. A successful Go Live will require a collaborative and coordinated approach to data cleansing across all of IR. We propose categorising the work into the following 4 work streams: 1. Everyday BAU Data cleansing carried out by CCSI and CCSB & IT&C 2. Known data issues - data cleansing work carried out by CCSI, CCSB & IT&C - driven by the Business Data Stream Team 3. Converted Data cleansing activity - driven by the Data Conversion Team 4. Data Enrichment to enable Transformation benefits realisation – driven by Business Lead, Data Enrichment Section 2 does contain some release 3 specific data issues as well as the general guidelines and approach for data cleansing for work streams 1 & 2. Section 3 is not release specific. It contains the general guidelines and principles of the conversion methodology and approach for work stream 3. It is not intended to identify release specific risks or data quality issues. Section 4 is new for Release 3 and contains high level general guidelines and principles of our approach to data enrichment which are still being developed. At this early stage the known data issues that have been prioritised as “Must Do”, “Should Do” and “Could Do” in the 4 work streams number as shown here: Key “Must Do” – critical for current delivery timeframe. “Should Do” – important, we will attempt to deliver as many as possible in the current timeframe. “Could Do” – desirable but not necessary for conversion. “Won’t Do” – least critical and not appropriate at this time. Currently there are no issues in this category but it may be that decisions are required at the CIR/ELT decision checkpoints proposed in the high level action plan to move issues into this category. Page 6 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] Transparency of the state of data issues will be vital at the Commissioner and Executive Leadership levels to enable important conversations and making difficult decisions such as moving issues into the “won’t do” category. At the same time a decision would need to be made on how to manage those issues once they are converted to START so that START does not inherit issues from FIRST that are then not resolved. To enable that the following high level action plan is proposed: Successful delivery of these work streams requires a partnership approach with support given at a Deputy Commissioner level as well as at Customer Segment Lead, Segment Management Lead, Group Lead and Team Lead levels across CCSI, CCSB & IT&C. A single point of visibility and governance for all data issues is a necessity. To enable this we recommend the following communication/reporting approach: Page 7 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] 2 Data Cleansing Approach The accountability for Data Cleansing is with the Business Data Stream Team. 2.1 Introduction This section of the document outlines the Data Cleansing Approach for Release 3 . It describes the processes and activities as well as the high level timeline for Data Cleansing. It sets out the roles, responsibilities for Data Cleansing Release 3 including the role of the Data Owners Forum. For key decision points and activities see the high level action plan in the Executive Summary and Appendix F for more details. 2.2 Roles and Responsibilities 2.2.1 Business Data Stream Team roles The Business Data Stream Team is financed by the Business Deployment Work stream and reports to the Chair of Data Owners Forum. T his group works closely with the FAST Data Conversion Team on work stream 3 to ensure that IRs data is in the best position, i.e. valid and remediated, for conversion and implementation of BT Release 3. The Business Data Stream Team is made up of a Project Manager/Data Lead and three Data Remediation Analysts seconded into the team, plus a further seven Data Remediation Officers on assignment from CCSI/CCSB to work on work stream 3 data issues. The number of Data Remediation Officers will be reviewed and adjusted if required in December 2018. The timeframe for achieving this is outlined in Appendix F the Data Cleansing Plan. Data needs to be managed from an IR wide perspective with a single point of contact. The Business Data Stream Team provides a connection between Data Owners Forum and CCSI, CCSB & IT&C. This ensures transparency and provides a channel for Data Owners Forum to advise and give direction on the appropriateness of on data cleansing activities underway. For more details see the proposed reporting and communications pathway in the Executive Summary and Appendix A. 2.2.2 Business Data Stream Team Responsibilities The Business Data Stream Team is responsible for the following streams of work: 2.2.2.1 Work stream 1 - Everyday BAU data cleansing carried out by CCSI and CCSB The Business Data Stream Team holds the following responsibilities in relation to this Work stream: • Monitor the progress of this everyday work that has an impact on conversion (i.e. must do’s) in order to provide visibility of all data cleansing activities to Data Owners Forum. • Communicate deadlines and restrictions on bulk BAU data cleansing work driven by the BT Release 3 Data Conversion Plan in conjunction with the Deployment Team to CCSI and CCSB by way of intranet news items and People Leaders updates. • NOTE: While it may be preferable that the bulk of this work is completed prior to the first Mock Go Live in November 2018, this BAU work will in reality continue right up to go-live. Page 8 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] • Receive data remediation work from BT (either from the BTMs/SMEs or from the FAST Data Conversion Team). This will then be channelled into the appropriate work stream depending on the effort/skills required. • Where possible identify any impacts on successful Release 3 conversion as result of BAU data cleansing activities. Raise these issues promptly with Data Owners Forum, and the FAST Data Conversion Team. • Inform CCSI, CCSB and IT&C of BAU data cleansing work regarding any decisions made by Data Owners Forum relating to their data cleansing work. 2.2.2.2 Work stream 2 – Known R3 data issues - data cleansing work carried out by CCSI, CCSB & IT&C The Business Data Stream Team holds the following responsibilities in relation to this Work stream: • Identify data cleansing work that falls into this work stream. Develop solutions and size the issues. • Access resources within CCSI and CCSB to complete pieces of data cleansing work. Ensure that business impact statements (e.g. time and people requirements) are undertaken by the Capabilities & Outcomes workflow team as required to enable this. • Access people and resources from within IT and BPS should a technology solution be required to cleanse data in FIRST as required. • Ensure that legal and policy implications are determined as required. • Utilising existing automation frameworks such as Business Systems Imperatives and Events (a team within the Capability & Outcomes, Customer & Compliance Services – Individuals Group) processes where applicable for agreed automation opportunities for remediation and data quality issues • Collaborate with CCSI, CCSB and IT&C regarding work to be completed by their teams • Plan and monitor progress, reporting back to Data Owners Forum. This includes raising any issues and risks that may require their intervention. • Communicate deadlines and restrictions on bulk BAU data cleansing work driven by the BT Release 3 Data Conversion Plan to CCSI and CCSB by way of intranet news items and People Leaders updates. • Receive data remediation work from BT (either from the BTMs/SMEs or from the FAST Data Conversion Team). This will then be channelled into Work streams 1, 2, 3 or 4 depending on the effort/skills required. • Identify any impacts on successful Release 3 conversion as result of BAU data cleansing activities. Raise these issues promptly with Data Owners Forum, and the FAST Data Conversion Team. 2.2.2.3 Work stream 3 – Converted data cleansing activity The schedule for this work stream is planned and managed by the Data Conversion Team. See section 2.1 for more details. Page 9 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] The Business Data Stream team is responsible for: • Administer converted data verification exercises. • Manage verifiers with support from the FAST Data Conversion Team • Oversee Customer Data Verification by BST Testers and re-verification of any exceptions logged • Review verification exceptions with support from FAST Data Conversion Team and CT&SP BTMs and SMEs, these exceptions may lead to identification of new data remediation • Provide input into changes to the conversion plan and follow on changes to the cleansing plan • Provide additional training for the verifiers • Implement changes and corrections to the conversion process. • START design changes in conjunction with BT SME’s • Manage the Data Quality Register in \[Information redacted\] • Identify and raise data remediation work with CCSI, CCSB & IT&C Units that requires manual intervention to ensure that the data is in the best condition possible to enable conversion to START. This will then be channelled into Work streams 1 or 2 depending on the effort/skills required. • Utilising existing automation frameworks such as Automation Team, Business Systems Imperatives and Events (a team within the Capability & Outcomes, Customer & Compliance Services – Individuals Group) processes where applicable for agreed automation opportunities for remediation and data quality issues • Access/engage appropriately skilled people and resources should a technology solution be required to cleanse data in FIRST (e.g. IT/BPS or a BSI project team). • Perform or oversee data remediation as identified as part of Work stream 3. • Select data to be remediated • Allocate and manage work given to data remediation officers • Review/Track remediated data issues • Log decisions made by the Business Data Stream Team ensuring a robust audit trail is in place • Coordinate a legal view to any data issues needed to be fixed, including any documentation to gain approval • Receive data remediation work from BT (either from the BTMs/SMEs or from the FAST Data Conversion Team). This will then be channelled into Work streams 1, 2, 3 or 4 depending on the effort/skills required. • Plan and monitor progress, reporting back to the START data conversion team and Data Owners Forum. This includes raising any issues and risks that may require their intervention. 2.2.2.4 Work stream 4 – Data Enrichment Page 10 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] The Business Data Stream Team collaborates with the Business Lead, Data Enrichment. See section 4 for more details. (For detailed descriptions for the known issues at the time this document was finalised see Appendix B) 2.2.3 Business Transformation Managers Business Transformation Managers (BTMs) are responsible for the management of data elements, data objects and processes, for both content and metadata within their Jellybean. The 11 Tax and Social Policy Jellybeans are: Customer, Compliance, Financials, Revenue Accounting, Disbursements, Payments, Contact Centre/Voice Channel, Audit/Case, Analytics, Returns & Forms and eServices. The 2 Tax and Social Policy products are: INC, FAM, and the 2 main Channels are Voice Channel and eServices. These spread across the 11 Jellybeans ensuring a joined up approach. BTMs take an enterprise view and have a specialist role that incorporates processes, policies, guidelines and responsibilities for administering IR’s data in compliance with policy and/or regulatory obligations. The role of the BTMs in relation to Data Cleansing is to provide specialist knowledge via subject matter experts for thorough remediation analysis, prioritisation and recommendations to the Data Owners Forum. Refer to Appendix C for details of the BTMs for Release 3. 2.2.4 Data Stewards Data Stewards are responsible for the management of data elements, data objects and processes, for both content and metadata within CCSI & CCSB. Data stewards take an enterprise view and have a specialist role that incorporates processes, policies, guidelines and responsibilities for administering IR’s data in compliance with policy and/or regulatory obligations. The role of the Data Stewards in relation to Data Cleansing is to provide specialist knowledge for thorough remediation analysis, prioritisation and recommendations to the Data Owners Forum. 2.2.5 Business Stakeholders For Release 3 a more collaborative approach across all of IR is proposed. Improved transparency of this work is required to enable Data Owners Forum to be able to give advice and guidance on the best use of our limited resources in the time available. Business stakeholders are the people leaders responsible for directing any data cleansing BAU work within CCSI & CCSB that falls into work streams 1 and 2. The point of contact between the Business stakeholders and Data Owners Forum is the Business Data Stream Team. 2.2.6 Data Owners Forum The role of the Data Owners Forum is to own the business process (for data) across IR to ensure known data issues are incorporated into the Business Transformation solutions and includes: • Validate the conversion plan and act as an escalation point for conversion decisions as part of Work stream 3 • Validate all recommendations and prioritisation of work that are to be managed or undertaken via the Business Data Stream Team Page 11 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] • Validate all data work, including management of BAU work, historical data and PICT problems (also known as user system support problems) as part of Work streams 1 and 2 • Act as an escalation point for data quality issues raised by the Business Data Stream Team on all 3 Work streams. • Validate all proposed Data Enrichment work – to ensure all proposed work is appropriately prioritised and manager effectively to align with the delivery of Business Transformation benefits and customer outcomes. The responsibilities of the Data Owners Forum are: • Represent a wide range of Inland Revenue’s business functions, act as advocates of the desired IR culture and will be the channel in and out of the business. • Ensure all relevant and appropriate decisions are escalated for endorsement and/or approval by the Business Transformation Design Authority and/or the Business Transformation Executive Working Committee. The membership of the Data Owners Forum is: Data Owners Forum Chair Customer Segment Lead, Small & Medium Enterprises Members Programme Director (Deputy Chair) Business Transformation Lead Programme Manager, Release 3 Enterprise Architect - Transformation Lead Group Lead, Individuals Customer Segment Director Corporate Finance START Project Manager Technology Lead, Heritage Change Lead, Organisational Change Management Guests as required Tax on Income Lead Families Lead Programme Manager, Intelligence Led Director, Digital Change Programme Manager, Release 4 ESS contact – (if required) Attendees & presenters Data Stream Lead, Business Data Stream Data Enrichment Lead FAST Consultant, Project Management Forum Co- ordinator Governance co-o rdinator, BT PMO Page 12 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] 2.3 Data Cleansing Approach Many of the data issues will require cleansing prior to the Release 3 conversion. However, due to current system limitations in FIRST it might be more feasible to resolve some issues post conversion for Release 3 (e.g. historical or broken data not required in START). 2.4 Process for Data Cleansing / Remediation for work stream 3 Data conversion cleansing requirements are identified via the BTM’s and the FAST Data Conversion Team and logged in \[Information redacted\] Guided by the Data Conversion Approach (this document Section 1), the Conversion Plan, and the BTM’s and START, the scope of the Data Quality Register items with priority sufficient to be cleansed will only include data required to enable Release 3 conversion and implementation. The prioritisation of work is done in consultation with START, BTM’s and the SME’s with endorsement or approval (as required) by the Data Owners Forum. The main purpose of cleansing / remediation is to action data where specific intervention is necessary to provide START with the data it needs to continue operations. Data Extraction and Verification occurs periodically which identify further data issues for prioritisation. Where data sets are identified and where action is required manual data remediation will be considered; however manual remediation is not the primary option. Any automation or programmatic options for cleansing will be considered first. All data deemed as requiring remediation is given a problem statement and if required undertakes data remediation analysis. Page 13 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] The outcome of this analysis can be a recommendation to action or accept. Should data be accepted in its current form, then that data may convert to START in the current form (with no remediation). Where the analysis recommends action – then this data is purified by priority. To take some data sets to an outcome will require legal and policy considerations and appropriately delegated decision making. Recommendations are taken to the Data Owners Forum to ensure that appropriate legal, policy and decision making has been applied. Also it is likely that data quality issues with a low priority may not be remediated. 2.5 Data Cleansing Guiding Principles Approved by PGB April 17 for Release 2, the same principles will be applied for Release 3. A plan will be developed in conjunction with FAST for how Inland Revenue will manage manual data cleansing and validation that is in scope for Release 3 using existing standards. We will use existing practices to address data anomalies leveraging current delegations and escalation processes. A process, including appropriate escalation to manage data issues that cannot be mutually agreed to ensure effective and timely resolution will be developed. Business data will be managed in a structured way using the correct delegations and ownership. Standards already agreed across Inland Revenue will be used – however the Data Owners Forum will recommend practical changes if needed. Ensure that there is an agreed approach that can be consistently applied in Release 3 including identification of long term data issues Inland Revenue needs to address. Ensure that early consideration of the impacts of Release 3 Income tax changes on Release 3 deployment are made to ensure Social Policy products are not compromised. Will continue using the Data Business Owner Forum to gather business input and agree decisions when required. Will consider the Strategic Governance inputs recognising Organisation Design and programme and business requirements, to ensure the right decisions are made at the right time in relation to data. 2.6 Lessons Learned from Release 2 Release 2 data conversion identified many successful approaches for dealing with data and it would be practical to use the same or similar methods for Release 3 . The lessons learned during Release 2 and the actions taken against them are shown below: JIRA Ref Description Actions Taken Status BTLL-307 Collaboration between the Business Data Stream Team and FAST Conversion Team. This was a “what went well” lesson so no action required. Closed BTLL-308 DataBOF as a governance group. This was a “what went well” lesson so no action required. Note: the Data Owners Forum is a reporting group rather than a governance group. Closed BTL-359 Time consuming and complicated administration tasks for setting up conversion verification. The Data Stream Lead has met with the FAST Project Manager responsible for the process and organised a fix for this for R3 – they will send through a list of who In Progress Page 14 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] the testers are for the following week to our team by COP Friday. BTL-360 Earlier identification and allocation of data cleansing of issues as BAU work as part of work stream 2 is required. The Business Data Stream team are actively considering and managing these during their weekly team meetings. In Progress BTL-362 Changing reporting requirements for various governance Group A new format consolidated view for the Data Owners Forum has been tabled and is now being updated based on their feedback. PMO have confirmed their reporting requirements for Release 3. The Business Data Stream Team will report on work stream 2. The START Conversion Team already reports on work stream 3. In Progress BTL-363 Data cleansing work being carried out as BAU - Collaboration between the Business Data Stream Team and the Business on data cleansing work being carried out as BAU as part of work stream 1. The Data Stream Lead is developing a regular coms plan to enable this. In Progress BTL-364 Data Conversion Plan - Conversion rules should be run past Heritage IT as things change. During R2 when the Heritage IT team asked to see the conversion rules they encountered push back. This has been logged as risk BTBTR- 4332. For R3 the recommendation is that the conversion rules be shared with the Heritage IT team so that they can help identify any gaps so that we avoid unnecessary post conversion issues. Open 3 Data Conversion Methodology and Approach This section of the document focuses on principals and guidelines that makeup the methodology for converting data into START. Its contents were delivered during stage 1 of BT and are intended to be independent of any one release or stage of the programme. The accountability for Data Conversion is with the FAST Data Conversion Team. 3.1 Work stream 3 – Converted data cleansing activity The data cleansing work that is generated by the mock conversion and mock go live exercises is driven by the FAST Data Conversion Team and supported by the Business Data Stream Team. The FAST Data Conversion Team is responsible for: • Planning and managing the data conversion schedule. • Identifying data issues that require remediation in conjunction with the BTM’s. • Identify work required to be remediated as part of Work streams 1, 2 and 3 • Providing technical support for the Data Quality Register in FCR • Identify and analyse issues and incidents requiring urgent remediation. For details of the cross-over responsibilities with the Business Data Stream Team on this work stream see section 2.2.2.3 3.2 Inventory Data Resources The first task in the conversion process is to identify and inventory all of the possible FIRST data sources. Other conversion activities typically cannot be started until this inventory has Page 15 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] been created. The inventory will define the scope of customer data that is available for conversion. 3.2.1 Creating the Inventory In addition to identifying sources of data for potential conversion, i nformation useful for further actions should be collected. This information will include but will not be limited to: • Types of information such registration or financial information • Inland Revenue personnel such as subject matter experts with expertise regarding specific data • Technology and platforms used for data storage. This task will be done for each rollout, e ach iteration will produce a separate document. 3.2.2 Review the Inventory for Integrity and Quality Once the inventory has been created and other conversion activities can continue, each data source should be examined for integrity and the quality of its data. This process should seek to determine if the data in the resource is consistent, reliable, and complete. This process will require the conversion team to be granted access to the resources inventoried. If granting access requires a protracted process and an extended amount of time then it may be necessary to include others in the conversion team who currently have access. 3.3 Data Purification FIRST application data will be analysed prior to and during the conversion process, and corrected within the FIRST application prior to START conversion. Wherever possible, existing on -line and batch facilities provided by the FIRST applications will be used to make the data corrections in the source environments. The FAST Data Conversion Team will identify the corrections to be made in order for the data to be compatible with START. The FAST Data Conversion Team is responsible for developing the approach to “filling in the blanks” and setting defaults when START requires data that does not exist in the FIRST data stores. Correction should occur within the FIRST applications prior to START conversion. Corrections should not take place in backups, or any other auxiliary replicas of the production data. Nor should data be corrected as it is extracted from the FIRST systems for conversion to START. Ensuring that the data is cleansed in the FIRST application prior to conversion will allow the conversion process to be reconciled and users to verify that the conversion was correct and accurate. It may not be possible to resolve all issues identified in the FIRST data. For example this could occur if there is not functionality available in the FIRST system to resolve the issue, there are not enough resources available, there is insufficient time to address the issue, or legislation prohibits it. It is recommended that data purification begin as early as possible once issues are identified in order to allow sufficient time for data corrections. If it is not possible to correct an issue before conversion, an analysis of the impact should be conducted and risks associated with the issue identified. In addition, each issue should include a plan in order to mitigate the impact of unresolved data issues post conversion. Some of the solutions used to address FIRST data issues will include: • The FIRST selection criteria will be adjusted to exclude the data (where appropriate) • Use the “Do Not Convert” list to isolate undesirable data. This list is compiled over time; each category is reviewed by the Business Data Stream Team and signed off by a Core Business Transformation Manager (BTM). Page 16 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] • Post-conversion manual cleansing in START, which can be implemented during cutover or provided as work lists for cleansing at a later date • Indicators can be added at the customer, account, or period level to modify system behaviour post conversion. • Data can be manually converted 3.4 Detailed Conversion Plan For each rollout a specific plan of what will be converted will be created and appended to this document. The conversion plan will be stored in the \[Information redacted\] delivery workbench as definition items. These plans will detail all aspects of conversion including: • The types of data that will be converted • The source systems of that data How that data will be converted How much of the data will be converted. The FAST Data Conversion Team Lead is responsible for developing the detailed conversion plan. The decisions made in these plans will be based on the following principles. 3.4.1 Approach to Historic Data Only current, active information will be converted. For example, the history of a customer’s mailing address changes over time will not be converted; the conversion process will provide START with only a customer’s most recent address. 3.4.2 Types of Data to be converted It is helpful to group the types of data to be converted. The conversion plan will include the following groups by default, and additional groups will be added as necessary. Registration – This will include customer, location, and account demographic information like names, addresses, contacts, etc. Financial – This will describe how financial information will be converted, typically a system of record will be identified for period level balances and an other for the individual transactions inside that period. This section will typically include returns / filings, payments, and disbursements. Enforcements – This outlines the activities around compliance which usually includes collections, securities, payment plans, etc. Content – This outlines the approach that will be followed in regard to non-structured data such as images and correspondence. This information is not always converted into START but may be converted to another system or left where it is. 3.4.3 Establish a System of Record Depending on the FIRST environment, data may be stored in multiple systems. In that situation a system of record needs to be established for each type of data. For example both the registration and collections systems may contain names and addresses, and this begs the question of which system should be used as the master for this information. In this situation the quality and completeness of the both systems along with business direction should determine which system is the system of record. 3.4.4 Live vs. FIRST Reference Page 17 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] Not all FIRST data should be converted to live data in START. Many aspects of FIRST data may not be required for START operations, but may be needed for users to do the research needed and an integral part of their daily tasks. Consequently, data will be converted into one of the two following formats: Live \*(operational): This is the FIRST data START will need on an on -going basis for things such as tax return amendments, collections of unpaid balances, revenue accounting, and issuing correspondence. The conversion plan primarily deals with the conversion of operational data. Legacy Data: This is FIRST data typically not used in daily START processing but which is available to START and users to view. Legacy data can assist users by providing a more complete picture of the data as it existed in the FIRST systems. Legacy data structure design will typically parallel the structure of the data in the FIRST systems. 3.4.5 Approach to Selection Criteria It is important to clearly define which data is required to be converted into the START operational database. A realistic scope of the amount of data to convert will be developed, and this scope is referred to as the ‘selection criteria’. Selection criteria will be developed for different categories of data which at a minimum will include periods, accounts, and customers. A separate set of selection criteria will be created for each data category and it is these selection criteria that will determine how much of each category will be converted. The following principles should be observed when developing selection criteria: 3.4.5.1 Impact on Daily Operations Selection criteria should be developed to support important administrative activities. Converted data will be used primarily for processing amended returns, posting payments to the correct debt, and audit, billing, and collection activities. Consequently selection criteria should identify data in both scope and breadth that will support these (and other important) activities. Additionally, s tatistical information regarding the use of historical data with respect to these activities should be used to narrowly focus the selection of data. 3.4.5.2 Impact on Planned System Processes Converted data must be sufficient to support planned systematic processes. For example, if the process for calculating penalty requires payment information over the last 24 months, then this must be taken into consideration when defining the scope of period information for conversion. 3.4.5.3 Impact on Data Purification Because data quality typically declines with age, age should be a consideration when defining selection criteria. The decision to convert older data will increase the effort required to achieve minimum quality standards. 3.4.5.4 Impact on Cutover Timeline Converting more data will take longer to achieve. Because conversion is performed in a “Big Bang” fashion where all data is cutover to the new system during a shutdown period the decision to convert more data will impact the amount of time required to perform overall conversion during that shutdown period. Often the difficulty will be that the amount of time required will not be determined until the mock run process has progressed in include to all data, full mock which will occur much after selection criteria needs to be decided. 3.4.6 Automatic vs. Manual Processes Page 18 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] Where appropriate, the conversion plan will call for the use of START on -line functionality to manually convert small amounts of data. These decisions will be driven by data volumes, the complexity of the manual task, and the resources of developing, testing, and maintaining automatic conversion processes. In some cases a manual conversion process will be more appropriate, less error-prone, and more efficient, than developing and testing a one-time-use conversion program to convert a small number of items. 3.4.7 Approach to Work in Progress Work that is still in progress at the time of conversion should not be brought into START. This therefore will be a key task that should be completed prior to cutover. 3.5 Conversion Process The standard START conversion process entails Obtaining data extracts from the FIRST systems. Translation of data extracted from FIRST systems to be loaded into START. Data loads into START via business objects tailored for Inland Revenue business needs. Reconciliation of data converted to START. User verification and testing of data when it arrives in START. Data purification in the source system. 3.5.1 Extract Data from FIRST Applications Necessary data from the applicable FIRST applications will need to be made available to the START conversion environment. This data must come from the production system and must fully represent the FIRST application data. This data is then translated to tables used to load the data into START. Inland Revenue (IR) is responsible for facilitating the conversion team with access of this data. How data will be accessed from the primary FIRST system, FIRST on the mainframe, has already been determined. IR has contracted with the mainframe support vendor, to use a technology named DataBridge to create SQL Server clone of all data in the OLTP and ARCHIVE databases on the FIRST production mainframe. This data is made available to the START conversion environment through SQL Server log shipping allowing the conversion team to control how frequency updates are applied to the START conversion environment copy of the FIRST data. START FIRST Systems START Conversion Database Selection Criteria and Translation Reconciliation START FIRST Apps Purification Verification Conversion Load Page 19 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] Access to other FIRST system will be made by SQL connections as well as flat file extracts. 3.5.2 Translation of Extracted Data from FIRST Applications Data will be translated from data extracts of FIRST systems into various tables used to load the data into START. The conversion team is responsible for creating and running the translation process. START jobs and SQL files will be heavily used by the conversion team in the translation process. Separate formats will be developed for most record types, such as Account and Financial records. The extraction process will be a ‘big bang’ that will extract data in one relatively short, well-defined procedure. T he following key principles will be observed. 3.5.2.1 Mapping and Reformatting vs. Transforming Data While it will be necessary to perform mapping and reformatting in the extraction process it should be done in a way that does not meaningfully alter the data. Meaningfully altering data during the extraction process will lead to reconciliation issues and impede the ability to verify that the process is comprehensive and accurate. 3.5.2.2 Avoid Production Copies Data should be extracted from production systems, rather than backups or other copies such as a Quality system. 3.5.2.3 Reduce Risk by Reducing the Toolset Only the tools necessary to execute a standard conversion should be used. START includes out of the box conversion utilities, and extensions to these utilities will also be developed on site as necessary. This tool set is necessary and sufficient for running and managing the entire conversion process from end to end, from extraction to load. 3.5.2.4 Leverage IR Expertise Knowledgeable and experienced IR staff, experienced with the technical and business aspects of FIRST data, will be leveraged to create conversion extract and translation processes. 3.5.3 Loading Data into START 3.5.3.1 Validate Transformed Data Before data is loaded into START a series of checks will be performed on that data. While some of these checks could also be done during extraction and translation they should be performed directly before data is converted into START. These checks will include: A systematic search for orphaned records and missing details Initial reconciliation to selection criteria tables and FIRST report Verification of metadata such as Business Industry Codes match those maintained in START 3.5.3.2 Customer is the logical Unit of Work Data will be converted into START on a per-customer basis, and all data for a single customer will be converted in a single transaction. This means that a customer will not be converted unless all of the data associated with that customer can be loaded without error (an error will result in a rollback). This prevents the introduction of incomplete data into START, enables detailed reporting on conversion exceptions, and enables multiple customers to be loaded concurrently without interference from exceptions thrown by other customer records. 3.5.3.3 Use Standard Business Objects Page 20 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] Extracted data will be converted into START using START business objects; including several fit for purpose extension built specifically for IR. T hese are typically the same business objects that START runs during normal activity. This ensures that START w ill be able to process non- native data without exception and also provides consistency between converted and native START data. 3.5.3.4 Suspending Some Core Functionality As stated above, converted data will be created primarily using the same business objects and configuration employed for processing native data. Automatic system notes can be suppressed since all ids, names, and addresses will be added by the conversion process. These changes will be effective only during the conversion process and will not affect any other START processing. 3.5.4 Reconciliation Reconciliation is a critical part of the conversion process. It ensures the relevant data was extracted from the FIRST systems and converted into START. The major steps include: Reconciliation of extracted data to the data loaded into START through the conversion process. Reconciliation of the data converted into START with independent FIRST reports of the applicable data in FIRST systems. 3.5.4.1 FIRST R eport A FIRST report will be used in the reconciliation process to ensure that the correct data was converted. This report should be generated independently of the conversion team and should be as simple and direct as possible. Removing complexity from the report will reduce the risk of not reconciling because of invalid logic built into the report. Where available an existing well established report should be used. The FIRST report should include, at minimum, non-nil balance periods by individual period. This granularity is necessary to help identify and reconcile any possible discrepancies. 3.5.5 User Verification While computer-based reconciliation of data extracted and loaded into START is necessary, it is insufficient to verify an accurate conversion. During user verification of converted data, knowledgeable users will view converted data in START and compare it to how it appears and is used in the FIRST applications. This stage will greatly increase the confidence in the conversion process and can identify, for instance, incidents of data elements being converted into the wrong field on a return. As users identify issues with the converted data those issues will be logged and triaged and may lead to changes in the conversion plan. It is typical to find issues that will lead to changes in: • Data purification • Training • START Development. 3.5.6 Mock Conversion Runs NOTE: This section addresses mock conversion runs not Mock Go-Lives. Mock conversion runs occur much more frequently and occur much earlier than Mock Go-Lives. Page 21 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] Because the conversion process will be a one-time use, it must be tested and trusted. To provide that high degree of trust a series of iterative mock conversions will be completed. A mock conversion, sometimes referred to as a mock run or dry run, will test the conversion process by performing the same steps as will occur during the final live conversion. Mock conversions will include extraction, translation, conversion, reconciliation, and user verification. Mock conversion runs will be executed iteratively and start as partial mock conversion runs and slowly ramp up to full mock conversion runs. A partial mock conversion run lacks either some type of data to be converted or uses limited selection criteria. A full mock conversion run contains all types of data and all data available. Successive mock conversion runs will increase the breadth and/or depth of FIRST data in “step” fashion as START configuration for each step becomes more advanced. For example some steps will include: • Customer level data • Customer and Account level data • Customer, Accounts, and Period level data • Customer, Accounts, Period, and Collection data. • It is important that mock conversion runs use, as close as possible, the actual steps, data, infrastructure, and users that will be involved in the final conversion. This will confirm that the conversion process is accurate, complete, and efficient. Mock conversion runs will verify the following: • The steps in the conversion process are correct and in the proper order • Data is being converted correctly • Assumptions regarding data volumes • The timing of conversion events including but not limited to: • Length of time required for the final full conversion is run • Pre-conversion and post conversion batch jobs in START • Sequencing of reconciliation tasks. • The adequate allocation of hardware resources for conversion. 3.5.7 Business Function Definitions During conversion process another key document is used that records key Business Function Definitions. In summary these definitions provide configuration specifications of how data is selected, designed and converted for START. These are assigned and defined by relevant Core Subject Matter Experts, designed by FAST Developers and approved by relevant BT Manager. It also provides foundation of various Business System Testing scenarios. The log of approved definitions is regularly provided to Data Owners Forum for review and confirmation. 3.6 System Cutover 3.6.1 Cut-off for Processing Items in FIRST Systems To allow functionality to be cutover from the FIRST applications to START, a number of activities will be stopped, started, or altered. The System Cutover plan will detail the required activities and associated schedules and process owners and responsible staff. These activities are managed by the deployment team. The Conversion Team will be responsible for the Page 22 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] automatic conversion set of activities and the Data Cleansing Team will be responsible for manual conversion and data cleansing activates. A point in time will be identified after which no new data should be processed in the FIRST applications. Common examples of these activities include: • Payment batch uploads • Return batch uploads • Disbursement / refund processing. • Other FIRST processes may have to be run one final time before that functionality can be performed in START, such as: • Closure of revenue accounting time period • Various month-end, year-end, period-end processing. This may include running annual and semi-annual reports where data from FIRST and START will be required to generate a summary report. 3.6.2 FIRST Enters a Read-Only State Once the conversion extract process has been initiated, no new activity or data should be entered in the FIRST systems. Access to FIRST applications during this time will be limited to read-only and might be unavailable due to impacts from the cutover process. Once data is being extracted for conversion to START the FIRST system should be set to “read only” for the products affected by that rollout in order to prevent users from performing work, such as new registrations or financial updates, that could have a detrimental effect on data conversion. Putting FIRST into a read-only state may require FIRST system programming changes. Such changes include, but are not limited to: Modifying FIRST on -line functionality to prevent users from modifying converted accounts Modifying FIRST off -line or batch functionality to prevent the FIRST system from automatically processing converted accounts. 3.6.3 Final Conversion Process This will be the culmination of all efforts in the conversion process. The final conversion run will be managed and monitored using a detailed conversion checklist. Due to repeated full mocks acting as rehearsals leading up to conversion, the exact sequencing and time requirements for every item on the checklist will be known. In addition, the final reconciliation reports will be similar to those produced during the final full mock conversion. 3.6.3.1 Suspend Maintenance Due to conversion activity, non-critical hardware or software updates should not occur in either FIRST or START environments during the final conversion. Any critical updates that should have occurred during the conversion process will be addressed after go live. 3.6.4 Going live The primary goal of the project’s conversion effort is to provide the agency with a base set of data to support its business needs when the new system comes online. At this point in the cutover plan that base data has been provided. The final steps are to accept the new system and enable access for all authorized users. 4 Data Enrichment Approach Page 23 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] Data enrichment covers any improvements to data with the aim of contributing to benefits realisation of the Business Transformation Programme. This is work stream 4 as mentioned in section 2.2.2.4. Many of the data issues that fall within this work The Business Lead, Data Enrichment is responsible for: • Develop selection criteria – including identifying relationship to Benefits and programme sequencing • Develop prioritisation commitment • Determine effort, cost, risk, value proposition • Recruit external team • Work closely with range of stakeholders including : o BT programme team – particularly BTMs and Product Owners o Segment Management Leads – understand existing work underway or planned in the business o FAST o Heritage o Data Lead, Business Data Stream Team – ensure alignment with existing work • Regular reporting, measurement and monitoring to DATA OWNERS FORUM and potentially Executive Working Committee. • Full scope to be drafted, project plan, milestones, deliverables • Weekly meeting with Sponsor 5 Reporting Data Owners Forum Regular status reports for data cleansing, conversion and enrichment will be produced by each team (FAST Conversion Team, Business Data Stream Team and Data Enrichment Team) and presented to the Data Owners Forum for inclusion in the relevant Release 3 Programme Management reports as required. Appendix A – Business Data Stream Team – The 4 Work streams Page 24 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] Page 25 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] Appendix B – High Level Data Cleansing Plan/Timeline Page 26 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] Appendix G – Definitions Data Cleansing refers to the correction of data that is required to enable the successful conversion of data to START and includes any automated or manual fixes in either the FIRST or START systems to provide START with a base set of data for IR to continue its operations. Data enrichment refers to improving data in order to ensure that the intended benefits of the Business Transformation programme are realised both for the customer and the business experience. Often this work does not impact on data conversion while it may still impact on the business or the customer. Data purification and/or remediation these terms are sometimes used interchangeably and over the top of Data Cleansing and Data Enrichment and depending on the context could refer to either. The qualifying factor will be whether the change is required to enable successful conversion of data from FIRST to START or to improve the Customer/Business Experience. Often there is a cross-over between the two outcomes. Data Stewards Data Stewards are responsible for the management of data elements, data objects and processes, for both content and metadata within CCSI & CCSB. Data stewards take an enterprise view and have a specialist role that incorporates processes, policies, guidelines and responsibilities for administering IR’s data in compliance with policy and/or regulatory obligations. The role of the Data Stewards in relation to Data Cleansing is to provide specialist knowledge for thorough remediation analysis, prioritisation and recommendations to the Data Owners Forum. Business Stakeholders are the people leaders and decision makers within the Business that initiate and drive data cleansing work as part of BAU. This work falls into work stream 1. A close relationship needs to be maintained between the Business Data Stream Team and CCSI, CCSB & IT&C. Stakeholders to give Data Owners Forum transparency of all data cleansing activities being carried out across IR and to enable the communication of decisions and advice to the Business. Core Subject Matter Experts (SMEs) are responsible for the management of data elements, data objects and processes for both content and metadata. Core SMEs take an enterprise view and have a specialist role that incorporates processes, policies, guidelines and responsibilities for administering IR’s data in compliance with policy and/or regulatory obligations. There are a set of SME’s for both FIRST and START systems that work closely with the Core Business Transformation Managers (BTMs). The Business Data Stream Team Data Remediation Analysts provide input and advice during design discussions held by the SMEs relating to impacts on conversion. Core Business Transformation Managers (BTMs) are responsible for the management of data elements, data objects and processes, for both content and metadata within their Jellybean. The Business Data Stream Team Data Remediation Analysts provide input and advice into design discussions with the BTMs relating to impacts on conversion. Converted Data Verification is an activity undertaken as part of testing the Release 3 conversion solution, and verifies that the data that we are moving from FIRST systems to START is moved/transposed accurately, in the correct location and as intended by the conversion plan. Page 27 of 27 \[IN CONFIDENCE RELEASE EXTERNAL\] The accountability and responsibility for the conversion plan (including Extraction, Transformation and Load) sits with the FAST Data Conversion Team. (See section 2) The Business Data Stream Team support and administer converted data verification by means of Work stream 3 of the Data Cleansing Plan. Work stream 1 – refers to everyday BAU data cleansing carried out by CCSI, CCSB and IT&C rather than directly by the Business Data Stream Team (See 3.2.1.1) Work stream 2 – refers to data cleansing work carried out on known R3 data issues by CCSI, CCSB and IT&C, driven by the Business Data Stream Team (See 3.2.1.2) Work stream 3 – refers to converted data verification cleansing activity, driven by the FA ST Data Conversion Team. (See 3.2.1.3) Work stream 4 – refers to data enrichment to enable Transformation benefits realisation, driven by the Business Lead, Data Enrichment (see 3.2.1.4)
[Skip to main content](#main-content-tt)

DDG0112

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

01 Aug 2006

Draft general depreciation determination - exposure draft
=========================================================

Draft general depreciation determination DDG0112 (2006) relating to two CCH products will not be finalised and related Prov4 has no on-going application.

In _Tax Information Bulletin Volume 18, No 7_ (August 2006) on page 4 we advised of the availability of a draft general depreciation determination - Exposure Draft DDG0112 ('DDG0112') for comment. DDG0112 proposed the setting of general depreciation rates for the following asset classes:

*   CCH Electronic New Zealand Master Tax Guide, designed for a specific tax year.
*   CCH Electronic New Zealand Essential Tax Package, designed for a specific tax year.

DDG0112 if issued would have replaced Determination PROV4: Tax Depreciation Rates Provisional Determination Number 4 ('Prov4'), which was issued on 7 September 1995 and published in _Tax Information Bulletin Volume 7, No 3_ (September 1995). Prov 4 set the provisional depreciation rates for the two CCH products listed above.

As a result of comments received on DDG0112, the Commissioner is now aware that the two CCH products are no longer available in the form described in DDG0112 and Prov4. Consequently the Commissioner does not intend to proceed with finalising DDG0112.

In addition, as there are no longer any depreciable property to which Prov4 applies, Prov4 has no on-going application.

Report a Problem with this Page or Publication

DDG0112

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DDG0112

Issued

01 Aug 2006
[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Ngā kaihokohoko rawa whenua, ngā kaiwhakaahu me ngā kaihanga Property dealers, developers and builders
======================================================================================================

You’ll probably need to pay tax on any profit from a property sale if you’re a dealer, developer or builder, or otherwise involved in the property business.

Buying as part of your business
-------------------------------

If you buy property as part of your property or construction business, you’ll need to pay tax on any profit when you sell it. This applies no matter how long your business owns the property.

Buying outside your business
----------------------------

If you buy property while you’re in the property or construction business, you may need to pay tax if you sell it, even if you bought it outside your business. For example, you bought a property under your own name while you were also in business as a property developer.

This depends on when you sell it and what kind of business you’re in.

### The 10-year rule if you're dealing, developing or subdividing property

Generally, you’ll have to pay tax on your profits from selling a property if both of the following apply.

*   At the time you bought the property, you, or someone you were associated with, was in the business of dealing, developing or subdividing property.
*   You sold it within 10 years of buying it.

### The 10-year rule for builders

Generally, you’ll have to pay tax on your profits from selling a property if both of the following apply.

*   When improvements began on the property, you, or someone you were associated with, was in the building business.
*   You sold the property within 10 years of completing improvements on it.

#### When the 10-year rule does not apply

The 10-year rule does not apply in any of the following situations.

*   The property is your main home.
*   You used the property in your business, but not as a rental.
*   You're an employee of a property dealer, developer or builder, not in business yourself.
*   You're no longer in the property business when you buy the property, or you bought it before you went into business.
*   You're associated to a property developer at the time you acquired the property and after partitioning a subdivision there was no substantive change in ownership.

Associated with the property business
-------------------------------------

If you're associated with someone in the property business, you may have to pay tax on all or some of your property transactions, even if you're not personally a property dealer, developer or builder.

[Associated with a property dealer, developer or builder](/property/buying-and-selling/when-you-need-to-pay/associated-with-property)

Property affected by weather events
-----------------------------------

The land time-related tests do not tax properties affected by a North Island adverse weather event purchased by a Crown or local authority.

[January and February 2023 weather events](/topics/tax-relief-for-emergency-events/january-and-february-2023-weather-events)

Get advice
----------

If you’re in the property business or associated with someone who is, we recommend you speak with a tax or legal professional to find out how these rules apply to you.

* * *

Was this page helpful?

 Yes

 No

What did you like about this page?

 This isn't what I was looking for.

 There aren't enough examples.

 The information is hard to understand

 The information doesn't solve my issue.

 Other

Please tell us how we could improve this page?

Submit

**Thanks for sharing your opinion!** Your feedback has been received.

Sorry there was an issue submitting your feedback, please try again later.
[Skip to main content](#main-content-tt)

[Policy issues](/new-legislation/act-articles/taxation-base-maintenance-and-miscellaneous-provisions-act-2005/policy-issues "Policy issues")

Death and Asset Transfers
=========================

2005 rules clarify the treatment of 'in kind' or 'in specie' distributions from companies, trusts, gifts, and transfers of assets/liabilities on a taxpayer's death.

_Subpart FI and sections CZ 6, EC 4, EE 34, EE 38, EE 40, EH 5, EH 19, EH 50, EH 67, EW 29, EW 36, EW 39, EW 41, EW 44, EX 55, FB 3, GD 2 and GD 14 of the Income Tax Act 2004 and the definition of "date interest starts" in section 120C(1) of the Tax Administration Act 1994_

Generic rules have been introduced to clarify the income tax treatment of "in kind" or "in specie" distributions from companies and trusts, gifts, and transfers of assets and liabilities on a taxpayer's death. Such distributions, gifts and transfers are treated as disposals and acquisitions at market value. The new rules have implications only to the extent the property is inside the tax base to start with.

The effect of the new rules on the estates of deceased individuals is that there will generally be two market value transfers: one at the time of the taxpayer's death, and one on the subsequent distribution of the assets to beneficiaries. A

number of exclusions to the market value rule reduce compliance costs.

#### Background

Tax law in the area of "in kind" distributions from companies and trusts, gifts and transfers on the death of a taxpayer has been neither clear nor consistent. Cases in recent years highlighted this lack of clarity, and there have been repeated calls to clarify the tax treatment of assets and liabilities on the death of a taxpayer and their subsequent distribution to the beneficiaries. For example, a beneficiary had no depreciation cost base for assets distributed by a trust, although the trustees were required to treat the distribution of the assets as a disposal at market value. These issues were raised by the Valabh Committee in its 1992 report, Tax accounting issues.

An officials' issue paper, Tax implications of certain asset transfers, was published in April 2003, and the proposals in that paper were modified as a result of submissions received.

#### Key features

The new generic rules are provided by new subpart FI of the Income Tax Act 2004. Assets and liabilities distributed or transferred are deemed to be a disposal and acquisition at market value.

Unless an exception applies, there will be two valuation points in respect of each deceased individual's estate: one at the date of death, and the other when the estate is distributed. The exceptions are:

*   Section FI 4 provides that assets and liabilities that pass to a spouse or de facto partner of a deceased person can be transferred at their tax book value, as long as all assets of the deceased that were in the tax base pass to the spouse or de facto partner or another person who is a relative within the second degree of relationship. (Transferring assets at their tax book value is known as rollover relief.)
*   Section FI 5 provides for simple estates when assets are left either to charity or to relatives within the second degree of the deceased taxpayer. Rollover relief will apply on the distribution of the estate. The transfer of the assets from the deceased to the administrator or executor of the estate will be at market value, unless any of the other exceptions apply.
*   Both of these exceptions will continue to apply if there are legacies to third parties of assets that are not in the tax base.
*   Section FI 6 provides rollover relief both on the date of death and when the estate is distributed for forestry assets if the beneficiaries of the estate are relatives to within the second degree of relationship to the deceased.

In addition, to reduce compliance costs, certain assets can be valued at cost rather than market value:

*   Section FI 8 provides that unexpired accrual expenditure continues to be valued at cost. The valuation date is treated as the end of the income year.
*   Section FI 11 provides that when an estate is a cash basis holder, financial arrangements are valued at cost both on the date of death and when the estate is distributed.

Generally, a taxpayer's death does not, in itself, lead to an asset being brought into the tax base. While the rule applies to all assets, it has relevance only to the extent the assets are already in the tax base. A particular example of this is the treatment of land held on capital account, the proceeds of which would be assessable if the property was sold within 10 years of acquisition. Section FI 7 ensures that death by itself does not trigger this 10-year rule.

Use-of-money interest will not be imposed on a deceased individual's tax liability in the year of death, so long as all tax due is paid by the due dates.

Sections FI 9 and FI 10 are transitional provisions that ensure that the tax treatment of past deaths and distributions from trusts and estates are not to be disturbed when:

*   the tax base is protected by the position that was taken, either because the tax book values of assets and liabilities were rolled over, or because a market value exercise was done; and
*   the beneficiaries of the trust or estate are limited to persons that are New Zealand-resident for tax purposes and are not exempt from income tax because they are charities; and
*   the underlying law was not clear.

### Application date

The new rules apply prospectively and come into force on 1 October 2005.

#### Detailed analysis

##### Section FI 1: Disposals and resulting acquisitions to which subpart FI applies

To ensure comprehensive and generic rules, the new subpart provides a disposal value and an acquisition cost price of property that includes:

*   distributions from a trustee to the beneficiary of a trust;
*   "in kind" or "in specie" distributions from a company to a shareholder that are dividends;
*   gifts;
*   transfers to an administrator or executor or trustee of a deceased estate;
*   distributions by an administrator, executor or trustee of a deceased estate to a beneficiary; and
*   a settlement from one trust to another.

##### Section FI 2: Disposal and resulting acquisition of property treated as occurring at market value

Distributions and transfers to which subpart FI refers are treated as disposals and acquisitions at market value. The same market value that is used for the disposal must be used for the acquisition.

##### Section FI 3: Date on which disposal and resulting acquisition are treated as occurring

The date of the disposal and acquisition for tax purposes will generally be the date the person disposes of the property.

Subsection (2) provides that transfers upon death are treated as occurring immediately before death.

##### Section FI 4: Disposal and resulting acquisition of property by spouse or de facto partner of the deceased taxpayer

Assets and liabilities that pass to a spouse or de facto partner on the death of a taxpayer are transferred at tax book values as long as the beneficiaries of the rest of the property that is in the deceased's tax base are limited to family members who are within the second degree of relationship to the deceased person. It does not matter who receives assets that are not in the tax base. Property that is within the tax base is:

*   revenue account property;
*   an interest in a foreign investment fund;
*   financial arrangements which were not accounted for by the deceased taxpayer as a cash-basis person; and
*   assets upon which depreciation has been claimed.

The rationale for this relief is that it appropriately replicates the Property (Relationships) Act 1976.

##### Section FI 5: Distributions of property to close relatives and charities

When certain conditions are met, a distribution from the administrator or executor to the beneficiaries is transferred at tax book values. The conditions for this exception applying are:

*   the only beneficiaries of an estate are persons related to the deceased to the second degree, or are charities; and
*   the estate does not establish any life interests; and
*   the terms of the will or intestacy require that no property of the deceased taxpayer be held in trust; and
*   in the tax year during which the property is subject to administration or executorship or in which the property is held in trust for this purpose, the net income of the estate is distributed beneficially to the maximum extent possible.

This relief will not be affected if there are legacies of assets that are not in the tax base to persons who are not relatives. The spouse or de facto partner relief takes precedence over this relief, except when charities receive assets that are within the tax base. It is intended to reduce compliance costs.

##### Section FI 6: Disposal and resulting acquisition of property that is standing timber

When timber, standing timber, or a right to take timber owned by a deceased person is left to a person who is related to the second degree, the transfer to the administrator or executor of the estate and the  
subsequent transfer to the beneficiary is at the tax book value.

This exclusion recognises that immature forests, in particular, are difficult to value.

##### Section FI 7: Relationship of section FI 2(2) to subpart CB

The subpart CB 10-year "tainting" rules (sections CB 7, CB 8, CB 9 and CB 12) do not apply to the transfer of assets and liabilities to the administrator or executor of the estate (section FI 1(3)(d) transactions) and the subsequent transfer to the beneficiaries (section FI 1(3)(e) transactions) if the property passes to a person who is related to the deceased taxpayer within the second degree of relationship.

If the relief provided by section FI 8(1) and (2) does not apply, section FI 8(3) provides that a deduction will be allowed against the proceeds of the property, for the original cost of the land to the deceased person, plus all other costs incurred by the deceased person, the administrator or executor or the beneficiary.

##### Section FI 8: Relationship of subpart FI to unexpired prepayments

Property that is subject to section EA 3 (Prepayments) is valued at cost, rather than market value, when it is transferred to the administrator or executor and when it is subsequently transferred to the beneficiary. The valuation date is treated as the end of an income year.

This provision will reduce compliance costs.

##### Section FI 9 and 10: Death or trust distributions before 1 October 2005

Section FI 9 and 10, when read together with the general savings rule in the Income Tax Act 2004 (subpart YA), provide that certain past tax treatments are saved, generally when the past treatment was uncertain and the tax base is not at risk.

Section FI 9 applies when the following criteria are met:

*   The taxpayer died before 1 October 2005.
*   The beneficiaries are New Zealand-resident for tax purposes and are not exempt from income tax because they are charities.
*   The Income Tax Act does not explicitly specify a treatment for both the deceased taxpayer and the executor or trustee.

If the same valuation method was used for both the disposal by the deceased taxpayer and the acquisition by the administrator or executor, and that valuation was either at market value or a rollover, it will be accepted as appropriate.

Section FI 10 provides the same rules for distribution from trusts.

##### Section FI 11: Disposal of certain financial arrangements on death

Financial arrangements will be valued at cost, both upon the death of the taxpayer, and at the time of distribution to beneficiaries, if the deceased taxpayer's estate is a cash-basis person. For the estate to be treated as a cash-basis person, the deceased taxpayer would need to be a cash-basis person at the date of death.

##### Use-of-money interest

The definition of "date interest starts" in section 120C of the Tax Administration Act 1994 has been amended to restrict the imposition use-of-money interest on a deceased taxpayer's tax liability in the year of death, as long as provisional and terminal tax payments are made by due date. Although the amendment provides that the concession will apply only to dispositions to which section FI 4 (disposal and resulting acquisition of property by spouse or de facto partner) of the deceased taxpayer applies, the policy intention is that it should apply to all estates. This will be corrected in the next tax bill.

This is a concessionary measure which ensures that estates will not incur unexpected use-of-money interest liabilities when a taxpayer's death triggers a tax liability.

##### Consequential amendments

Subpart FI is a comprehensive set of rules which provide for the tax treatment of "in kind" or "in specie" distributions, including the transfer of assets upon a taxpayer's death. Accordingly, a number of specific provisions which address specific transactions have been repealed. Other sections are being amended to make them consistent with the new rules.

_Sections CZ 6(3), EC 4, EE 40(7), EW 29(13), EW 36(1)(b)(i), EW 39, EW 41(1)(b)(i), EW 44, EX 55, and GD 2 have been repealed. Sections EE 34, EE 38, EH 5(4), EH 19(2), EH 50(2), EH 67(4), FB 3, and GD 14(3)(c) are amended._

Section EE 34 provides that a taxpayer who acquires depreciable property from an associated person cannot claim more depreciation on that property than the associated person would have been able to had they retained the property. Subject to certain exceptions, the taxpayer's depreciation base is limited to the original cost of the property incurred by the associated vendor for anti-avoidance reasons.

As death is not a planned event there is no concern about anti-avoidance. When a rollover does not apply, the estate should use market value if that is appropriate. New subsection (6) has been added to section EE 34 to ensure this.

If property is disposed of for less than its market value, section EE 38 deems the consideration to be the market value of the property. New subsection (2B) provides that the market value rules do not apply if either of the rollover provisions, sections FI 4 or FI 5 apply.

Sections EH 5(4), EH 19(2), EH 50(2) and EH 67(4) are amended so that they continue to operate as if section FI 3 (date on which the disposal and resulting acquisition is treated as occurring) had not been enacted.

Section FB 3 is amended to make it clear that it does not apply when the rollover provisions of sections FI 4 to FI 6 apply.

Section GD 14(3)(c) is amended because subparagraph (ii) is no longer necessary, given the new rules for distributions.
[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Te nama me te kaihautanga Debt and insolvency
=============================================

If you have tax debt you cannot pay, we can help you. Individuals, companies, partnerships and trusts can apply for either:

*   an instalment arrangement
*   financial relief.

We might ask you for more information so we can understand your situation and work out the best way to help you. If you're in business, we may get you to send us a Twelve month cash flow forecast - IR591.

If you're unsure of your options, give us a call and we'll help you out. If you know ahead of time that you will not be able to pay your tax, contact us or start the application that best fits how you want to move forward.

[Debt and refunds - contact us](/contactus/debt-refunds)

Applying for an instalment arrangement
--------------------------------------

Splitting up what you owe over weekly or fortnightly payments can make it easier to repay your tax debt. Apply for an instalment arrangement if you cannot afford to pay the tax you:

*   already owe
*   will owe in the future.

You can apply for instalment arrangements for all tax types, except child support, in myIR. We'll either:

*   approve it
*   contact you for more information.

Setting up direct debit payments is a good way to make your ongoing instalments. You'll be able to set these up in myIR or choose a different way of paying.

[Apply for an instalment arrangement](/managing-my-tax/debt-and-insolvency/apply-for-an-instalment-arrangement-in-myir)

Applying for financial relief
-----------------------------

If you cannot meet your payments, we might be able to write off penalties or certain amounts. We'll need you to send us information in your application for financial relief before making a decision.

If you're [overseas-based](/api/glossary/item?id={0D56A105-8E3D-4EF9-B502-52EEBC261811})
 with a student loan or a [non-resident taxpayer](/api/glossary/item?id={629D26DB-A2DC-4E9F-88E8-397C0AA00D67})
, we'll need a bit more information in your application. We normally have most of the information we need for companies, partnerships and trusts, so your application is also a different process.

[Apply for financial relief - individuals in New Zealand](/managing-my-tax/debt-and-insolvency/financial-relief-nz-individuals)

[Apply for financial relief - overseas-based or non-resident individuals](/managing-my-tax/debt-and-insolvency/financial-relief-overseas-based-or-non-resident-individuals)

[Apply for financial relief - companies, partnerships and trusts](/managing-my-tax/debt-and-insolvency/financial-relief-companies-partnerships-trusts)

Student loan debt
-----------------

If you have a student loan, check our student loan section before applying for an instalment arrangement or financial relief. There, you'll find information about:

*   interest on your debt
*   other options you may be able to use in managing your student loan debt.

[I am having difficulty repaying my student loan](/student-loans/tracking-my-student-loan-balance/difficulty-repaying-student-loan)

Child support debt
------------------

Get in touch with us if you have child support debt. We'll work with you to manage your payments. We may be able to write off your penalties.

[Sorting out child support debt](/child-support/managing/debt)

Working for Families overpayments
---------------------------------

If you've been overpaid Working for Families, you'll need to know the different ways you can repay it.

[Paying back Working for Families overpayments](/working-for-families/managing/repaying)

#### Topics

*   [Interest on overpayments and underpayments (UOMI)](/managing-my-tax/penalties-and-interest/interest-on-overpayments-and-underpayments "Interest on overpayments and underpayments (UOMI)")
    
*   [Penalties and debt](/managing-my-tax/penalties-and-interest/penalties-and-debt "Penalties and debt")
    

#### Situations

*   [I am in Working for Families debt](/situations/i-am-in-working-for-families-debt "I am in Working for Families debt")
    
*   [I'm struggling to file and pay my tax](/situations/unable-to-pay-my-tax-debt "I'm struggling to file and pay my tax")
    

#### Roles

*   [Self-employed](/roles/self-employed "Self-employed")
    
*   [Partnerships](/roles/partnerships "Partnerships")
[Skip to main content](#main-content-tt)

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2012

Issued

2012

Decision

15 Mar 2012

Appeal Status

Appealed

Debtor-initiated payments
=========================

2012 case note - considers debtor-initiated payments and the law of restitution regarding mistaken payments - good faith, mistake of law.

Case

Stiassny & Ors v Commissioner of Inland Revenue

Legislative References

Goods and Services Tax Act 1985, Personal Property Securities Act 1999

### Summary

The Court of Appeal considered the issues of debtor-initiated payments under section 95 of the Personal Property Securities Act 1999 ("PPSA") and how such payments effected priorities and claims in restitution for payments made by mistake. The Court of Appeal found that not only had the Commissioner of Inland Revenue ("the Commissioner") provided good consideration, but he had also acted in good faith in receiving payment of goods and services tax ("GST") from the receivers. The Court of Appeal dismissed the Appellants' appeal.

### Impact of decision

This decision, although significant in terms of quantum has limited tax technical implications. However, the decision is very significant for its analysis of section 95 of the PPSA dealing with debtor-initiated payments and how it relates to the law of restitution regarding mistaken payments.

### Facts

The respondents in this case are:

*   two companies, who were partners in the Central North Island Forestry Partnership ("CNIFP") and the receivers of those companies
*   the secured creditors of the CNIFP.

The partner companies were each placed in receivership by a secured creditor. The CNIFP itself was not in receivership.

The CNIFP sold a forest for US$621 million, plus GST of approximately NZ$127 million. There were insufficient funds to repay secured lenders as well as the GST on the sale, which resulted in a dispute as to the priority of the GST amount. The receivers paid the GST to the Commissioner and commenced proceedings to claim the funds back. The respondents sought:

*   an order that the receivers were not liable to pay the GST
*   the return of the funds as money paid under a mistake of law (a restitutionary claim).

The Commissioner applied to strike out the claim in the High Court.[1](#1)
 The Court found in favour of the respondents. The Commissioner subsequently appealed the High Court's decision to decline to strike out the respondents' claim to the Court of Appeal.

The issues for the Appeal were:

1.  whether the receivers were liable for the GST
2.  whether section 95 of the PPSA operates so as to confer priority to the Commissioner over any claim the respondents have to the GST
3.  whether the respondents could recover the GST from the Commissioner on the basis it was paid under a mistake of law namely that the receivers were personally liable to pay the GST.

### Decision

The Court of Appeal affirmed the decision made by the High Court that the receivers were not liable to pay the GST; the liability was that of the partnership.

The Court of Appeal was not persuaded by the Commissioner's argument that the combined relevant purposes of sections 57 and 58 of the Goods and Services Tax Act 1985 ("GST Act") are to achieve efficiency and to ensure that a receiver pays the registered person's GST liabilities during a receivership.

*   We are not persuaded that this interpretation is available to the Commissioner and agree with Mr Simcock's submissions on this issue. First, this interpretation would require the notional insertion of words in s 58 which are not there. Secondly, and more importantly, this approach would directly contradict s 57(2)(a) which provides that partners shall not be registered persons. The Commissioner's approach would mean that partners in a partnership were effectively made registered persons in respect of the partnership's taxable activities whenever the partners went into receivership, despite the clear wording of s 57(2)(a). Thirdly, such an interpretation is not "required" because the Commissioner has a secondary right of recovery against the members of the partnership by virtue of s 57(3) and (5). \[24\]

The Court of Appeal held that the GST Act contemplates that primary liability for the payment of GST falls on the unincorporated body as the registered person. Secondary liability under subsections 57(3) and (5) falls only upon the members of that body:

*   The section does not, for example, provide that directors or executives of a company which is a member of a partnership might become liable for GST because they somehow participate in the taxable activities of the partnership. Secondly, the GST Act provides that receivers only become personally liable to pay GST in the carefully defined circumstances of s 58, which we have found do not apply here.

The Court of Appeal held that the receivers were not carrying on the taxable activities of the partnership:

*   Thirdly, although the receivers manage the partner companies and, through them, the affairs of the partnership, it does not follow that they are deemed for the purposes of the GST Act to be carrying on the taxable activities of the partnership. The partnership (CNIFP) continues to conduct its own activity for GST purposes and, as such, is primarily liable for the payment of GST. \[27\]

The Court of Appeal agreed with the High Court that the payment of GST by the receivers to the Commissioner was a debtor-initiated payment within the meaning of section 95 of the PPSA on the footing that the receivers, as agents for the two partners (and through them the CNIFP), initiated payment to the Commissioner:

*   ... Importantly too, the payment was made from funds belonging to the CNIFP and with the express consent of the BNZ on behalf of the senior secured creditors. There is no question that the CNIFP owed the GST sum to the Commissioner whether or not the receivers may have believed they were also personally liable for payment of this sum. \[67\]

Whether the security interests had crystallised and whether the payment was made in the ordinary course of business were not relevant to the operation of section 95. The payment was a debtor-initiated payment, notwithstanding it was paid under compulsion or pressure as a result of exposure to interest and penalties:

*   ... There is nothing in the language or purpose of s 95 which requires that a gloss be placed on the meaning of the term "debtor-initiated payment". There can be no question here but that the payment was initiated by or on behalf of the debtor in the sense that a conscious decision was taken by the receivers to forward a cheque to the Commissioner for the amount of the GST liability. The fact that they did so because they believed that they were or might be personally liable for the amount of the GST concerned could not justify the conclusion that the payment was other than debtor-initiated. Although the payment was made for motives associated with the sanctions for late payment imposed by the relevant statutory regime, it could not be said that the payment thereby lost its debtor-initiated status. \[72\]

The Court also considered it was a factor that the members of the partnership, the receivers and the BNZ as the security trustee for the senior secured creditors all agreed that GST should be paid from the sale proceeds and authorised the receivers to proceed accordingly. The Court also noted that:

*   We add that the receivers no doubt required the purchaser to pay GST on the purchase price so they would have the necessary funds to discharge the GST liability to the Commissioner. At the time the payment was made, it was never contemplated that the secured creditors would receive the windfall benefit of the GST collected on the sale of the partnership assets.

The Court of Appeal did not accept the respondents' submission that the issue of whether this was a debtor-initiated payment should have been left for trial rather than being dealt with on a strike-out application.

*   ... This was a straightforward issue capable of ready determination as a matter of law on the undisputed facts before the Court. Counsel did not elaborate on what further factual material might have been relevant. \[71\]

The Court of Appeal concluded that the Commissioner was prima facie entitled to priority over the secured creditors in relation to the GST payment subject to the possibility of _in personam_ claims.

The Court of Appeal found that not only had the Commissioner provided good consideration, but that he had also acted in good faith in receiving payment of the GST from the receivers. The Court rejected an argument by the receivers that the CNIPF (through its member companies) had no authority to make the GST payment as the payment was made with the express authority of the BNZ as the security trustee for the secured creditors and, more importantly, section 95 of the PPSA recognises that a debtor is entitled to make a payment to a creditor notwithstanding the existence of a security interest over the assets from which payment is made.

The Court of Appeal confirmed the approach of the High Court that defences to a restitutionary remedy may include the giving of good consideration by the payee or alteration of position by the payee and concluded that:

*   It is unnecessary for us to enter further into this debate other than to note that the giving of good consideration has been accepted as a proper ground upon which a court may determine that the defendant has not been unjustly enriched. This follows on the simple footing that, if the defendant is entitled to the money, then it cannot be said to be unjust, or against conscience, to require repayment. \[94\]

The Court found that there was no suggestion that the Commissioner knew of the receiver's mistaken belief that they were personally liable to pay GST. The issue was whether mere notice of an adverse claim is sufficient to demonstrate an absence of good faith on the part of the Commissioner. The Court considered that the current authorities and academic commentary were of no real benefit because they had no direct relevance to where the defence is that the Commissioner gave good consideration for the payment. Accordingly the Court found:

*   All the Commissioner has done in the present case is to receive the GST payment in the belief that it was properly due, a view which was shared at the time by the receivers and their advisers. Although the Commissioner was advised prior to the making of the payment that the secured creditors claimed to be entitled to the money, there is no suggestion that the Commissioner doubted his entitlement or had reason to believe there was a likelihood he would have to repay the money. Indeed, he rejected the Notice of Proposed Adjustment later issued by the receivers under the Tax Administration Act and has consistently maintained the view that he is entitled to the payment. \[105\]

The Court of Appeal also made a further point, not addressed by counsel, that it may be inappropriate to engraft good faith requirements upon the statutory regime under the Tax Administration Act 1994 for the resolution of disputes of this kind. The Court explained that:

*   When the Commissioner receives a payment of GST he does so with the knowledge that any dispute over liability to pay the GST is subject to the dispute resolution processes under that Act. Absent dishonesty or some other wrongdoing, no question of bad faith arises.

* * *

1 _Stiassny v Commissioner of Inland Revenue_ HC Auckland CIV-2008-404-549, 4 November 2010.

Report a Problem with this Page or Publication

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2012

Issued

2012

Decision

15 Mar 2012

Appeal Status

Appealed
[Skip to main content](#main-content-tt)

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2012

Issued

2012

Decision

28 Nov 2012

Appeal Status

No right of appeal

Debtor-initiated payments
=========================

2012 case note – debtor-initiated payments and the law of restitution regarding mistaken payments – consideration, good faith, mistake of law.

Case

Stiassny & Others v Commissioner of Inland Revenue

Legislative References

Goods and Services Tax Act 1985, Personal Property Securities Act 1999

### Summary

The Supreme Court considered the issue of debtor-initiated payments under section 95 of the Personal Property Securities Act 1999 ("PPSA") and how such payments effected priorities and claims in restitution for payments made by mistake. The Supreme Court found that not only had the Commissioner of Inland Revenue ("the Commissioner") provided good consideration, but she had also acted in good faith in receiving payment of the goods and services tax ("GST") from the receivers. The Supreme Court dismissed the appellants' appeal.

### Impact of decision

This decision, although significant in terms of quantum, has limited tax technical implications. However, the decision is very significant for the analysis of section 95 of the PPSA and how it relates to the law of restitution regarding mistaken payments.

### Facts

The appellants in this case were:

*   two companies, and the receivers of those companies, who were the partners in the Central North Island Forestry Partnership ("CNIFP"); and
*   the secured creditors of the CNIFP.

The partner companies were placed into receivership by a secured creditor. The CNIFP itself was not in receivership.

The CNIFP sold a forest for US$621 million, plus GST of approximately NZ$127 million. There were insufficient funds to repay secured lenders as well as the GST on the sale, which resulted in a dispute as to the priority of the GST amount. The receivers paid the GST to the Commissioner and commenced proceedings to claim the funds back. They sought:

*   an order that the receivers were not liable to pay the GST;
*   the return of the funds as money paid under a mistake of law (a restitutionary claim).

The Commissioner unsuccessfully applied to strike out the claim at the High Court and subsequently appealed the High Court's decision to decline to strike out the respondents' claim to the Court of Appeal. The Court of Appeal allowed the Commissioner's appeal holding that section 95 of the PPSA gave the Commissioner the priority. The Court of Appeal did however find that the receivers were not personally liable to pay the GST. The appellants were granted leave to appeal to the Supreme Court.

### Decision

The Supreme Court affirmed the decision made by the High Court, and by the Court of Appeal that the receivers were not liable to pay the GST; the liability was that of the partnership.

The Commissioner's first argument advanced was that in effect section 58 of the Goods and Services Tax Act 1985 ("GST Act") should be read as if section 57 did not appear in the Act. Absent section 57, each partner would be treated as carrying on the partnership's taxable activity and would be required to register. As each partner in the CNIFP was an incapacitated person because they were each in receivership then, the receivers would then be their specified agents and must under section 58(1A) be treated as carrying on the taxable activity and so be liable to pay the GST incurred. The Supreme Court held at \[26\]:

*   The argument is ingenious but, like the Courts below, we do not accept it. It requires the carefully crafted and very clear directives in section 57(2) that members of an unincorporated body are _not_ liable to be registered and that the body's taxable supplies are deemed _not_ to be made by any member to be disregarded or, as the Court of Appeal said, contradicted; and it would require a reading of the definition of "incapacitated person" in section 58(1) as if it said "a registered person (or someone who would be required to be registered but for section 57)". It would be wrong to ignore the directives in section 57 and to put into section 58 additional words which are not obviously required by the sense of the provision.

The second and alternative argument advanced by the Commissioner was in respect of section 57(3) of the GST Act, which makes a member of an unincorporated body jointly and severally liable for all the tax payable by the body during that person's membership. A "member" is defined in section 2 as including a partner, a joint venture, a trustee, or a member of an unincorporated body. The Commissioner submitted that section 57(3) should be read as also including a receiver of a member. The Supreme Court held at \[27\]:  

*   ... Once more, and in common with the High Court and the Court of Appeal, we decline to accept this argument. It again involves reading into the statute something which is certainly not implicit. Those expressly designated as members by the definition are all persons who would be the owners of the assets of, or a share or interest in, the unincorporated body. It is a stretch too far to treat as a member for the purposes of section 57 someone like a receiver who has no legal or beneficial entitlement to any such assets or share or interest – in this case, to the assets of the partners. And it would involve the imposition of a receiver's personal liability in circumstances where section 58, directed, inter alia, at the position of insolvency administrators, does not do so.

The Supreme Court agreed with the High Court and Court of Appeal that the payment of the GST by the receivers to the Commissioner was a debtor-initiated payment within the meaning of section 95 of the PPSA on the footing that the receivers, as agents for the two partners (and through them the CNIFP) initiated payment to the Commissioner.

The Supreme Court did not accept the appellants' argument that even if the partnership did have legal title to the proceeds of sale and made the payment of the GST, those proceeds were to be viewed as held on a bare trust for the secured creditors, and so, in equity, the payment to the Commissioner utilised their property, which they could recover. In essence, the appellants were seeking to overcome section 95 of the PPSA by arguing that if the payment was made using funds in a partnership bank account, in circumstances where at common law the partnership had only a bare legal title to the chose in action represented by the credit balance in the bank account from which the cheque was drawn, the payment was not debtor-initiated. Accordingly, it cannot be treated under section 95 of the PPSA as a payment by the debtor partnership.

The Supreme Court also did not accept the appellants' argument that the Commissioner could not rely on section 95 of the PPSA because she had actual knowledge or notice when she received the GST that the payment to her was in breach of the terms of the security interests in the proceeds of sale held by the Bank of New Zealand ("BNZ") and CNIFP and that she had not acted in accordance with the requirements of section 25 of the PPSA to exercise good faith.

The Supreme Court did accept the appellants' argument that even if section 95 of the PPSA would give the Commissioner a priority over the secured creditors, that did not prevent any of them from arguing their case as a claim for recovery of the GST as a payment made by mistake or under compulsion. Moreover, the Supreme Court accepted that the receivers had made a mistake about the law when they caused the partnership to make the GST payment, thinking that they were personally liable for the GST. However, the Supreme Court found that the partnership's claim must nevertheless fail on restitutionary principles (at \[65\]):

*   The partnership did owe the Crown the amount of GST which it paid to the Commissioner. Therefore the Commissioner gave good consideration in accepting its payment in discharge of the debt.

The Supreme Court concluded that (at \[70\]):

*   It has not been shown by the Commissioner at this stage of the case that the receivers were personally liable for the GST. The payment was made by the partnership. On the basis that the receivers were not personally liable, it was made because of a mistake by them. But it is not recoverable from the Crown. The claim of the partnership for recovery of a payment made by mistake or under compulsion fails because the Commissioner gave good consideration. The claim of the secured creditors fails because of section 95. The receivers have no independent claim.

Report a Problem with this Page or Publication

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2012

Issued

2012

Decision

28 Nov 2012

Appeal Status

No right of appeal
[Skip to main content](#main-content-tt)

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2016

Issued

2016

Decision

14 Jul 2016

Court

NZHC

Appeal Status

Not appealed

Decision reinforces strength of section 81 provisions
=====================================================

2016 case note - High Court reinforces the strength of s 81 (Tax Administration Act) provisions regarding secrecy as applied to discovery obligations.

Case

FAF Holdings Limited (in liq) and Ors v R J Bethune CIV 2015-412-0080 \[2016\] NZHC 1595

Legislative References

S 81 Tax Administration Act 1994

### Summary

The High Court found that due to s81(3) of the Tax Administration Act 1994 ("TAA"), the Commissioner of Inland Revenue ("the Commissioner") is not required to comply with discovery obligations under r 8.25 of the High Court Rules. Associate Judge Christiansen stated that due to the secrecy provisions invoked in s81(3), disclosing was not necessary for carrying into effect the Revenue Acts. His Honour further noted that the proceeding was between liquidators (governed by the Companies Act 1993) and Mr Bethune, the director of FAF Holdings Ltd ("the Company"), thus the tax liability of the company was not in dispute.

### Impact

This judgment upholds the long-standing principle that the Commissioner does not have to comply with information requests or discovery orders from parties who are not entitled to that information under any of the exceptions to secrecy in s 81.

### Facts

FAF Holdings Limited was put into liquidation on an application from the Commissioner on 11 December 2014.

The liquidators, who are the second respondents in these proceedings, are suing Mr Bethune, sole director and shareholder of the company, for a number of alleged breaches of director's duties under the Companies Act 1993.

Mr Bethune denies that he breached these duties and says in his defence that he was unaware that the company had difficulties until December 2013 and that it was an in-house accountant who had control and responsibility of the company's finances.

The liquidators requested from the Commissioner the company's files. These were provided by the Commissioner and duly discovered to Mr Bethune. The liquidators filed an affidavit stating that they had fully discovered to Mr Bethune all relevant documents obtained from the Commissioner. Mr Bethune, however, contended that there were exchanges between himself and Inland Revenue that were not part of the discovered documents.

To further his defence, Mr Bethune applied for non-party discovery against the Commissioner, seeking (inter alia) correspondence, internal reports and file notes on the company’s solvency and potential claims by the Commissioner against Mr Bethune.

The Commissioner opposed the application under section 81(3) TAA. Pursuant to that section, no officer of the Department shall be required to produce in any Court or Tribunal any document or to devolve or communicate to any Court or Tribunal any matter or thing coming under the officer’s notice in the performance of the officer’s duties as an officer of the Department, except when it is necessary for carrying into effect the Revenue Acts, the listed accident compensation legislation, any other act imposing taxes or duties payable to the Crown or Commissioner’s powers, duties or functions under the New Zealand Superannuation Act 1974.

The Commissioner also submitted that Mr Bethune was not entitled to the company's information under s 81(4)(l) (information held or obtained in relation to that person or their representative) because directors cease to have powers, duties or functions (other than those permitted under the liquidation provisions of the Companies Act) once a company is placed into liquidation.

### Decision

Associate Judge Christiansen dismissed the application. His Honour held that s 81(3) applied as disclosing was not necessary for carrying into effect the Revenue Acts.

His Honour also held that due to the privilege in s 81(3), the Commissioner is not required to comply with discovery obligations under the High Court Rules.

The fact that the Commissioner had lodged the claim resulting in the company’s liquidation was irrelevant; the tax liability of the company is not in dispute. The proceeding is between the liquidators, who have duties under the Companies Act which is not a Revenue Act, and Mr Bethune. Accordingly, the Commissioner is not required to produce the documents for the purpose of carrying into effect the Revenue Acts.

Mr Bethune did not have standing to request the company's documents under the exception in s 81(4)(l), therefore the section does not authorise the Commissioner to provide the company's information to Mr Bethune.

Costs were awarded on a 2B basis plus disbursements as approved by the Registrar.

Report a Problem with this Page or Publication

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2016

Issued

2016

Decision

14 Jul 2016

Court

NZHC

Appeal Status

Not appealed
[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Ngā whakatau mai i ngā arotake tautoko tamaiti Decisions from child support reviews
===================================================================================

After the hearing, the review officer considers the information given by everyone involved, as well as any relevant information we hold. They look at how the child support assessment affects:

*   the child
*   you
*   the other people involved.

There is no guarantee the assessment will be changed.

We usually finalise the decision within 3 weeks of the hearing and send everyone involved a copy. The review officer must provide reasons for their decision. Any information given to the review officer may also be in the decision, including any information:

*   given by the other person or people involved
*   already held by us.

Contrary decisions
------------------

When you apply for a child support review, it may not be limited to the grounds or reasons given in the application. The decision can have the opposite effect to the change you’ve applied for. We call this a 'contrary decision'.

When you’re thinking about applying for a review under one ground, keep in mind that the review officer may also consider other grounds.

Example - contrary decisions

You’re a liable parent and it costs you extra to cover your dependent child's special needs.

You could apply for these extra costs to be taken into account when your child support payments are worked out. But if the review officer sees that you’ve also recently had a large pay rise, you may find your child support payments go up overall.

Applications from 1 or more people
----------------------------------

The other people involved can complete their own application for an administrative review at the same time as they respond to your original application. We call this a 'cross-application' and you’ll have the opportunity to respond to it. 

Disagreeing with a decision from a child support review
-------------------------------------------------------

We cannot change the review decision once it has been issued to everyone involved in the review.

If you disagree with the review decision, you have the following options depending on your situation.

| Situation | Option |
| --- | --- |
| We did not accept your application because you did not meet the requirements. | You can apply to the Family Court for a departure order. |
| You applied for the administrative review and disagree with the review decision. | You can have the same grounds considered at the review looked at again by applying to the Family Court for a departure order. |
| You were the respondent to the administrative review and disagree with the review decision. | You can appeal the decision in the Family Court. The Court will then hear the original case. Appeals normally need to be lodged with the Family Court within 2 months. |
| There’s either a:<br><br>*   new ground or matter not considered by the review officer<br>*   change of circumstances since the last review. | You can apply for a new administrative review. |
| You were involved in the review and the review officer decided the matter was 'too complex'. | You can apply to the Family Court for a departure order. |

For more information about how to apply for a departure order or appeal a decision, read our guide Helping you to understand child support and the Family Court - IR174.

[Appeal an Inland Revenue decision - departure orders and appeals (justice.govt.nz)](https://www.justice.govt.nz/family/paternity-and-child-support/child-support/appeal-an-inland-revenue-decision/#appeal)

[Helping you to understand child support and the Family Court IR174 2020 (PDF 88KB) Download guide](/-/media/project/ir/home/documents/forms-and-guides/ir100---ir199/ir174/ir174-2020.pdf?modified=20240802001312&modified=20240802001312)

[Helping you to understand child support reviews IR175 2023 (PDF 649KB) Download guide](/-/media/project/ir/home/documents/forms-and-guides/ir100---ir199/ir175/ir175-2023.pdf?modified=20240717214128&modified=20240717214128)

* * *

Was this page helpful?

 Yes

 No

What did you like about this page?

 This isn't what I was looking for.

 There aren't enough examples.

 The information is hard to understand

 The information doesn't solve my issue.

 Other

Please tell us how we could improve this page?

Submit

**Thanks for sharing your opinion!** Your feedback has been received.

Sorry there was an issue submitting your feedback, please try again later.
[Skip to main content](#main-content-tt)

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2005

Issued

13 May 2005

Decision

13 May 2005

Appeal Status

Pending

Declaratory judgment on deemed value payments by fishers
========================================================

2005 case note - taxpayers successfully sought a declaratory judgment that deemed value payments are subject to GST – fisheries.

Case

Pacific Trawling Ltd & Forty South Ltd v the Chief Executive of the Ministry of Fisheries & the CIR

Legislative References

Fisheries Act 1983, Fisheries Act 1996, Goods and Services Tax Act 1985

### Summary

Pacific Trawling Ltd and Forty South Ltd successfully sought a declaratory judgment that deemed value payments made by fishers are subject to GST.

### Facts

The Crown regulates the commercial exploitation of fish species in New Zealand waters under what is known as the quota management system, which the Ministry of Fisheries ("the Ministry") administers. Under the quota management system, a commercial fisher may take and sell quota species only if it holds a valid fishing permit and a quota for a share of the total allowable commercial catch for the relevant species.

When fishing, a fisher frequently catches other quota species for which it does not hold quota. These fish are called by-catch. Both the Fisheries Act 1996 ("the 1996 Act") and its predecessor, the Fisheries Act 1983 ("the 1983 Act"), recognise that by-catch is inevitable, and seek to create incentives to minimise it and avoid wastage. A fisher is required to land by-catch, and may then process and sell it, but must also buy/lease quota to cover the by-catch, or make a "deemed value" payment to the Ministry. Deemed values for each quota species are set at a level that makes by-catch unprofitable, but creates an incentive to land the fish (dumping by-catch at sea is prohibited under both Acts).

The plaintiffs are commercial fishers who have held fishing permits and fish lawfully against quota owned by other firms. They called on the Chief Executive of the Ministry of Fisheries in November 2000 to issue tax invoices in respect of their deemed value payments. The Chief Executive assesses the deemed value of by-catch and administers the quota management system. The Commissioner of Inland Revenue was included in the proceedings because the plaintiffs sought a binding ruling from him under section 91E of the Tax Administration Act 1994. They abandoned it when it became clear that the ruling, if issued, would have been unfavourable.

### Decision

For the plaintiffs, Mr Cullen argued that a taxable supply is made when something is supplied in consideration for payment. He characterised that which the Ministry supplies in return for deemed value payments in various ways: as the right to keep and sell the fish, as 'authorisation' of the fisher's ownership of the fish, and as an entitlement to continue fishing without attracting prosecution (under the 1983 Act) or automatic suspension of a fishing permit (under the 1996 Act).

For the defendants, Mr Coleman responded that deemed value payments do not confer property rights since the fisher retains ownership of the fish throughout. They are not fees for services since no services are supplied, nor payments for statutory privileges. If anything, they are statutory demands analogous to levies. Lastly, imposition of GST would give rise to practical difficulties.

After covering the background to the GST Act 1985 and the deemed value regime, His Honour turned to consider what goods or services, if any, the Ministry supplies in return for the deemed value payments.

He concurred with the defendants' contention that ownership of fish, including by-catch, remained with the fisher whether or not deemed value payments were made. The payment did not, therefore, confer a right to keep and sell the fish.

However, Miller J noted that under the 1983 Act, payment of deemed values was part of a defence to what would otherwise be unauthorised possession and sale of by-catch (it being a strict liability offence to catch fish for which the fisher did not hold quota). That being so:

> "\[i\]t follows that something was indeed supplied in consideration for the payment, in the form of authority to keep and sell the by-catch covered by the payment where the fisher could also prove that it was genuine by-catch."

He went on to say that although the mechanism used to control by-catch under the 1996 Act is quite different (non-payment of deemed value payments results in suspension of the fishing permit), it too confers a right in return for payment of deemed values - the continued right to use the fishing permit.

As far as the defendants' submissions that the deemed value payments were analogous to a levy or a penalty were concerned, His Honour noted that nothing in the GST Act expressly excludes fines, levies or penalties from GST. Rather, they are excluded because they are not a taxable supply, in which a good or a service is provided in consideration for payment.

Justice Miller was not persuaded that the fact that payments are held on trust until the end of the year in any way altered the situation, and also dismissed the defendant's submissions that there would be practical difficulties in imposing GST on deemed value payments.

Report a Problem with this Page or Publication

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2005

Issued

13 May 2005

Decision

13 May 2005

Appeal Status

Pending
[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Decommissioning and archiving of systems, services and data
===========================================================

The decommissioning and archiving of legacy systems and data was carefully planned and funded as part of Business Transformation. In addition to delivering cost savings, this ensured the ethical and secure management of data.

A team of dedicated specialists
-------------------------------

More than 400 applications were identified to be decommissioned by the end of the transformation. A team was established in 2017 to focus solely on identifying dependencies, planning the decommissioning of legacy applications and services, and disposal of hardware and data as appropriate.

Taking a staggered approach
---------------------------

As new technology was progressively introduced, and tax and social policy products were moved over to the new system, the team started turning off the technology which was no longer required.

Continuous engagement with key internal and external stakeholders was a critical success factor of this work.

Decisions around data
---------------------

The team worked in partnership with system owners and users to understand what needed to happen to the data. Decisions were taken around whether data should be:

*   moved to the new system
*   archived in an appropriate system for a period
*   transferred to Archives NZ (New Zealand) for permanent retention, or
*   permanently and ethically deleted in line with legal requirements and Archives NZ Disposal Authorities standards.

Decommissioning the legacy core tax system
------------------------------------------

One of the more complex tasks of this workstream was switching off the old core tax system which had been in place for more than 30 years. Users of this system were given more than a year’s notice that it would be turned off, to ensure they were ready and able to support customers using the new system.

A full copy of the legacy database was archived to ensure any data not taken across to the new system was available if required. A limited number of people had access to this archive, but people could request access.

Identifying system connections and inter-dependencies
-----------------------------------------------------

Working within a complex technology landscape, the team had to carefully navigate multiple dependencies and connections between systems and had to ensure people who still used legacy applications understood what was changing and were prompted to use new technology. This took time and a great deal of collaboration between multiple parties.

Critical success factors
------------------------

A few key things contributed to the successful completion of this work:

*   Having the right people on board - people with deep knowledge and understanding of who owns which systems, and the inter-dependencies between systems.
*   Having people with the tenacity to work through what was in the data centre.
*   Having supportive leadership in place to guide and support the team.
*   Having the right governance forums in place.
*   Continuous engagement and coordination with people and teams across Inland Revenue.
*   Continuous information sharing, with full transparency of what was happening.

After more than 5 years, the team reached the final milestone on 31 March 2022 when the final few applications were turned off.

[Review and update approach for Decommission, Migration & Archive Pathways (PDF 626KB) Download exec summary](/-/media/project/ir/home/documents/about-us/bt-guide/delivering-the-transformation/support-and-transition/decommissioning-and-archiving/review-and-update-approach-for-decommission-migration-and-archive-pathways-executive-summary.pdf?modified=20220805034719&modified=20220805034719)

#### Topics

*   [Where we started](/about-us/business-transformation/where-we-started "Where we started")
    
*   [What we learnt](/about-us/business-transformation/what-we-learnt "What we learnt")
    
*   [Outcomes](/about-us/business-transformation/outcomes "Outcomes")
[Skip to main content](#main-content-tt)

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2015

Issued

2015

Decision

29 Jun 2015

Court

NZTRA

Appeal Status

Appealed

Deductibility of management fees/tax avoidance
==============================================

2015 case note – Decision of TRA in deductibility of management fees and tax avoidance - Section BD 2, s BG1, s 141D.

Case

TRA 013/10 \[2015\] NZTRA 10

Legislative References

Income Tax Act 1994, Tax Administration Act 1994

### Summary

The Taxation Review Authority ("TRA") found for the Commissioner of Inland Revenue ("the Commissioner") on the basis there was no evidence that management services were provided and that the Q Land Trust ("the Trust") incurred the management fees. The TRA was also satisfied the arrangement was one of tax avoidance.

### Impact

This decision confirms that a deduction is available only where the expenditure has the necessary relationship both with the taxpayer concerned and with the gaining or producing of his assessable income, or with the carrying on of a business for that purpose.

### Facts

The disputant is the corporate trustee of the Trust. The disputant challenged the Commissioner's assessment that disallowed $1,116,000 claimed as a deduction for a management fee expense paid by the disputant to Q Land Limited ("Land Limited") in the 2005 income tax year.

Mr X was the settlor and a discretionary beneficiary of the Trust. Mr X was also shareholder and director of the disputant.

The Trust purportedly undertook management services for related companies and trusts. The Trust did not have any employees and at all material times it used management services provided by Land Limited to manage its property and other business interests. There was no written management agreement between the Trust and Land Limited.

Mr X gave evidence that Land Limited incurred significant costs in undertaking management services for the Trust in the income tax year ended 31 March 2005. Mr X also gave evidence that Land Limited engaged Mr X and Mr Y through their respective management companies to provide management services. However, no formal agreements were executed in relation to the provision of these services.

The financial statements of the Trust for the 2005 year record management fees totalling $1,152,824 as an expense to the Trust. $1,116,000 of this sum is recorded as being management fees paid to Land Limited.

Without the management fee expense the Trust would have recorded income of $1,685,529 in the 2005 year. After the distribution of dividend income, the Trust would have had trustee income of $1,116,000 with tax to pay of $368,280. The management fee expense had the effect that the Trust then had no tax to pay.

The Commissioner disallowed the management fee expense on two grounds:

1.  that it was not incurred in the derivation of gross income, or necessarily incurred in the course of carrying on a business for the purpose of deriving the disputant's gross income and was not therefore deductible under s BD 2 of the Income Tax Act 1994 ("ITA"); or
2.  alternatively, if the management fee meets the requirement of s BD 2, it was part of a tax avoidance arrangement under s BG 1 of the ITA, which is void against the Commissioner for tax purposes.

The Commissioner also sought to impose a shortfall penalty for taking an abusive tax position or in the alternative, for taking an unacceptable tax position (in both cases reduced by 50%).

### Decision

#### _Deductibility under s BD 2 of the ITA_

Section BD 2(1)(b) of the ITA allows a taxpayer a deduction for an amount of expenditure or loss to the extent it is either:

1.  incurred by the taxpayer in deriving the taxpayer's gross income; or
2.  necessarily incurred by the taxpayer in the course of carrying on a business for the purpose of deriving the taxpayer's gross income.

The TRA referred to the relevant case law on deductibility which made it clear a deduction is available only where the expenditure has the necessary relationship both with the taxpayer concerned and with the gaining or producing of his assessable income, or with the carrying on of a business for that purpose.

The TRA agreed with the Commissioner's submission that an entry in the Trust's financial statements recording a management fee expense does not establish that management services were provided. It found there was no evidence of any company resolution or any agreement between the Trust and Land Limited for the charging of management services, and there was no invoice for the management fee or supporting accounts for any of the work allegedly done.

The TRA concluded that the management fee was not deductible under s BD 2 of the ITA. It was not satisfied on the evidence that management services were provided and that the management fee was incurred by the Trust. Accordingly, it was not satisfied that there was the requisite nexus between the management fee of $1,116,000 (or any part thereof) and the gaining or producing of the Trust's assessable income or the carrying on of its business.

#### _Tax avoidance_

The TRA went on to consider whether the transaction is part of a tax avoidance arrangement under s BG 1 of the ITA, in the event it was wrong in finding the management fee was not deductible under s BD 2.

The TRA stated that the general avoidance provision does not confine the court as to the matters that may be taken into account when considering whether a tax avoidance arrangement exists.

The TRA found the whole transaction to be contrived and artificial and that it made no commercial sense. It was satisfied that one of the purposes of the arrangement was the avoidance of tax. Accordingly, the TRA was of the view that the tax avoidance purpose or effect of the arrangement was not merely incidental and as such, the arrangement is void against the Commissioner in accordance with s BG 1.

The TRA was also satisfied that the disallowance of the deduction claimed by the Trust was the only step required to be taken by the Commissioner to counteract the tax advantage.

#### _Shortfall penalty_

The TRA considered that it could not be said (on any basis) that when viewed objectively the tax position adopted by the disputant was "about as likely as not to be correct".

The TRA was satisfied that when viewed objectively under either the deductibility provisions or an anti-avoidance arrangement, the transaction had a dominant purpose of avoiding tax. Accordingly, the TRA imposed a shortfall penalty under s 141 D of the TAA for taking an abusive tax position reduced by 50% for previous good behaviour under s 141FB.

Report a Problem with this Page or Publication

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2015

Issued

2015

Decision

29 Jun 2015

Court

NZTRA

Appeal Status

Appealed
[Skip to main content](#main-content-tt)

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2011

Issued

2011

Decision

25 Jan 2011

Court

NZTRA

Appeal Status

Not appealed

Deductibility of share losses
=============================

2011 case note – loss of overseas shares - share speculation, partnership loss, deductible, valid or real shares, loan by family trust.

Case

TRA 37/08

Legislative References

Income Tax Act 1994

### Summary

The partnership invested in shares overseas and eventually lost all that was invested. The partnership claimed the loss and the partners to the partnership each claimed the deduction. The Commissioner denied the claim. The Taxation Review Authority ("TRA") found the expenditure was on revenue account and deductible.

### Impact of decision

The TRA has taken a broad view on what constitutes a business. The TRA has also taken the view that the disputant using funds from the Family Trust without authority did not mean there was no loan. This case also follows the reasoning in _Inglis_ and _Stockwell_ whereby, if shares are purchased with the intention of selling to make a profit, any loss will be deductible.

### Facts

The taxpayer is a husband and wife partnership. The husband received a "cold call" from overseas brokers offering the opportunity to invest in shares. The brokers were extremely convincing, persuasive and persistent. The modus operandi of the brokers was to purchase undervalued shares in companies in the United States and then persuade overseas persons to buy those shares at a highly inflated price. The brokers promised the buyers that they would be able to sell the shares at a profit after the shares became publicly listed on the American Stock Exchange.

Over a period of about three years from 1999 to 2002, the disputant purchased shares in five USA companies at a total cost of about $1.1 million.

While the shares were purchased in the name of the partnership, the funds used to pay for the shares came from the Family Trust.

Eventually, after ongoing difficulty in obtaining share certificates and responses to his request for information, the partners realised that the money spent had been lost.

The partnership claimed the loss in its 2003 income year and each partner claimed $627,564 as their half share of the partnership loss. The Commissioner denied the deductions and imposed a shortfall penalty on both the husband and the wife for having taken an unacceptable tax position.

### Decision

It was put to the TRA by the Commissioner that the disputant could not demonstrate that it acquired any such shares or incurred any such loss. The Commissioner claimed that the shares did not exist and it was the Family Trust that paid for the shares, not the disputant. Also, that there was no agreement between the disputant and the Trust for the lending of the money.

However, the TRA found that the disputant did incur a loss and that real shares were purchased by the disputant, which became worthless by late 2003.

Judge Barber concluded that the partnership borrowed the money from the Trust:

> ... Much was made in submissions as to whether the Trust could have been the shares purchaser in reality, or as a result of a resulting Trust or an agency or something like that; but with a complete absence of records as to any funding contract from the Trust to the partnership, I consider that the partnership simply borrowed money from the Trust, possibly, on an unauthorised basis without clear terms and without any arrangements for payment of interest by the disputant partnership to the Trust \[10\].  
> It seems to me that the disputant partnership acquired funds (mainly by borrowing from the Family Trust) and, at all material times, owned the funds which it applied to the share purchases listed above ... \[42\].

Judge Barber found that real shares were acquired by the disputant:

> I understand that, until the hearing before me, the defendant Commissioner had not been prepared to accept that \[...\] Groups sold real shares to the disputant, and considered that the so-called brokers had simply misappropriated the disputant's funds. However, the hearing before me showed that the disputant did receive real shares and these were known as Regulation S shares ... \[60\].

The relevant sections in regards to whether losses are deductible are sections BD 2 and CD 4 of the Income Tax Act 1994. The leading authorities on the deductibility of losses incurred in respect of shares to which section CD 4 applies are _CIR v Inglis_ \[1993\] 2 NZLR 29 (CA) and _CIR v Stockwell_ \[1993\] 2 NZLR 40 (CA).

Judge Barber considered whether the disputant was operating a business of trading in shares. His Honour considered that it seemed that there was sufficient activity on the part of the disputant regarding those speculative investments for the activity to amount to a business, when coupled with the intention of seeking fairly quick profit, and that those investments were real. While the husband admitted to the Inland Revenue investigator that he was not carrying on a business of share dealing, Judge Barber said that that was an issue for the Court to decide.

However, Judge Barber said that the point was peripheral in this case because he considered that the partnership had the dominant intention of purchasing the shares for a fairly speedy resale at a profit. Judge Barber concluded:

> The evidence is clear that the speculative share purchase transactions were entered into by the disputant with a view to profit for the partners ... \[11\].  
> The evidence is that the partners purchased the shares with the intention of soon selling them at a profit, as promised by the high powered broker vendors \[13\].  
> I find from the evidence adduced to me that the husband purchased the shares listed above for the disputant with the intention of the disputant very soon selling the shares at a profit after they became publicly listed on the American Stock Exchange \[47\].

Therefore, the TRA found expenditure was on revenue account and deductible.

Report a Problem with this Page or Publication

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2011

Issued

2011

Decision

25 Jan 2011

Court

NZTRA

Appeal Status

Not appealed
[Skip to main content](#main-content-tt)

[Taxation (Tax Administration and Remedial Matters) Act 2011](/new-legislation/act-articles/taxation-tax-administration-and-remedial-matters-act-2011 "Taxation (Tax Administration and Remedial Matters) Act 2011")

Deductibility of use-of-money interest
======================================

2011 amendments clarify that use-of-money interest (UOMI) payable to IR is deductible for tax purposes and the deduction is made in the year the UOMI is paid.

**Deductibility of use-of-money interest**

_**Sections DB 3B, EF 4, EF 5 and EF 6 of the Income Tax Act 2007; section DB 3B of the Income Tax 2004; section DB 2 of the Income Tax 1994; and section 184AA of the Tax Administration Act 1994**_

The amendments clarify that use-of-money interest (UOMI) payable to Inland Revenue is deductible for tax purposes and the deduction is made in the year the UOMI is paid.

### Background

The penalty and interest rules have applied since the 1997-98 income year. The policy intention of the interest rules was that interest paid on overpayments of tax would be taxable, and interest charged on underpayments of tax would be deductible under the normal income tax rules. This approach provided consistency with the treatment of interest generally, removed the need to convert rates to after-tax rates and distinguished between penalties and interest. Furthermore, the discussion documents released before the introduction of the rules noted interest would be deemed to be interest on money lent for the purposes of determining whether a deduction was available under the Income Tax Act. This was, however, never specified in the legislation.

Over time questions were raised as to whether UOMI was in fact deductible. This led to a number of taxpayers seeking case-specific rulings from Inland Revenue on this issue. There appeared to be some inconsistency over whether interest is deductible for companies and individuals. Generally companies were automatically entitled to deduct interest, but other taxpayers (specifically individuals) needed to satisfy a nexus with assessable income requirement - meaning that interest may not have been deductible. This inconsistency arose as a result of a lack of clarity over what Parliament's intention was on the nexus requirement and resulted in calls for legislative clarity on the deductibility of UOMI.

### Key features

The amendments clarify that UOMI is deductible for tax purposes. The amendments ensure consistency, in particular between companies (for whom interest was typically always deductible) and individuals. The amendment also ensures symmetry in treatment for tax purposes so that UOMI is both taxable and deductible.

The provisions setting out which period the deduction is allocated to have also been amended. Previously the UOMI deduction was allocated to the same year to which the tax liability relates, the following year or to the income year following the income year in which the Commissioner issues the notice of amended assessment. This meant that if there was a dispute involving court proceedings which was eventually resolved in the Commissioner's favour, the previous rules could inappropriately allocate the deduction to a year many years earlier than the year in which the interest is paid. The previous rules could also inappropriately allocate the deduction to the year of assessment in cases when the taxpayer simply failed to pay any relevant tax and the UOMI may not be paid until much later (if at all).

The timing provisions have been amended to provide for the deduction of UOMI in the year in which the UOMI is paid. This approach provides taxpayers with certainty on this issue and deals appropriately with the problematic cases described previously. Importantly, a paid approach is also consistent with the timing of assessability, that is, UOMI is assessable in the year the Commissioner pays the interest.

The amending provisions override the capital limitation, the employment limitation and the private limitation. This means the provision is consistent with section DB 3 (which allows for the deduction of expenditure incurred in calculating or determining tax liabilities).

Under section RM 2 of the Income Tax Act 2007, the Commissioner may refund tax if the four-year period for the amendment of an assessment has not ended. The four-year period can be extended to eight years in certain circumstances, for example, if the refund arises from a clear mistake or simple oversight of the taxpayer. These amendments apply retrospectively from the 1997-98 income year (the start of the UOMI rules). Therefore the time limitations on the Commissioner refunding tax do not apply to prevent these amendments being effective.

### Application dates

The amendments clarifying the deductibility of UOMI apply retrospectively from the 1997-98 income year (the start of the UOMI rules) for taxpayers who have claimed deductions for UOMI in returns filed or notices of proposed adjustment issued before the date of introduction of the amending legislation, that is 24 November 2010. These amendments also apply generally to the 2010-11 and later income years.

The amendments to the timing provisions for UOMI deductions apply for the 2011-12 and later income years.
[Skip to main content](#main-content-tt)

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2014

Issued

2014

Decision

09 Dec 2014

Court

NZTRA

Appeal Status

Appealed

Deduction denied following cessation of property development business
=====================================================================

2014 case note – deduction of expenses denied following cessation of property development business – resource consent.

Case

TRA 008/13 \[2014\] NZTRA 17

Legislative References

Tax Administration Act 1994, Income Tax Act 2007, Resource Management Act 1990

### Summary

The taxpayer entered into a sale and purchase agreement to purchase land for the purpose of undertaking a large retail and residential development. The taxpayer obtained resource consent to build the development but the sale and purchase agreement was cancelled following civil litigation between the taxpayer and the vendor of the land. The taxpayer sought to deduct all expenses incurred in relation to the land and subsequent court proceedings with the vendor. The Commissioner of Inland Revenue ("the Commissioner") denied deductions incurred after the taxpayer had sought to cancel the agreement for sale and purchase on the basis it was no longer in business, as it did not have the intention to make a profit once it sought to extricate itself from the agreement.

### Impact of decision

The Taxation Review Authority ("TRA") has confirmed that deductions will not be available after the cessation of a business.

### Facts

The disputant entered into a sale and purchase agreement ("the Agreement") in February 2006 for a block of land ("the Land") from AB Limited ("the Vendor").

The Agreement was conditional on the Vendor obtaining resource consent for the subdivision of a larger property to be able to provide title to the Land. The disputant and the Vendor subsequently agreed to extend the date for the satisfaction of this condition.

On 10 March 2008, the Vendor's lawyers wrote to the disputant's lawyers recording that the condition relating to the subdivision had not been satisfied and therefore the Agreement was at an end. On 17 March 2008, the disputant's lawyers replied stating that it did not accept the Vendor's purported cancellation of the Agreement.

On 23 April 2008, the disputant was granted resource consent for land use to build a mixed retail/apartment development on the Land.

On 1 May 2008, the disputant issued proceedings against the Vendor seeking an order for specific performance of the Agreement.

On 2 July 2008, resource consent for the subdivision of its property was granted to the Vendor. On 24 July 2008, the disputant's lawyers replied to the vendor stating that "our client now accepts the unlawful termination as repudiation and the contract is therefore at an end subject to the right to seek damages for losses incurred".

The disputant initiated court proceedings in the High Court for specific performance of the Agreement, but later amended its claim (after the contract was declared unconditional) to seek damages from the Vendor. Those proceedings were settled in December 2010.

On 9 December 2011, the disputant entered into an agreement to sell the documentation and resource consent rights related to the project ("the Project Rights Agreement"). However, the Project Rights Agreement did not proceed and the resource consent for land use eventually expired on or about 5 March 2013.

The Commissioner disallowed all income tax deductions claimed by the disputant after 24 July 2008 on the basis that the disputant was not in business after the date it sought to cancel the Agreement.

The disputant claimed that its business did not cease until on or about 5 March 2013 when the resource consent rights for the project expired or when the parties entered into a settlement agreement in December 2010. Alternatively, it argued the expenditure was deductible as a revenue expense.

### Decision

The Commissioner's assessments for the 2009, 2010 and 2011 years were confirmed and the imposition of a shortfall penalty for the 2011 year was upheld.

#### _Cessation of business_

The TRA found the disputant's focus clearly changed after 24 July 2008 and its time, effort and resources moved from advancing settlement of the purchase of the Land to getting out of the Agreement and recovering the deposit and costs incurred. The TRA did not accept that there was any temporary cessation of business by the disputant after 24 July or that the disputant had any expectation of resuming its business of property development following the High Court proceedings between the disputant and the Vendor.

The TRA dismissed the disputant's alternative argument that it ceased being in business after the cancellation of the Project Rights Agreement in December 2011 or on the expiry of the resource consent. It recognised that the disputant's business was that of property development and not one of selling resource consents.

#### _Land held on revenue account_

The disputant also argued that the Land was acquired for the purpose of resale and was therefore held on revenue account. It contended that any gains derived by the disputant would have been taxable under ss CB1, CB3, CB6 or CB7 of the Income Tax Act 2007 ("ITA"). Taxable profit could have been derived from the sale of its equitable interest in the Land, the sale of the Land, damages awarded in the High Court proceeding or from the sale of the resource consent and plans.

The disputant went on to argue that, accordingly, any expenses incurred are on revenue account and deductible under s DA1(1)(a) of the ITA. This would include at \[60\]:

1.  a payment made by the disputant to escape an onerous agreement; or
2.  a loss of the disposal of equitable rights in and to the land; or
3.  a payment of damages.

The TRA did not consider there to be sufficient nexus between the expenses claimed and any income-earning process undertaken by the disputant. It found that the disputant's payment was to escape the onerous contract after the business had ceased. Furthermore, the only income the disputant earned after 24 July 2008 was interest on the deposit paid. The TRA agreed with the Commissioner that there was no nexus between the disputant's deriving or earning its interest income and the expenditure incurred to extract itself from the Agreement.

The TRA found no income was derived from disposing of the land and therefore s CB6 of the ITA did not apply.

Finally, the TRA did not accept the disputant's argument that payment of damages is an "occupational hazard for property developers" and is therefore an "expected expense".

#### _Expenses incurred before business ceased_

The disputant argued that as it paid the deposit of $1,942,655 on 1 June 2007, the loss related to the forfeiture of part of the deposit was an expense to which the disputant had been legally committed from that date (being at a time when the disputant was in business) as were some of the legal fees.

The TRA dismissed this argument, finding there was not sufficient nexus under s DA1(1)(a) of the ITA for two reasons. First, the legal fees were incurred by the disputant trying to get out of the property development project. Second, the settlement sum paid to the Vendor was a negotiated amount paid from the deposit monies held by the disputant's lawyer as stakeholder rather than payment of the deposit.

#### _Section CG4 of the Income Tax Act 2007_

At the end of the hearing on 6 August 2014, Mr Carruthers, for the disputant, made oral submissions on the possible application of s CG4 of the ITA. The TRA found that this was a new proposition of law and no explanation has been provided as to why this was not included in its statement of position, meaning it did not need to consider it.

However, the TRA considered the argument and found the disputant was not able to claim a deduction for its legal fees in reliance on s CG4 as the disputant was not in the business of civil litigation, and as such, there was no nexus.

#### _Shortfall penalty_

The TRA determined that this case involved the application of established principles and did not raise any novel points of law. In its view, the disputant's claim for deductions for the expenditure incurred in the 2011 income tax year did not have any prospect of being close to a 50% chance of success. Accordingly, the disputant failed to meet the standard of being "about as likely as not to be correct" and is liable for an unacceptable tax position shortfall penalty.

Report a Problem with this Page or Publication

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2014

Issued

2014

Decision

09 Dec 2014

Court

NZTRA

Appeal Status

Appealed
[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Deduction notices: collecting taxes from taxpayers who refuse to pay
====================================================================

Most taxpayers pay their taxes in full and on time.

But sometimes people have difficulty paying by the due date. We understand life happens, and we'll do everything we can to help the taxpayer get back on their feet.

We often work with taxpayers to arrange a payment plan that fits their budget.

Even then, some taxpayers still do not pay their taxes. When our offers of assistance are not taken up, we may then collect the amount owing by sending out a deduction notice.

What is a deduction notice?
---------------------------

When a taxpayer has unpaid taxes, we can send a deduction notice to a third party, such as an employer or a bank, that owes money to the taxpayer. The deduction notice requires the third party to pay the money to Inland Revenue instead.

What if you receive a deduction notice?
---------------------------------------

If you receive a deduction notice, you need to deduct the amount shown ‒ before you make any further payments to the taxpayer ‒ and pay the money to Inland Revenue.

The deduction notice tells you how to pay and explains your legal obligations.

We'll send a copy of the deduction notice to the taxpayer if we have their current address.

If the taxpayer was an employee and they have left your employment, make sure you have entered a cease date on your employment information.

How much do you deduct?
-----------------------

The deduction notice will tell you how much to deduct (up to a maximum ‒ see the next section) and if you need to pay a lump sum or instalments.

These deductions are in addition to the usual PAYE, student loan, child support or KiwiSaver deductions.

Please note the deduction notice will continue to apply until the full amount has been paid, or we ask you (in writing) to stop making deductions.

Maximum deductible amount
-------------------------

You may need to deduct less money than the amount shown on your deduction notice, to ensure the taxpayer has enough left over for living expenses.

The maximum you can deduct is the lesser of:

*   10% of the tax debt, or
*   20% of the gross salary or wages payable to the taxpayer on payday.

The minimum deduction is $10 per week.

Please note this maximum applies to overdue income tax, GST, student loan repayments and gaming duty. There's a different calculation for child support ‒ see more information in the next section.

You can find a worked example of an income tax deduction in the first blue box at the bottom of the page.

Maximum deductible amount for child support
-------------------------------------------

Child support has priority over other deductions.

The maximum child support you can deduct is the lesser of:

*   the total amount of the child support owing, or
*   40% of the after-tax amount of any salary or wages payable to the taxpayer on payday.

The minimum deduction is $10 per week.

If the taxpayer has other overdue tax, that will be dealt with separately.

You can find a worked example of a child support deduction in the second blue box at the bottom of the page.

How to pay the deductions to Inland Revenue
-------------------------------------------

If you receive a deduction notice, you should deduct the money, keep it separate from normal PAYE deductions, and pay it to Inland Revenue by the end of the month.

Please ensure you pay on time. If you have any questions or cashflow problems, do get in touch with us. We're here for you and ready to help.

If you don't get in touch and you don't make deductions and pay them to us by the end of the month, you'll become liable for the amount owed. You may also face prosecution action.

When do you stop making deductions?
-----------------------------------

The deduction notice will continue to apply until the full amount has been paid, or we ask you (in writing) to stop making deductions.

What if the taxpayer asks you about the deduction notice?
---------------------------------------------------------

If the taxpayer has questions about the deduction notice, ask them to contact us directly. The taxpayer has no authority to cancel their deduction notice.

More information
----------------

If you'd like to know more about deduction notices, see our standard practice statement:

[SPS 21/01 Deduction notices](https://www.taxtechnical.ird.govt.nz/standard-practice-statements/processing/sps-21-01)

Example: Deduction notice for income tax

Kerry has overdue income tax of $3,000 but refuses to make arrangements to repay the debt.

We send Kerry's employer a deduction notice requiring a deduction of the lesser of $300 (10% of the tax debt) or 20% of Kerry’s gross wage.

Kerry earns a gross weekly wage of $900 and 20% of this figure comes to $180.

Every week, the employer deducts $180 from Kerry's wage.

Example: Deduction notice for child support

Michael has overdue child support of $3,000 but refuses to make arrangements to repay the debt.

We send Michael's employer a deduction notice requiring a deduction of the lesser of $3,000 or 40% of Michael’s wage after PAYE is deducted.

Michael earns a weekly wage of $800 (after PAYE deductions) and 40% of this figure comes to $320.

Every week, the employer deducts $320 from Michael's wage.

#### Roles

*   [Employers](/roles/employers "Employers")
[Skip to main content](#main-content-tt)

[Questions we've been asked](/publications#f-ttTypeFacet=Questions%20we've%20been%20asked&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2005

Issued

01 Apr 2005

Deductions from GST output tax for subsequent changes to taxable use (April 2005)
=================================================================================

QB (Apr 2005) clarifies the tests that must be met before a registered person can make deductions from GST output tax for change from non-taxable to taxable use.

We have been asked to clarify the tests that must be met before a registered person can make deductions from GST output tax for change from non-taxable to taxable use under section 20(3)(e) of the Goods and Services Tax Act 1985 ("the GST Act"). This includes discussion of the requirements under section 21E, amount of deductions under section 21F and timing of deductions under sections 21G and 21H.

(Note: All legislative references in this item are to the GST Act.)

### Introduction

In 2000, sections 21E to 21H were inserted into the GST Act. Section 20(3)(e) allows registered persons to make deductions from GST output tax, provided that the tests in section 21E are met and the amount of deductions can be determined under section 21F. Sections 21G and 21H set out when the deductions can be claimed. The policy statements on these legislative provisions were originally set out in _Tax Information Bulletin_ Vol 12, No 12 (December 2000).

This item clarifies some issues surrounding the application of sections 21E through to 21H. In particular, for section 21F to apply, sections 21E(2) and 21E(3) are no longer considered to be cumulative requirements.

The following application of the legislation represents the current practice of the Commissioner.

### Application of the legislation

The purpose of section 21E is to specify the deductions from GST output tax allowed under section 20(3)(e) for changes from non-taxable to taxable use for:

1.  goods and services acquired or imported by the registered person on which GST has been charged; and  
      
    
2.  some acquisitions of secondhand goods.

Where the tests in section 21E are met, section 21F applies to determine the amount of deduction from GST output tax allowed under section 20(3)(e).

The requirements for claiming deductions from GST output tax under sections 21E and 21F will apply in relation to changes to taxable use from 1 October 1986, unless a claim for deduction under section 20(3) has been made (whether in a GST return or under the disputes procedures under Part IVA of the Tax Administration Act 1994) and the Commissioner:

1.  has not been notified of the claim, other than by way of inclusion in the registered person's return, and on this basis has not queried the claim in writing before 16 May 2000; or  
      
    
2.  has not queried the claim in writing before 16 May 2000 but has agreed in writing to the claim before 16 May 2000; or  
      
    
3.  has queried or considered the claim in writing before 16 May 2000 but has agreed in writing to the claim before 16 May 2000.

### Change of use in respect of services and non-secondhand goods

A registered person who has acquired services and non-secondhand goods can make deductions from GST output tax under section 20(3)(e) of the amount allowed under section 21F, if the following requirements in sections 21E(1)(a), 21E(1)(b) and 21E(2) are met:

1.  The goods and services were acquired on or after 1 October 1986 for a principal purpose other than that of making taxable supplies. (See section 21E(1)(a))  
      
    Pursuant to section 21E(4), some goods and services are treated as if they were acquired for the principal purpose other than that of making taxable supplies. Generally, section 21E(4) applies if:  
      
    
    1.  section 21 or 21I have treated goods and services (including fringe benefits and entertainment under section 21I) as being supplied by the registered person; or  
          
        
    2.  goods and services are deemed to have been supplied by a person who ceased to be registered for GST under section 5(3) and the goods or services are subsequently applied by that person for a purpose of making taxable supplies; or  
          
        
    3.  goods and services are deemed to have been supplied by a person who ceased to be registered for GST under section 5(3) and the goods or services are subsequently applied by a partnership of which the person is a partner for a purpose of making taxable supplies.
    
      
    
2.  The goods and services are then applied for a purpose of making taxable supplies by the registered person, being either the taxpayer or a partnership of which the taxpayer is a member. (See section 21E(1)(b))  
      
    This means that section 21F may apply if a partner, on behalf of a partnership, acquires or imports the goods and services for non-taxable purposes and then applies them in the partnership for a purpose of making taxable supplies.  
      
    
3.  The goods or services when acquired by the person must have been subject to GST under section 8(1). (See section 21E(2)(a))  
      
    Alternatively, in the case of imported goods, GST must have been levied under section 12(1) on the importation of the goods by the person. (See section 21E(2)(b))

### Change of use in respect of secondhand goods

Where a registered person acquires secondhand goods and changes the use of the goods from non-taxable to taxable, the registered person can claim deductions from GST output tax under section 20(3)(e) in relation to the secondhand goods of the amount allowed under section 21F, if all of sections 21E(1)(a), 21E(1)(b) and 21E(3) are met.

Sections 21E(1)(a) and 21E(1)(b) are discussed above. There are four requirements under section 21E(3):

1.  The secondhand goods were supplied to the registered person by way of sale;  
      
    
2.  The secondhand goods that were sold to the registered person have always been situated in New Zealand, or in the case of imported goods, have been subject to GST under section 12(1) when imported.  
      
    
3.  The supply to the registered person was not a taxable supply (that is, GST was not charged on that supply).  
      
    
4.  The goods have not been supplied to another GST registered person who is the importer of the goods.

### Amount of deduction under section 21F

If the requirements under section 21E are met, the person or partnership to whom the goods and services are supplied will be allowed to make a deduction from GST output tax under section 20(3)(e) of the amount allowed under section 21F. The amount of the deduction equals the product of the tax fraction of the lesser of:

1.  The cost of the goods and services, including any tax charged or input tax deduction claimed for the goods and services; and  
      
    
2.  The open market value of the supply of the goods and services, multiplied by the percentage extent to which the goods or services are applied for the purpose of making taxable supplies.

### Timing of deduction from output tax as calculated under section 21F

Section 21G sets out when a registered person can make a deduction from output tax, as calculated under section 21F. In general, a registered person may make the deduction in each taxable period or in each year in which goods and services are applied for a purpose of making taxable supplies (at the registered person's election).

However, this general timing rule is subject to some exceptions:

1.  Where the goods are capital assets with a cost of less than $18,000, the registered person may make a single deduction from output tax in the taxable period in which the goods are applied for a purpose of making taxable supplies.  
      
    
2.  Under section 21H, where the goods and services cost $18,000 or more the registered person may apply to the Commissioner to make a single deduction from output tax in the taxable period in which the goods and services are wholly applied for a purpose of making taxable supplies. Acceptance of the registered person's application is at the Commissioner's discretion, although in making his determination the Commissioner must have regard to the factors set out in section 21H(3).

Report a Problem with this Page or Publication

[Questions we've been asked](/publications#f-ttTypeFacet=Questions%20we've%20been%20asked&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2005

Issued

01 Apr 2005
[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Ngā tangohanga mai i ngā moni ā-tau me ngā moni ā-wiki Deductions from salary and wages
=======================================================================================

Employees need to give you a completed IR330 - Tax code declaration. The tax code your employee uses will depend on the work type and their situation.

If your employee does not give you a completed IR330, you need to deduct PAYE at the 45% non-notified rate.

If we notice that one of your employees is using the wrong tax code, we'll write to you. This letter will tell you what their code should be. You'll need to start using the correct code and deduct tax based on that code.

Making deductions
-----------------

When you pay an employee their salary or wages, you will need to make deductions for:

*   PAYE
*   child support
*   student loan repayments
*   KiwiSaver employee contributions 
*   KiwiSaver employer net contributions 
*   [employer superannuation contribution tax (ESCT)](/api/glossary/item?id={B1FC84AD-4393-48A3-92EF-2EF29C640520})
    . 

If we need you to deduct child support, we’ll tell you how much to deduct and when to start deducting. These deductions will then need to be paid to us.

If you file your employment information electronically, you can offer payroll giving to your employees. You deduct the employee's donation each payday and pass it on to the approved charity.

Child support and protected net earnings
----------------------------------------

If you’re deducting child support from an employee's pay, the maximum amount of child support you can deduct is 40% of their net earnings (after tax). This is called ‘protected net earnings’. Protected net earnings are usually only affected if you’re paying an employee less than their usual pay, for example, if they take unpaid leave.

Protected net earnings only apply to child support. Other deductions should still be made even if these add up to more than 40% of their pay.

For more protected net earnings information, download the IR335 - Employer's guide below.

If the child support deduction we’ve asked you to make is more than 40% of your employee's net pay, you should only deduct 40% of their net pay amount. We will arrange with your employee to pay the balance, so you do not need to make up the missing amount in future pays.

Child support codes
-------------------

If the child support amount you deduct is different to the amount we asked for, we need to know why to make sure we update the liable parent’s account correctly. It’s important that you provide a variation code on the employment information form if one applies.

Work out the right variation code to use

The amount is different because...

Select the situation that applies to you Ceased employment - Employee ended employment Other - None of the other situations apply Payment in advance - The employee was paid in advance Previously deducted - Advance payment was made Protected earnings - Payment is more than 40% of net earnings Short-term absences - Employee took temporary unpaid leave

Use the following variation code

Variation code: C

If an employee stops working for you, deduct child support only from the last full pay you gave them, and from any holiday pay owed. If this code is used, we can remove the employee from your records.

Variation code: O

If none of the other variation codes can be used to explain why the child support deducted does not equal what was expected, enter 'O' as the variation code.

Variation code: A

Sometimes you may pay an employee in advance. In this case, deduct the same amount of child support as you would if you were paying the employee on the usual payday. You must include the child support with the deductions for the period when the employee was given the advance pay. Your child support will be more than usual for that period.

Variation code: D

Sometimes the full amount of child support requested from an employee's wages may not be deducted because you made an advance payment. Your child support will be less than usual for that period.

Variation code: P

If you're unable to deduct the full amount of child support requested from an employee's wages due to protected net earnings.

Variation code: S

If an employee is off work on unpaid leave for a short period of time and you're unable to deduct any or all the child support requested.

[KiwiSaver employer guide KS4 2020 (PDF 452KB) Download guide](/-/media/project/ir/home/documents/forms-and-guides/ir1---ir99/ks4/ks4-2020.pdf?modified=20220330224517&modified=20220330224517)

[KiwiSaver for employers KS9 2020 (PDF 42KB) Download guide](/-/media/project/ir/home/documents/forms-and-guides/ir1---ir99/ks9/ks9-2020.pdf?modified=20210929004746&modified=20210929004746)

[Meeting your employer obligations for KiwiSaver KS45 2022 (PDF 54KB) Download form](/-/media/project/ir/home/documents/forms-and-guides/ir1---ir99/ks45/ks45-2022.pdf?modified=20220330221159&modified=20220330221159)

[Employer's guide IR335 Nov 2024 (PDF 1MB) Download guide](/-/media/project/ir/home/documents/forms-and-guides/ir300---ir399/ir335/ir335-2024-nov.pdf?modified=20241107235439&modified=20241107235439)

5 minutes

PAYE deductions from salary or wages calculator

Employers and employees can work out how much PAYE should be withheld from wages.

[Go to this tool](https://myir.ird.govt.nz/tools/?LINK=CLCPAYE)

[Weekly and fortnightly PAYE deduction tables IR340 Aug 2024 (PDF 3MB) Download guide](/-/media/project/ir/home/documents/forms-and-guides/ir300---ir399/ir340/ir340-2025.pdf?modified=20240821033750&modified=20240821033750)

Previous years - IR340

[Apr 2025 IR340 (PDF 3MB) Download guide](/-/media/project/ir/home/documents/forms-and-guides/ir300---ir399/ir340/ir340-apr-2025.pdf?modified=20240821040645&modified=20240821040645)
 [2024 IR340 (PDF 3MB) Download guide](/-/media/project/ir/home/documents/forms-and-guides/ir300---ir399/ir340/ir340-24.pdf?modified=20240821040654&modified=20240821040654)
 [2023 IR340 (PDF 3MB) Download guide](/-/media/project/ir/home/documents/forms-and-guides/ir300---ir399/ir340/ir340-2023.pdf?modified=20240821040704&modified=20240821040704)
 [2022 IR340 (PDF 2MB) Download guide](/-/media/project/ir/home/documents/forms-and-guides/ir300---ir399/ir340/ir340-2022.pdf?modified=20240821040715&modified=20240821040715)

[Four weekly and monthly PAYE deduction tables IR341 Aug 2024 (PDF 3MB) Download guide](/-/media/project/ir/home/documents/forms-and-guides/ir300---ir399/ir341/ir341-2025.pdf?modified=20240821040743&modified=20240821040743)

Previous years - IR341

[Apr 2025 IR341 (PDF 3MB) Download guide](/-/media/project/ir/home/documents/forms-and-guides/ir300---ir399/ir341/ir341-apr-2025.pdf?modified=20240821040724&modified=20240821040724)
 [2024 IR341 (PDF 3MB) Download guide](/-/media/project/ir/home/documents/forms-and-guides/ir300---ir399/ir341/ir341-2024.pdf?modified=20240821040735&modified=20240821040735)
 [2023 IR341 (PDF 4MB) Download form](/-/media/project/ir/home/documents/forms-and-guides/ir300---ir399/ir341/ir341-2023.pdf?modified=20240821015855&modified=20240821015855)
 [2022 IR341 (PDF 2MB) Download guide](/-/media/project/ir/home/documents/forms-and-guides/ir300---ir399/ir341/ir341-2022.pdf?modified=20240821015855&modified=20240821015855)

#### Topics

*   [Tax codes and tax rates for individuals](/income-tax/income-tax-for-individuals/tax-codes-and-tax-rates-for-individuals "Tax codes and tax rates for individuals")
    
*   [Paying deductions to Inland Revenue](/employing-staff/payday-filing/paying-deductions-to-inland-revenue "Paying deductions to Inland Revenue")
[Skip to main content](#main-content-tt)

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2010

Issued

2010

Decision

19 Mar 2010

Appeal Status

Pending

Default assessments are inevitable where returns are not filed
==============================================================

2010 case note - confirms that there are obligations on everyone to pay tax, irrespective of race - default assessments, confidentiality, NZ Bill of Rights.

Case

John David Hardie v Commissioner of Inland Revenue

Legislative References

Tax Administration Act 1994, Income Tax Acts, Goods and Services Tax Act 1986, Bill of Rights Act 1990

### Summary

The appellant appealed unsuccessfully against a District Court decision which held the Commissioner could recover unpaid taxes and penalties of $10,341,410.32.

### Impact of decision

This judgment confirms that there are obligations on everyone to pay tax, irrespective of race. It also confirms that when a taxpayer fails to file a return the Commissioner can issue default assessments.

### Facts

This is an appeal by the taxpayer against the District Court decision of Judge Recordon.

The taxpayer had failed to file his relevant tax returns and the Commissioner made default assessments. The taxpayer failed to exercise his right to challenge those default assessments pursuant to section 89D of the Tax Administration Act 1994. The District Court granted the Commissioner judgment by default for $10,341,410.32.

### Decision

In the High Court, his Honour Stevens J began with considering the taxpayer's request to have the hearing and subsequent judgment subject to total confidentiality orders.

The Court rejected this. It did not consider that any exceptional circumstances in this case outweighed the principle of open justice. The Court then went through each of the grounds of appeal.

First, whether the taxpayer ceased to be an employer from March 2004. The Commissioner conceded this issue in favour of the taxpayer. The appeal was, therefore, allowed in part to the extent that $6,250 was to be removed from the judgment debt of $10,341,410.32.

Next, whether the taxpayer, being of part Māori descent, is not a person who must compulsorily pay any form of tax. The Commissioner submitted that Parliament has the right to enact legislation imposing taxes. The Commissioner also noted that the appellant had not provided any evidence of his whakapapa establishing on the facts that he is of Māori descent. The Court rejected the taxpayer's arguments. There was no authority to support such a submission that statutes passed by Parliament are not applicable to persons of Māori descent. There is an obligation to pay tax irrespective of race.

The taxpayer also argued that the decisions of the Commissioner "transgress the provisions of sections 9 and 27" of the New Zealand Bill of Rights Act. The Court agreed with the Commissioner that these sections had no application in the circumstances of this case.

Next, the Court discussed the "fresh evidence" that the taxpayer sought to present at the hearing in an attempt to support a new point that the Commissioner abused his powers by making the taxpayer's assessments. The Court held that the taxpayer did not meet the requirements for adducing fresh evidence on appeal. Nor in any event was it held that the proposed "new evidence" would have made any difference.

Finally, the Court reviewed the point raised by the taxpayer that the District Court Judge accepted the assessments as made by the Commissioner. The Court noted that the taxpayer had not filed the relevant tax returns and had failed to commence proceedings challenging the default assessments. The Court agreed with the Commissioner that it is a fundamental statutory obligation for the taxpayer to file returns. The Commissioner had no choice but to make assessments by default. As the taxpayer failed to challenge, the assessments are now indisputable and are deemed to be correct. The taxpayer cannot now go behind the assessments.

Report a Problem with this Page or Publication

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2010

Issued

2010

Decision

19 Mar 2010

Appeal Status

Pending
[Skip to main content](#main-content-tt)

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2016

Issued

2016

Decision

07 Oct 2016

Court

NZTRA

Appeal Status

Not appealed

Default assessments for income tax and shortfall penalties for evasion, abusive tax position and gross carelessness upheld by Taxation Review Authority
=======================================================================================================================================================

2016 case note – default assessments upheld by Taxation Review Authority - suppressed income, tax avoidance, evasion penalties.

Case

TRA 26/14 & TRA 5/16 \[2016\] NZTRA 11

Legislative References

Income Tax Act 2007 ss BG 1, GA 1 and GB 27 Income Tax Act 2004 ss CA 1 and GC 14B Income Tax Act 1994 ss CH 3 and GC 14B & Tax Administration Act 1994 ss 141, 141C, 141D and 149A

### Summary

The Taxation Review Authority (“the Authority”) upheld the Commissioner of Inland Revenue’s (“the Commissioner”) default assessments issued on the basis that the disputant had suppressed income by failing to return amounts paid to him and on his behalf as a condition of his employment, arranging for management fees to be paid to trusts he controlled, and by arranging for his services to be remunerated by loan payments either made to himself or his family trusts. The Authority also upheld shortfall penalties imposed for evasion, abusive tax position and gross carelessness.

### Impact

The decision provides a useful statement of the standards required for the imposition of tax evasion shortfall penalties, abusive tax position penalties and gross carelessness shortfall penalties. It also reaffirms the principle in _Brent v Commissioner of Taxation_ (1971) 125 CLR 418, that all amounts received for services rendered will be income under ordinary concepts.

### Introduction

The disputant challenged default assessments and **s**eparate proceedings were issued in March 2016 for the shortfall penalties issued to him by the Commissioner for the 2001 – 2009 income tax years. The assessments were issued on the basis that the disputant had suppressed income:

1.  by failing to return amounts paid to him and on his behalf by his employer as a condition of his employment;
2.  by arranging for management fees for services he performed to be paid to trusts he controlled; and
3.  by arranging for his services to be remunerated by receipt of loan payments either made to himself or his family trusts.

In addition, the Commissioner imposed shortfall penalties, which the disputant also challenged. By consent, both challenges were heard together.

### Facts

The disputant is a businessman who was involved in the management and control of a number of companies during the relevant tax years. During this period he enjoyed a comfortable lifestyle and accumulated substantial assets. He achieved this using various payment arrangements and a number of different companies and trusts.

The investigation into the disputant’s tax affairs was complex and took a number of years. The Authority noted that the disputant took an obstructive position and had been convicted of aiding and abetting his wife in obstructing Inland Revenue officers executing a search warrant and he had also been convicted of failing to comply with a notice issued under s 17 of the Tax Administration Act 1994 (“the TAA”).

During the 2001 – 2003 tax years the disputant was employed by GPL. He received a minimal salary and paid a small amount of PAYE. GPL paid the disputant’s personal and living expenses, totalling $220,974.16. The Commissioner assessed these payments as employment income or alternatively as income under ordinary concepts or as part of a tax avoidance arrangement.

After this period the disputant worked for a group of entities controlled by a businessman referred to as Mr Smith. The group of entities, described as the Q/C Entities, involved a complex structure of companies and trusts which grew rapidly in the 2002 – 2007 period.

In the 2004 – 2008 tax years, the Q/S Entities paid various amounts of management fees to the disputant’s family trusts (the AF 2 Trust, AF Trust and Y Trust) for services provided by the disputant. The Commissioner assessed these fees as attributable to the disputant under the personal services attribution rule or in the alternative, as part of a tax avoidance arrangement. The Commissioner also assessed management fees of $40,000 and $180,000 charged by the AF 2 Trust solely as being part of a tax avoidance arrangement.

In 2006, the disputant received $600,000 which he says was a loan from QLL. The funds were paid from a facility that QLL had with X Finance Co. The Commissioner assessed this amount as income to the disputant under ordinary concepts.

Finally in the 2004 – 2009 tax years, the disputant and/or trusts associated with him (his family trusts and R Trust) received loans from the Q/S Entities. The Commissioner contended that these loans were received as part of a tax avoidance arrangement.

### Decision

_GPL payments_

The disputant initially maintained that the payments from GPL towards his personal and living expenses were a loan to him or the AF2 Trust. This was in direct contradiction to an affidavit the disputant had sworn during separate court proceedings in 2003. At the end of the hearing the disputant conceded that these payments were employment income but contended that the total amount should be reduced by the sum of $100,000 (which was a repayment by the disputant and the AF 2 Trust under a settlement agreement with GPL and other shareholders of GPL).

The Authority did not accept that the payments made by GPL were a loan or that the $100,000 settlement amount related to repayment of the alleged loan.

The Authority was satisfied that the disputant received the total amount of $220,974.16 over the 2001 – 2003 income years for personal services provided by him to GPL and that these payments were income to the disputant under s CH3 of the Income Tax Act 1994.

_Management fees_

The Commissioner alleged that various management fees derived by the disputant’s family trusts were attributable to the disputant under the personal services attribution rule (GB 27 of the Income Tax Act 2007 and GC 14B of the Income Tax Act 1994 and 2004). Following the completion of evidence the disputant conceded that these fees were attributable to him.

_X finance co payment_

The Commissioner contended that a payment of $600,000 made to the disputant in 2006 was consideration for services rendered by the disputant and is income under ordinary concepts. The Authority recognised the principle that “under ordinary concepts all amounts received from the provision of services whether as an employee or independent contractor is income” and cited _Brent v Commissioner of Taxation_ (1971) 125 CLR 418_._

The disputant entered into an agreement to purchase an apartment in 2005 and the balance of the purchase price ($600,000) was paid using funds drawn down on QLL’s loan facility with X Finance Co. The disputant submitted that the sum was a loan from QLL which had been secured by a caveat over the apartment. However, no caveat was registered on the title. In 2005 the disputant borrowed $500,000 from Z Bank, which was secured against the apartment. The disputant stated that this other loan was used to repay the advance from X Finance Co.

The Authority however found that there was no evidence of the $600,000 payment being a loan from QLL.

The disputant also submitted that it was a reasonable inference that the $500,000 loan from Z Bank was used for investment purposes in the Q Group, and was in effect a partial repayment of the $600,000 to QLL. The Authority found that there was no sufficient factual basis for such an inference as there were no records as to where the funds were paid.

The Authority found that the disputant was unable to discharge the onus that the Commissioner was wrong in her assessment that the $600,000 payment was income under ordinary concepts.

_Tax avoidance arrangements_

The Commissioner contended that there were two discrete tax avoidance arrangements:

1.  the “Management Fee Arrangement” (limited to the payments of $40,000 in 2003 and $180,000 in 2004 due to the disputant’s concession that the management fees were properly assessed under the personal services attribution rule); and
2.  the “Q/S Entities Loan Arrangement”, where instead of receiving income that was commercially realistic for the services rendered to the Q/S Entities, the disputant and/or his trusts received loans.

The Authority treated these arrangements individually, applying the two-stage analysis in _Ben Nevis Forestry Ventures Ltd v Commissioner of Inland Revenue_ \[2008\] NZSC 115, \[2009\] 2 NZLR 289 (“_Ben Nevis_”).

_First arrangement: management fees arrangement_

_Was there an arrangement?_

The Authority accepted the arrangement as defined by the Commissioner, describing the arrangement as: the AF 2 Trust contracted with DML and the QL Trust for the provision of management services which were provided by the disputant. AF 2 Trust charged management fees to these entities. The disputant and his family were beneficiaries of the AF 2 Trust. While the disputant resigned as a trustee in 2003, he remained in control of the AF 2 Trust (including its bank accounts) and made decisions for this trust. The disputant used the management fees paid to the AF 2 Trust for his benefit and that of his family. The tax effect of the arrangement was that the AF 2 Trust derived the management fees and became liable for the tax rather than the disputant. The AF 2 Trust did not return the income and nor did it pay the disputant for his services.

_Specific provisions? (Ben Nevis stage one inquiry)_

The Authority agreed with the Commissioner that the disputant avoided s CH 3 (employment income) and s CD 5 (income under ordinary concepts) of the Income Tax Act 1994 (and the comparable provisions in the 2004 Act - Sections CE 1 and CA1(2)) by ensuring that the funds that would be his income for services rendered were received by the AF 2 Trust. The Authority also agreed that Parliament would not have contemplated that either of those provisions could be bypassed through the use of an artificial and contrived agreement that lacked commercial merit.

_Parliamentary contemplation? (Ben Nevis stage two inquiry)_

The Authority acknowledged that the facts were similar to _Penny & Hooper_ \[2011\] NZSC 95, \[2012\] 1 NZLR 433_,_ and outlined the Supreme Court decision.

The Authority stated that Parliament would not have contemplated that the disputant could divert income earned from his personal exertions to his family trust without being paid a market salary where the disputant still continued to enjoy the benefit of those funds. The Authority did not consider that there could be any commercial explanation for the structure and in all the circumstances, it found the arrangement to be artificial and contrived.

The Authority was satisfied that taking all the factors into account, the purpose or effect of this arrangement was one of tax avoidance.

_Tax purpose or effect of the arrangement more than merely incidental_

On the basis that the arrangement was contrived and artificial and lacked any commercial reality, the Authority held that the tax avoidance purpose or effect of the arrangement was more than merely incidental to any other purpose or effect.

_Counteracting the tax advantage?_

The Authority was satisfied that the management fee arrangement was a tax avoidance arrangement, and agreed with the Commissioner’s reconstruction of the disputant’s income on the basis that the management fees paid to AF2 trust were the income of the disputant.

_Second arrangement: Q/S Entities loan arrangement_

_Was there an arrangement?_

The Authority accepted that during the 2004 - 2009 tax years there was a pattern of substantial loans made to the disputant or his trusts by the Q/S Entities, where there were no specific loan agreements, no requirements to pay interest and no provision for repayment. These loans were used to pay the living and other expenses of the disputant and his family. Over the same period the disputant received employment income on which he paid PAYE fixed at a rate which was not in any way commensurate with his various management positions.

The Authority accepted that there was an arrangement involving the steps as identified by the Commissioner.

_Specific Provisions? (Ben Nevis stage one inquiry)_

The Authority stated that Parliament would not have contemplated that ss CE 1 (employment income) and/or CA 1(2) (income under ordinary concepts) of the Income Tax Act 2007 (and the comparable provisions in the earlier Acts - ss CE 1 and CA 1(2) of the Income Tax Act 2004 and ss CH 3 and CD 5 of the Income Tax Act 1994)could be bypassed in the way that has occurred in this arrangement.

_Parliamentary Contemplation? (Ben Nevis stage two inquiry)_

The Authority noted that the Commissioner did not dispute that the amounts were loans, before outlining the analogous decision of _Krukziener v Commissioner of Inland Revenue_ (2011) 25 NZTC 20-055 (HC) (“_Krukziener_”)_._ In _Krukziener_, Courtney J held that a genuine loan does not necessarily mean that there cannot be a tax avoidance arrangement.

The Commissioner contended that the commercial and economic reality of the arrangement, notwithstanding the legal form, was that the amounts paid as loans were paid because of services provided to the Q/S Entities by the disputant. The Authority agreed with the Commissioner and stated that the disputant’s $36,000 income did not reflect the disputant’s roles and work responsibilities. The loans, totalling $7,302,275, were used as income subsidies to fund the disputant’s living and other expenses. The Authority stated that, though in theory, the loans had to be repaid, the disputant continued to have control of and access to the funds, there was no commercial rationale for the loans (the disputant and/or his trusts would not be able to repay the loans), interest was not charged (except in the 2007 year) or paid, and no provision or efforts were made for repayment.

The Authority agreed with the Commissioner that the disputant received the loans as income substitutes and the fact that they were used to purchase capital assets does not convert those payments into capital receipts.

The Authority was satisfied that viewed in a commercially and economically realistic way, the arrangement circumvents the relevant provisions in a way which Parliament would not have contemplated.

_Tax purpose_ _or effect of the arrangement more than merely incidental_

The Authority stated that the arrangement lacked any commercial reality, and the only purpose or effect of the arrangement was tax avoidance.

_Counteracting the tax advantage_

The Authority accepted the Commissioner’s reconstruction of the loans as the disputant’s income as being well within the Commissioner’s discretion and appropriate in the circumstances. The Authority did not accept the disputant’s attempt to raise the issue of apportionment, as the disputant had not established a factual foundation for the issue.

**_Shortfall penalties_**

The Commissioner assessed the disputant for shortfall penalties at different rates: evasion penalties in relation to the payments received from GPL; abusive tax position penalties in relation to the loans from Q/S Entities, the payment from X Finance Co and the management fees; and gross carelessness penalty for the DML payment.

_Tax evasion shortfall penalties – payments by GPL_

The Commissioner argued that the taxpayer was liable to pay an evasion shortfall penalty under s 141(1)(a) of the TAA. The Authority, adopting the Commissioner's analysis, concluded that the disputant was well aware that he was required to pay tax on the income earned by him as an employee of GPL, including on the expenses paid on his behalf by that company, and he deliberately failed to do so.

The Authority stated that evasion requires intentional behaviour or subjective recklessness. Subjective recklessness requires actual awareness of the risk of breaching the obligation. It observed that the disputant was an experienced businessman who has managed and owned a number of companies in different industries. It accepted that he was knowledgeable about tax matters (although it noted that it does not require sophisticated knowledge to be aware of the obligation to pay tax on employment income). The Authority found that the Commissioner had satisfied her onus of proof. The shortfall penalties for evasion were properly imposed.

_Abusive tax position penalties - Q/S loan, the X finance Co payment and management fees_

The Authority found that, regarding these payments, the disputant took a tax position which, viewed objectively, was not likely to be correct. The Authority was also satisfied that he took these tax positions with the dominant purpose of avoiding tax. The Authority concluded that the disputant took an abusive tax position and that the Commissioner was correct to impose penalties under s 141D of the TAA in respect of these payments.

_Gross carelessness shortfall penalty – the DML payment_

The Authority decided that a shortfall penalty for gross carelessness was properly imposed, finding that a reasonable person in the disputant’s position, with his experience, would have known that the amount was income and that the disputant showed a high level of disregard for the consequences of not returning the income.

Report a Problem with this Page or Publication

[Case summaries](/publications#f-ttTypeFacet=Case%20summaries&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / 2016

Issued

2016

Decision

07 Oct 2016

Court

NZTRA

Appeal Status

Not appealed
[Skip to main content](#main-content-tt)

[Research & development](/new-legislation/act-articles/research-development "Research & development")

Definition of R&D activities (section LH 7)
===========================================

The definitions of 'research' and 'development' in section DB 35 which allow tax deductibility to follow accounting treatment have been updated.

Only R&D activities as defined in section LH 7 are eligible for the tax credit.

The definitions of "research" and "development" in section DB 35, which apply to allow tax deductibility to follow accounting treatment, remain and have been updated. As the tax treatment is so closely linked to accounting, the accounting definitions have been retained for that purpose only and are not relevant for the credit.

The legislation defines research and development activities as:

*   systematic, investigative and experimental activities (SIE) that are performed for the purposes of acquiring new knowledge or creating new or improved materials, products, devices, processes or services and that:
    *   are intended to advance science or technology through the resolution of scientific or technological uncertainty; or
    *   involve an appreciable element of novelty.
*   other activities that are wholly or mainly for the purpose of, required for, and integral to, the carrying on of the activities in paragraph (a).

The definition is not limited to basic research and is expected to apply to a wide range of development activities in a variety of industries. However, routine business activities directed at improving efficiency that do not seek to advance science or technology, or that do not involve an appreciable element of novelty, are not eligible.

The definition draws on elements of the R&D definitions in the United Kingdom, Ireland, Canada and Australia. It is most similar to the Australian definition, which has advantages for businesses operating on both sides of the Tasman and also for Inland Revenue, which will be required to implement the credit within a short timeframe. In particular, it is expected that application of the "appreciable element of novelty" limb will draw on Australian experience.

Activities described in paragraph (a) are SIE activities and activities in paragraph (b) are support activities. This is relevant in relation to the excluded activities in Schedule 21, Part C.

The creation of new or improved production equipment and machinery is included in paragraph (a) as new or improved products.

R&D need not be successful to qualify for the credit.

There is legislative clarification of the meaning of some of the terms used in the definition. Further elaboration on the definition is included in guidelines.

**Systematic, investigative and experimental activities (subsection (2))**

Claimants must demonstrate that the R&D process followed a planned, logical progression of work involving hypothesis, experiment, observation and evaluation.

**Scientific or technological uncertainty (subsection (3))**

This exists when knowledge of whether something is scientifically or technologically possible, or how to achieve it in practice, is not publicly available or deducible by a competent professional working in the field. This definition, and the definition of "technology" are derived from the United Kingdom's R&D definition.

**Novelty (subsection (4))**

For activities to be "novel" there must be some development of the technology or a new use of existing technology. To establish whether something is new, it should be compared with what is already available in the public arena on a reasonably accessible world-wide basis at the time in that technology.

The "appreciable element of novelty" limb is drawn from the Australian R&D definition and the statutory clarification discussed in the paragraph above is based on the explanation of that term in the Australian _R&D Guide_ (Part B, page 16). The provisions should be very similar in scope. In particular, "appreciable" means meaningful or significant in the context of the activities undertaken.

**Technology (subsection (5))**

For the purposes of the R&D definition, "technology" is the practical application of scientific principles and knowledge.

**Simultaneous R&D**

Under the definition, R&D qualifies if it is done by two firms simultaneously and independently doing the same innovative work or when work has already been done, but this is not public knowledge because it is a trade secret, and another firm repeats the work.

**Improvements to existing products/processes**

Incremental development and improvements to existing products or processes can qualify as R&D. However, the improvement sought would have to involve an appreciable element of novelty or attempt to advance science or technology. It therefore should be more than routine upgrading.

**Support activities (paragraph (b) of R&D definition)**

Supporting activities that are wholly or mainly for the purpose of, required for, and integral to the carrying on of SIE activities referred to in paragraph (a), but which in themselves are not systematic, investigative and experimental, are eligible R&D. Support activities are eligible only if there is a SIE activity, though the support activities need not occur in the same income year as the SIE activity.

The requirement that activities be wholly or mainly for the purpose of SIE R&D is intended to exclude the following types of activity:

*   construction of an asset with an innovative component when the main purpose of construction is sale of the asset or use for commercial purposes; and
*   activities carried out simultaneously for routine business purposes and R&D if R&D is not the main purpose. For example, if a business collects data mainly for its routine business operations but also uses it as an input to R&D, it is not an eligible support activity.

##### Example 1

ACo is a boat building company that designs innovative components for its boats. It develops a new type of keel which advances boat building technology and is R&D. The keel is to be tested on a boat it is building for a customer. Construction of the boat is not a qualifying support activity as the boat is not built mainly for R&D. It is built mainly for sale to a customer. This means that none of the construction costs are eligible for the credit.

**Example 2**

BCo is a developer constructing an apartment complex on reclaimed land. It has commissioned an engineering firm to design a new type of base to provide maximum protection in the event of an earthquake. Construction of the building is not an eligible support activity as the main purpose of construction is use in BCo's business. None of the construction costs are eligible for the R&D credit.

"Required for" means that the supporting activity must be only to the degree necessary to support the project. For example, if a drilling company is developing an innovative piece of drilling equipment that can be adequately tested using computer simulation, drilling is not "required for" the SIE R&D activity. If drilling is required to test the equipment, only drilling that is the minimum necessary qualifies.

"Integral to" means that such activities must be part of an R&D project (rather than indirect supporting activities such as cleaning and administration, which are dealt with as expenditure on overheads).

Examples of support activities that could be eligible include scientific or technological planning activities, mathematical analysis or modelling used to analyse the results of the experiments and routine data collection.
![C:\Users\17gapa\AppData\Local\Temp\wz0524\IRD Business Transformation Logo\72dpi Jpeg\IRD Business Transformation Logo Small_72dpi.jpg](<Base64-Image-Removed>)Workstream and PMO Quality Control Checklist
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

This quality control checklist has been completed by the workstream on the specified deliverable (detailed below). The Responsible Owner has accepted the deliverable and approved the deliverable for issue to the Accountable Person for approval.

The PMO confirms the deliverable complies with the PMO information management requirements.

Name of the Deliverable and D#:
-------------------------------

**Responsible Owner:**

**Workstream:**

| **Quality Management Principle** | **Y/N** | **Requirement** | **Comments** |
| --- | --- | --- | --- |
| **Purpose** |     | The document provides clear details of the purpose of the document. It delivers against the scope agreed in the Deliverables Register and supports the objectives agreed for the Current Phase. |     |
| **Logic** |     | The assumptions underpinning the document are explicit and recommendations are logical and based on the evidence provided. |     |
| **Accuracy** |     | 1.  The data and information used to inform the document are explicit, sources are referenced, and data supports the conclusions reached.<br>2.  The title and deliverable number match the Deliverables Register.<br>3.  The document versioning number is consistent with version control protocols and appears in the document control section in the document e.g. V.0.1<br>4.  The filename for the document is consistent with the programme’s naming conventions. |     |
| **Options** |     | The document demonstrates that an adequate range of options have been considered before a recommendation has been made. |     |
| **Consultation** |     | 1.  The document provides details of the RACI process followed as per the Deliverable Register.<br>2.  The Responsible Owner has confirmed that adequate consultation with all RACI parties has taken place and the feedback has been incorporated where appropriate.<br>3.  All consults / Informed parties have been listed in the deliverable.<br>4.  The workstream lead has endorsed the deliverable before providing to PMO. |     |
| **Practicality** |     | 1.  The implementation, technical feasibility, timing and compatibility with other wider projects and policies have been considered. (As appropriate). |     |
| **Presentation** |     | 1.  The deliverable is in the correct BT template.<br>2.  The format of the document is consistent with BT standards, templates and IR standards as appropriate.<br>3.  The document classification is consistent with the Information Classification guidance.<br>4.  The document is clear, concise, well presented visually, spell checked and free from errors.<br>5.  The document has correct page. numbering.<br>6.  The document cover sheet contains the BT ID - UiD10825.<br>7.  The document contains all the appropriate attachments and appendices. |     |

**The following documents are attached for formal review and sign-off:**

|     |     |
| --- | --- |
|     | **** |
| Deliverable |     |
| Deliverable sign off memo (signed by the lead, Responsible and Accountable persons) |     |
| Deliverable product description (pre-approved) | **No longer applicable** |

**The following section is completed by the PMO:**

**\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\***

**PMO Feedback**

Feedback will be provided here (as applicable)

**PMO quality control checklist sign-off**

This Deliverable is now ready for formal review/approval.

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

PMO Team Member Date:
https://irnz.sharepoint.com/sites/BT/PMO/lead/IR's Guide to Transformation External Site - Developing the Narrative/Delivering the Transformation (Collateral)/Getting Going/PMO/IR BT Deliverables Process.docx Page | 1 BT Deliverables Process Guide \[IN CONFIDENCE RELEASE EXTERNAL\] Background BT tracks deliverables 1 in JIRA and stores the controlled documents in BT SharePoint. • Deliverable Documents in SharePoint. • Deliverables in JIRA. There are two main sections to this document • Pre-Release, Creating or Modifying a Deliverable Process • Deliverable Sign Off Process For more information about this process or any technical difficulties please contact PMO Workflow Deliverables PMOWorkflowDeliverables@ird.govt.nz 1 1. Pre-Release, Creating or Modifying a Deliverable Process A. Pre-Release Preparation Process Before the start of each BT Release, the required deliverables are identified. Workstreams are responsible for identifying these, developing the deliverables and on completion, for arranging formal sign off by the Responsible and Accountable persons. After approval, the BT PMO will facilitate a deliverable QA. Deliverables are recorded in a Release Specific Deliverables Register and on completion, stored in the Deliverables Library on BT SharePoint. Once the Deliverables Register is baselined, the deliverables are: • provided a unique Deliverable ID (e.g., BTDEL-1234), • a JIRA record is created for tracking purposes, and • managed under change control Being under change control means t hat no informal changes can be made to the: • Deliverable Name, Description, RACI, or Completion Dates, • Including descoping a deliverable. Formal approval is required to change a deliverable. The change management process must be followed, and a Programme Change Request (PCR) is required. 1 A deliverable is a programme artefact not a project artefact. For more information, please contact PMOWorkflowDeliverables@ird.govt.nz https://irnz.sharepoint.com/sites/BT/PMO/lead/IR's Guide to Transformation External Site - Developing the Narrative/Delivering the Transformation (Collateral)/Getting Going/PMO/IR BT Deliverables Process.docx Page | 2 BT Deliverables Process Guide \[IN CONFIDENCE RELEASE EXTERNAL\] Use JIRA and SharePoint to manage work on the deliverable. 1 Request a Change Request (PCR) in JIRA Lin k to PCR process Once the PCR is approved the PMO will update your BTDEL JIRA deliverable or create a new one. Is this prior to the commencement of the Release? A formal / controlled deliverable document is required or needs to be changed as part of the BT Programme. A Yes Contact the PMO and add the Deliverable to the Register for the Release. The PMO will then ensure BTDEL numbers are assigned and document sets in SharePoint are created B No Follow the process for creating / updating a Deliverable during the Release B.1 B.2 AP PRO VED JIRA can be used to manage the deliverable going out for consult or any other logging of the deliverable. You should also link deliverables to scope and dependencies. NEW Pre Release Process B. Process during a Release B.1 Request a PCR To request a NEW deliverable or AMEND an existing deliverable you must use the Programme Change Management process. Link to PCR process B.2 BT PMO Update JIRA and BT SharePoint Once the PCR is approved, BT PMO will: a) Update the existing JIRA BTDEL record, or b) Create a NEW deliverable JIRA item (this will provide the unique BTDEL ID.) c) Create a BT SharePoint Deliverable Doc Set for the deliverable documents to be stored. d) Update the Document link in JIRA to point to the SharePoint doc set. e) Update the master Deliverable Register The JIRA deliverable status will be set to NEW. The SharePoint Doc set will be set at 01 – DRAFT. https://irnz.sharepoint.com/sites/BT/PMO/lead/IR's Guide to Transformation External Site - Developing the Narrative/Delivering the Transformation (Collateral)/Getting Going/PMO/IR BT Deliverables Process.docx Page | 3 BT Deliverables Process Guide \[IN CONFIDENCE RELEASE EXTERNAL\] See 3.1 Add Documents to MS SharePoint from Template 2 2. Deliverable Sign Off Process This is the process when the deliverable is ready for the BT PMO to quality review and formally approve. 2 Once a deliverable is ready for Review and Sign off Ensure the Deliverable is uploaded to the BT SharePoint Doc Set for the Deliverable 2.1 2.2 Update the status of the BTDEL JIRA item to PMO Review The PMO then checks the Deliverable and updates SharePoint Doc set to 02 PMO REVIEW 2.3 2.4 The Workstream then manages/ facilitates review and sign off of Deliverable updating JIRA as progress is made The PMO use JIRA to communicate and update. Emails will be added in comments in JIRA On approval the BTDEL will set to Approved and the SharePoint Doc Set updated to 03- APPROVED APPROVED PMO REVIEW PENDING APPROVAL Before submitting for PMO Review the workstream must confirm that the RACI has been followed, endorsements must please be noted in the JIRA BTDEL ticket “comments” as per the deliverable RACI 2.1 Ensure all the documents are in BT SharePoint Ensure the following are uploaded: • Deliverable document/s – this will be the deliverable itself plus any supporting reports, data sheets, charts, etc) https://irnz.sharepoint.com/sites/BT/PMO/lead/IR's Guide to Transformation External Site - Developing the Narrative/Delivering the Transformation (Collateral)/Getting Going/PMO/IR BT Deliverables Process.docx Page | 4 BT Deliverables Process Guide \[IN CONFIDENCE RELEASE EXTERNAL\] 2.2 Update JIRA Status to PMO Review Before updating the status in JIRA ensure that you have: • Saved the deliverable in the SharePoint Doc ument Set, • Linked the deliverable file to the JIRA ticket (get/copy the link from SharePoint), then Change the status on the JIRA item to PMO Review 2.3 BT PMO Document Review JIRA Deliverables in PMO Review will auto assign and generate a notification to the PMO 1. The PMO will update the status of the MS SharePoint Doc Set to 02 - PMO Review. 2. The PMO will review / QA the deliverable documents in the SharePoint Doc set. (You may need to Review, Accept or Reject track changes as advised by PMO.) 2.4 Manage Deliverable Approval The PMO will change the JIRA status to PENDING APPROVAL.  T he Workstream will facilitate the approvals by the Responsible and Accountable person(s).  An email from the approver embedded in the deliverable document or sign-off memo is ideal.  Endorsement / Approval in the JIRA thread is acceptable. Once approved and approvals have been embedded in the deliverable/ JIRA. T he PMO will: 1. APPROVE in JIRA 2. Change the status of the SharePoint Doc set to 03 APPROVED 3. Save the deliverable as a major version in SharePoint 4. Update the Deliverable Register . https://irnz.sharepoint.com/sites/BT/PMO/lead/IR's Guide to Transformation External Site - Developing the Narrative/Delivering the Transformation (Collateral)/Getting Going/PMO/IR BT Deliverables Process.docx Page | 5 BT Deliverables Process Guide \[IN CONFIDENCE RELEASE EXTERNAL\] 3 3. Appendix 3.1 Add Documents to MS SharePoint from Template To upload documents, see Uploading a document into SharePoint For ease, we suggest you create the templates. This is easier than copying older templates. 1. Go: https://irnz.sharepoint.com/sites/BT/deliv • Find the Deliverable Doc set which has been created for you by the PMO • Open the Doc set • Choose + New • Choose the template you wish to use: • PowerPoint, or MS Word 2. The template will open 3. In the Properties on the right give the file a title and 4. Fill in the metadata 5. The Save 6. Name the file: Always start with the deliverable number: D####: Deliverable Name 7. Choose the location: BT SharePoint Home > Deliverables 8. Then click More save options 9. Choose the doc set 10. Then Save Alternatively, you can save the document to another location and when ready upload it to the doc set. • Please remember to do this from the doc set location and to fill in the metadata. https://irnz.sharepoint.com/sites/BT/PMO/lead/IR's Guide to Transformation External Site - Developing the Narrative/Delivering the Transformation (Collateral)/Getting Going/PMO/IR BT Deliverables Process.docx Page | 6 BT Deliverables Process Guide \[IN CONFIDENCE RELEASE EXTERNAL\] 3.2 Using JIRA to consult JIRA can be used to mention, log and track activity on the Deliverable. For general information see https://irnz.sharepoint.com/sites/BT/BTTools/SitePages/ JIRA.aspx. If you want to tag people for consult on a deliverable, please use the consult field. 3.3 Deliverable Dashboard in JIRA Within JIRA there is a Deliverable Dashboard. If you would like to see active deliverables, and their progress, see this link: https://jira.nsp.ird.govt.nz/secure/RapidBoard.jspa?rapidView=526. Many teams include deliverables in their own dashboards. Or, create their own document tracking dashboards that include deliverables and other documents. If you need help with JIRA dashboards, please contact your Project Coordinator or email BT PMO Tools BTPMOTools@ird.govt.nz 3.4 Viewing Deliverables in MS SharePoint To find deliverables in SharePoint go to the BT Deliverables Library. https://irnz.sharepoint.com/sites/BT/deliv. Sensitive deliverables can only be viewed by your team. Please contact BTPMOTools@ird.govt.nz for assistance with this. Deliverables can also be viewed by Workstream in other ways. https://irnz.sharepoint.com/sites/BT/deliv/For ms/Workstream.aspx See How to use views for more information.
[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Te tuku huringa Delivering our transformation
=============================================

The Inland Revenue transformation website is our way of sharing what we did, and what we learnt, while delivering one of the biggest transformation programmes of its kind. This was a once-in-a-generation change to tax and social policy, something which impacts the whole of New Zealand, from government, through businesses to the country’s people and families.

To capture the size of the task we start by sharing a timeline of activity beginning in 2013 at the inception phase and ending in June 2022 when we closed out the transformation programme.

Our delivery timeline
---------------------

Show all

2013 Inception

### Programme and policy

*   Late 2012, early 2013 Cabinet approved in principle the Business Transformation funding subject to an approved business case.
*   Deputy Commissioner Change role established and appointed. This role had responsibility for our change resources, the transformation programme and was also the Senior Responsible Officer.
*   Recruitment of an experienced transformation specialist team began.
*   The Business Transformation Method was established - the foundation for the programme deliverables and structure, including the programme planning process.
*   First programme structure established – focused round business case development and planning.
*   Established a commercial team – all commercial activity for Business Transformation was managed by the programme.

2014 Foundation

### Programme and policy

We established the foundations of the programme including the:

*   10 keys reporting framework
*   Programme Management Office
*   Initial governance approach including establishing the governance teams and terms of reference.

Other key actions were:

*   Tax policy conference held to gather ideas for ‘Tax Administration for the 21st century' and set the outline for the subsequent green paper.
*   Initial programme leadership team was finalised.
*   Accenture was selected as a programme delivery partner.
*   Initial view of scope and programme phasing established.
*   Change management framework developed – the foundation for all practices and processes.
*   Communications team established to deliver all business transformation communications.
*   High-level design work identifying what the transformation would deliver resulted in the creation of 6 blueprints.
*   Shortlist of three viable core tax solutions identified with site visits to establish capability. This included overseas travel with the then Minister of Revenue.
*   Management consultants, KPMG confirmed as external Independent and Technical Quality Assessment (IQA/TQA) provider.

### Organisation Design

*   Change Management function established to deliver organisation design.

### Technology

*   Foundation programmes initiated to provide technical infrastructure to keep the business running until the new platform was fully implemented.

2015 Mobilisation

### Programme and policy

*   Cabinet approves the business case and funding for the transformation.
*   Policy Green Paper issued (March 2015) outlining the main policy changes that are to be delivered as part of our transformation.
*   Transformation delivery methodology agreed.
*   Governance structures finalised for initial delivery.
*   Design blueprints finalised and shared within the organisation.
*   FAST appointed as core tax software partner.
*   Master services agreements and statements of work set up with critical partners Accenture and FAST with comprehensive deliverables and timelines.
*   A vendor management approach and process was put in place for all key vendors.

### Stage releases - core tax and social policy

*   First GST Application Programming Interface delivered working with MYOB and Xero, connecting with our heritage environment.

2016 Delivery

### Programme and policy

*   Transitioned the programme team structure to a delivery-oriented release structure for core tax and social policy work, introducing delivery teams, for example, testing, deployment and so on.
*   DC Change title and responsibilities changes to DC Transformation to reflect that Transformation needs a 100% focus. Senior Responsible Officer responsibility moves to Chief Executive Officer.
*   Kaikoura Earthquake hits 14 November, 4 months before stage 1 go-live – main Wellington building closed. Limit of 500 people able to ‘connect’ remotely across the whole of Inland Revenue made remote working extremely challenging.
*   The Taxation Bill 'Transformation: First Phase Simplification and Other Measures' was enacted – key activity to pave the way for our digital transformation.

### Stage releases - core tax and social policy

*   High-level release approach agreed - based around product sequencing for example, GST, then income tax, then Working for Families Tax Credits and so on. GST chosen for the first Release (Stage 1), due to its relative simplicity.
*   Detailed delivery work for Stage 1 commences.
*   Agreed that this initial stage would involve a full move of (almost) all customers from FIRST to the new system, but FIRST would remain the customer master until a later release.
*   Accenture contracted to provide co-existence solution using a blend of Accenture and Inland Revenue legacy programme resources.
*   Offshore development centre in Manila established by Accenture to assist with the delivery of co-existence.

### Intelligence led

*   First tranche of Intelligence-led programme kicked off with procurement process for the Enterprise Content Management system.
*   Team Asparona joint venture with Deloitte selected and Information Knowledge Management (IKM) project initiation began.

### Technology

*   SPARK Revera selected as the provider for our new data centre provider. Data centre network design delivered in advance of Stage 1 of our core tax solution.
*   Upgraded identity and middleware solutions delivered, both pre-requisites for core tax Stage 1.

2017 Delivery

### Stage releases - core tax and social policy

*   Transformation Stage 1 delivered 7 February 2017: GST and digital registration for new immigrants.
*   Lessons learnt at Stage 1 identified the need for greater understanding of our customer/stakeholders’ business models. This led to the established of an account management function and with tax agents being seconded to the programme.
*   Multi-year appropriation of funding requested and approved.
*   Moved from a stage to a release strategy to de-risk and break down the delivery of tax into 2 releases.

### Intelligence led

*   Programme manager appointed to focus solely on Intelligence-led which included information knowledge management, advanced analytics and business intelligence and reporting.
*   Advanced analytics proof of concept completed.
*   Enterprise content management system (Stax) technical implementation with Infrastructure and initial business group roll out completed.
*   Intel-led key workshops with the Intelligence business groups to identify use cases which would inform scope.

### Technology

*   Cloud first policy established for future services.

2018 Delivery and adaption

### Stage releases - core tax and social policy

*   Release 2 go-live: withholding taxes, fringe benefit tax, and gaming machine duty moved to new systems - START and processes; the accounting income method (AIM) for provisional tax and the automatic exchange of information with international tax treaty partners (AEOI) were implemented; payday filing was introduced on a voluntary basis.
*   Lessons learned continue to drive improved processes across all areas of the programme, leading to first joint business and programme forum and yet greater focus on external stakeholders.

### Intelligence led

*   SAS selected as Inland Revenue’s advanced analytics partner and the advanced analytics (data and intelligence) foundational platform implemented. This was the first major cloud platform installed as part of the transformation programme.
*   Data and Intelligence Platform initial integration with START established.
*   Syl (Enterprise Search) proof of concept completed and informed the strategic direction of the Intelligent Information project

### Organisation Design

*   Over 3,900 staff move into new roles as the first 3 groups in Inland Revenue’s new organisation design were established: Customer & Compliance Services – Individuals, Customer & Compliance Services – Business, and Information & Intelligence Services.

### Digital

*   A pilot version of Inland Revenue’s re-designed website was released for customer feedback, initially focused on child support content.

### Technology

*   Technology upgrade to Office 365 and Windows 10 with the rollout of new mobile devices across the organisation to support staff to work more flexibly, completed December 2018
*   Exited from DXC Technology data centre - our legacy desktop technology provider.

2019 Delivery and adaption

### Stage releases - core tax and social policy

*   Release 3 go-live: tax on income and Working for Families (the first social policy product) moved to new systems (START) and processes; a new year-end process for individuals was introduced; payday filing became mandatory; new requirements for investment income reporting were introduced on a voluntary basis.
*   START takes over from FIRST as the customer master
*   Refined our release-scoping process to ensure that what was agreed to be delivered was based on the highest value (benefit and complexity/cost trade-offs).
*   Expanded the Early Life Support process to encompass people, operations, technology, customers and stakeholders, with an additional focus on reputational risk. Team made up of a mix of business transformation and organisation resources and overseen by the Deputy Commissioner Corporate Integrity and Assurance (outside the transformation programme).

### Intelligence led

*   The new Data and Intelligence Platform was implemented, enabling the vast and varied data Inland Revenue collects to be quickly collated and made of sense of.
*   Data and Intelligence Platform handed over to the organisation.
*   Enterprise content management solution (Stax) deployment / business roll out completed.
*   Initiated the Stax migration to a cloud solution.
*   Concept of the Intelligent Information and Enterprise Search developed.
*   Intelligent Information funding approved and project team mobilised.
*   Finalised and initiated data migration plans from heritage platform Enterprise Data Warehouse to Business Transformation systems.

### Organisation Design

*   Organisational changes within Information Technology and Communications took effect in March and December, with new structural roles and operating model.
*   The Policy and Regulatory Stewardship group was established as part of the new organisation design.

### Digital

*   Inland Revenue’s redesigned website went live with new income tax, Working for Families, and child support content. Content for other products was updated and moved over to the new website in line with releases.

### Enterprise support services

*   The first phase of the new enterprise support services platform (Ātea) went live, moving budgeting and forecasting functions to new systems and processes.
*   Second release of Ātea - finance, procurement and some human resources functions move onto the new platform.

2020 Delivery, adaption and sustain

### Stage releases - core tax and social policy

*   COVID-19 lockdown on 29 March strikes 2 weeks before Release 4 cutover on 9 April and go-live 16 April. Intense conversations, primarily with KiwiSaver fund providers result in a ‘go’ call to proceed with cutover.
*   Release 4 go-live: KiwiSaver, student loans and PAYE processing moved to new systems (START) and processes; investment income reporting changes became mandatory.
*   Digitising manual payments, ringfencing rental losses and changes to Research and Development Tax Initiative, also delivered by the programme.
*   Go-live was achieved with the team operating almost entirely remotely, from 208 people planned to be on site, to a maximum of 8 at any one time. 
*   As a result of the focus required to deliver the COVID-19 response, decision made to split the final stage of the transformation, Stage 4 into 2 releases, though the first would be delivered ahead of plan.

### Intelligence led

*   Developed Guided Help functionality (a user-friendly decision tree) to replace the Inland Revenue Knowledge Base. Released initially to front-line staff and actively used in response to the COVID-19 small business cashflow loan scheme.
*   Stax (our Enterprise Content Management system) moved to an ‘as a service’ construct and moved to cloud platform.
*   Foundations of the new intranet (Haukāinga) and Enterprise search functionality developed and tested.
*   Migrated all heritage Intranet sites into Haukāinga.

### Organisation Design

*   The Tax Counsel Office was established as part of the new organisation design.

### Digital

*   First release of the new and improved tax technical website went live.

### Enterprise support services

*   Third release of Ātea - sustainability and affordability functions go-live.

### Technology

*   Full upgrade of SPARK infrastructure and upgraded external identity management solution.
*   Wi-Fi first policy progressed.

### Covid-19 response

*   Several financial support solutions delivered in support of the Government’s Covid-19 response. These were delivered extremely rapidly using the flexibility of our new technology, primarily START.

2021 Delivery, adaption and sustain

### Stage releases - core tax and social policy

*   Stage 4, Release 1 go-live in March 2021: Paid parental leave, unclaimed money, duties and NZ foreign trusts moved to new systems (START) and processes.
*   Fully remote cutover executed.
*   Stage 4, Release 2 go-live in October 2021: Child support moves to new systems (START) and processes; first upgrade of START including myIR, the online services our customers use, and the software Inland Revenue’s people use.
*   Used new testing techniques to manage highly complex child support assessments, the final product to move into START.

### Intelligence led

*   Haukāinga released to all Inland Revenue users.
*   Stax (our Enterprise Content Management system) connected to Enterprise Search.
*   Availability of Haukāinga (intranet replacement platform) on mobile devices.
*   Guided Help expanded for use on www.ird.govt.nz (external customers).
*   Migrated START Help content into Haukāinga, allowing access to all Inland Revenue users.

### Organisation Design

*   The final groups supporting Corporate & Enabling Services were established as part of our new organisation design, including Enterprise Services, Enterprise Design & Integrity, CCS Planning Design & Delivery and Marketing & Communications.

### Digital

*   Transitioned all software providers to new Application Programming Interface's by April 2021.
*   Heritage gateway E-File decommissioned following the final Stage 4 release.
*   Moved KiwiSaver providers off a heritage function they used to automatically send data to us, to new gateway services, December 2021 ahead of schedule.

### Technology

*   FIRST, Inland Revenue’s heritage core processing system, archive solution implemented.
*   FIRST is switched off in November 2021.
*   Existing SAP Payroll moved to cloud.
*   Decommissioning and replacement activity underway including lift and shift of contact centre to SPARK data centre.

2022 Business, integration and transition

### Stage releases - core tax and social policy

*   Exited the final stage of Early Life Support for core tax and social policy transformation on the planned date of 31 January 2022.

### Technology

*   Completion of Decommissioning and Archiving programme involving over 400 applications.
*   Finalising programme of technology optimisation to finalised.
*   Deployed a new identity management system.

### Programme and policy

*   Transition of Inland Revenue knowledge, tools and templates to the organisation complete, including the launch of an enduring intranet site.
*   Development of external website to share what we have learned on the transformation journey with other organisations.

#### Topics

*   [Where we started](/about-us/business-transformation/where-we-started "Where we started")
    
*   [What we learnt](/about-us/business-transformation/what-we-learnt "What we learnt")
    
*   [Outcomes](/about-us/business-transformation/outcomes "Outcomes")
[Skip to main content](#main-content-tt)

DEP71

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

24 Jun 2009

Tax Depreciation Rates General Determination Number 71
======================================================

Determination DEP 71 (2009) sets a depreciation rate for firewood processors and log splitters (manual and computerised).

This determination may be cited as "Determination DEP 71: Tax Depreciation Rates General Determination Number 71".

1.  **Application**

*   This determination applies to taxpayers who own items of depreciable property of the kind/s listed in the table below that have been acquired on or after 1 April 2008.
*   This determination applies for the 2008 and subsequent income years.

2.  **Determination**

*   Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the economic rates to apply to the kind/s of items of depreciable property listed in the table below by:  
      
    *   Adding into the "_Timber & Joinery Industries_" industry category the general asset class for Firewood Processors and Log Splitters, estimated useful life 10 years, and diminishing value and straight-line depreciation rate of 20% and 13.5% respectively as listed below:
    *     
        
        | General asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
        | --- | --- | --- | --- |
        | Firewood Processor  <br>(manually operated) | 10  | 20  | 13.5 |
        | Firewood Processor  <br>(computerised) | 10  | 20  | 13.5 |
        | Log Splitter  <br>(manually operated) | 10  | 20  | 13.5 |
        | Log Splitter  <br>(computerised) | 10  | 20  | 13.5 |
        

3.  **Interpretation**

*   In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on the 24th day of June 2009.

  

Rob Wells  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP71

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP71

Issued

24 Jun 2009
[Skip to main content](#main-content-tt)

DEP72

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

01 Feb 2010

Tax Depreciation Rates General Determination Number 72
======================================================

Determination DEP 72 (2010) sets a depreciation rate for test chambers in the 'Electrical and Electronic Engineering' and other industry categories.

This determination may be cited as "Determination DEP: Tax Depreciation Rates General Determination Number 72".

1.  **Application**

*   This determination applies to taxpayers who own items of depreciable property of the kind/s listed in the table below that have been acquired during the 2010 or subsequent income years.
*   This determination applies for the 2010 and subsequent income years.

2.  **Determination**

*   Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the general rate to apply to the kind of items of depreciable property listed in the table below by:  
      
    *   Adding into the category "_Electrical and Electronic Engineering_", and to the "_Engineering (including automotive)_" industry categories, and to the "_Scientific and laboratory equipment_" asset category, the general asset class, the estimated useful life and diminishing value and straight-line depreciation rate listed below:
    *     
        
        | General asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
        | --- | --- | --- | --- |
        | Test Chambers – acquired during the 2010 or subsequent income years. | 12.5 | 16  | 10.5 |
        

3.  **Interpretation**

*   In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on the 1st day of February 2010.

  

Rob Wells  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP72

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP72

Issued

01 Feb 2010
[Skip to main content](#main-content-tt)

DEP73

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

30 Mar 2010

Tax Depreciation Rates General Determination Number 73
======================================================

Determination DEP 73 (2010) sets a depreciation rate for furniture in the 'Hire Equipment (short-term hire of 1 month or less only)' category.

This determination may be cited as "Determination DEP 73: Tax Depreciation Rates General Determination Number 73".

1.  **Application**

*   This determination applies to taxpayers who own items of depreciable property of the kinds listed in the table below and applies to the 2009/2010 income year and subsequent income years.

2.  **Determination**

*   Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the economic rates to apply to the kinds of items of depreciable property listed in the table below:  
      
    *   Adding into the "Hire Equipment (short-term hire of 1 month or less only)" asset category, the asset class, estimated useful life, and diminishing value and straight-line depreciation rates listed below:
    *     
        
        | Asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
        | --- | --- | --- | --- |
        | Furniture (loose) with a general DV rate of 20%\* | 2   | 50  | 40  |
        
          
        \* Residual value has been estimated at 25%

3.  **Interpretation**

*   In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on the 30th day of March 2010.

  

**Susan Price**  
Director, Public Rulings

Report a Problem with this Page or Publication

DEP73

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP73

Issued

30 Mar 2010
[Skip to main content](#main-content-tt)

DEP79

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

21 Oct 2011

Remedial matters relating to the depreciation of buildings Depreciation Determination Number 79
===============================================================================================

Determination DEP 79 (2011) amends the depreciation rate applicable to all of the generic building assets that have an estimated useful life of 50 years, to 0%.

* * *

### Note to determination DEP 79

The Taxation (Budget Measures) Act 2010, enacted on 27 May 2010, introduced significant changes to the depreciation regime applying to buildings. With effect from the start of the 2012 income year the depreciation rate of buildings with an estimated useful life of 50 years or more was changed to 0%. The changes were intended to make New Zealand's tax rules more neutral by recognising that allowing depreciation on buildings with long lives, and the application of depreciation loading on certain assets, provides tax depreciation rates in excess of true economic depreciation rates.

As a result of this legislation, it is necessary to amend the depreciation rate applicable to all of the generic building assets that have an estimated useful life of 50 years, to 0%. These are _Buildings (default class)_, _Buildings with reinforced concrete framing_, _Buildings with steel or steel and timber framing_ and _Buildings with timber framing_.

On 30 April 2010 the Commissioner issued Interpretation Statement IS 10/02: _Meaning of "building" in the depreciation provisions_ ("IS 10/02"). IS 10/02 concluded that essentially a building is a structure that has walls and a roof, is of considerable size, is meant to last a considerable period of time and is generally fixed to the land on which it stands; a building is a structure that can function independently of any other but is not necessarily a physically separate structure.

The effect of IS 10/02 is that some assets that were not previously regarded as buildings will now come within the meaning of "buildings" and the depreciation rate applicable to them is to be amended to 0%.

### Carparking buildings and carparking pads

Carparking buildings were previously regarded as "structures" for depreciation purposes. Inland Revenue acknowledges that many buildings provide carparking facilities for owners/occupiers. For the purposes of this determination, carparking buildings are buildings that are built and used predominately for carparking where the carparking facilities are the main function of the building.

The same treatment cannot be given to carparking pads, which are more in the nature of hardstanding. The depreciation rate available on this type of asset therefore remains unchanged.

In view of this change in treatment the current reference to _Carparks (buildings and pads)_ has been removed from the _Building and structures_ asset category and replaced with two new asset classes, _Carparking buildings_ and _Carparking pads_.

### Buildings (portable) and site huts

A further conclusion of IS 10/02 was that some items within existing asset classes could be either buildings or structures. This is on the basis that, while some of the items may have the appearance of a building, be of a considerable size and are attached to the land, others items may either not look like a building (they will look more like a container or some other structure) and/or may be too small and/or portable to be considered a building. Generally, a structure is considered to be too small to be a building when it is able to be moved without mechanical assistance (such as a crane or hiab) and it is not attached to the land. Due to their varying appearance, size and portability, buildings (portable) and site huts could potentially fall within this category.

The treatment of those portable buildings that have the appearance of a building, are of sufficient size and are sufficiently attached to the land so that they fall within the definition of a "building" remains unchanged_._ Structures that are too small, are sufficiently easy to relocate and/or do not have the appearance of a building will be treated as _portable huts (not buildings)_.

By their very nature, site huts will be either _portable huts (not buildings)_ or _buildings (portable)_, depending on their appearance, size and portability. Because of this, the current reference to _Site huts_ in the _Contractors, builders and quarrying_ industry category has been removed and replaced with _Buildings (portable)_ and _Portable huts (not buildings)_.

Note that despite both _Buildings (portable)_ and _Portable huts (not buildings)_ having an estimated useful life of 12.5 years, different rates of depreciation apply. The reason for this is the varying formulae used to calculate economic rates contained in subpart EE of the Act.

### Grandparenting provisions

On 30 July 2009 the Minister of Revenue announced "grandparenting" provisions for certain items of depreciable property acquired on or before 30 July 2009. This treatment was confirmed by the Taxation (Budget Measures) Act 2010. As carparking buildings and site huts are covered by this grandparenting provision they have been added to this Determination. Despite these assets now coming within the meaning of "buildings" those assets that were acquired or a binding contract was entered into for their purchase or construction, on or before 30 July 2009, will continue to be treated as structures for depreciation purposes.

**Grandstands**

A further example of assets that may or may not be a building, are grandstands. For example, stand-alone tiered seating is a structure, while grandstands that incorporate other facilities, such as changing areas, toilets or storage areas, are likely to be buildings (that have seating attached to them). To take account of this difference, it is proposed to include a new asset category _Tiered seating (not part of a building)_ for those grandstands that are structures and to amend the depreciation rate of _Grandstands_ to 0%.

* * *

General Depreciation Determination DEP 79
-----------------------------------------

This determination may be cited as "Determination DEP79: Tax Depreciation Rates General Determination Number 79".

### 1\. Application

This determination applies to taxpayers who own items of depreciable property of the kinds listed in the table below.

This determination applies for the 2012 and subsequent income years.

### 2\. Determination

Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the economic rates to apply to the kinds of items of depreciable property listed in the table below by:

*   Deleting from the "Building and structures" asset category the general asset classes, estimated useful lives and diminishing value and straight-line depreciation rates listed below:  
      
    
    | Building and structures | Estimated  <br>useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
    | --- | --- | --- | --- |
    | Buildings (default class) | 50  | 3   | 2   |
    | Buildings with reinforced concrete framing | 50  | 3   | 2   |
    | Buildings with steel or steel and timber framing | 50  | 3   | 2   |
    | Buildings with timber framing | 50  | 3   | 2   |
    | Carparks (buildings and pads) | 50  | 4   | 3   |
    | Grandstands | 50  | 3   | 2   |
    

*   Deleting from the "Contractors, builders and quarrying" industry category the general asset class, estimated useful life and diminishing value and straight-line depreciation rate listed below:  
      
    
    | Contractors, builders and quarrying | Estimated  <br>useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
    | --- | --- | --- | --- |
    | Site huts | 12.5 | 16  | 10.5 |
    

*   Adding into the category "Building and structures" asset category the general asset classes, estimated useful lives, and diminishing value and straight-line depreciation rates listed below:  
      
    
    | Building and structures | Estimated  <br>useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
    | --- | --- | --- | --- |
    | Buildings (default class) | 50  | 0   | 0   |
    | Buildings with reinforced concrete framing | 50  | 0   | 0   |
    | Buildings with steel or steel and timber framing | 50  | 0   | 0   |
    | Buildings with timber framing | 50  | 0   | 0   |
    | Carparking buildings | 50  | 0   | 0   |
    | Carparking pads | 50  | 4   | 3   |
    | Carparking buildings acquired, or a binding contract entered into for the purchase or construction of the building on or before 30 July 2009 | 50  | 4   | 3   |
    | Grandstands | 50  | 0   | 0   |
    | Tiered seating (not part of a building) | 50  | 4   | 3   |
    | Portable huts (not buildings) | 12.5 | 16  | 10.5 |
    

*   Adding into the category "Contractors, builders and quarrying" industry category the general asset classes, estimated useful lives, and diminishing value and straight-line depreciation rates listed below:  
      
    
    | Contractors, builders and quarrying | Estimated  <br>useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
    | --- | --- | --- | --- |
    | Buildings (portable) | 12.5 | 13.5 | 8   |
    | Portable huts (not buildings) | 12.5 | 16  | 10.5 |
    | Site huts acquired, or a binding contract entered into for the purchase or construction of the building on or before 30 July 2009 | 12.5 | 16  | 10.5 |
    

### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed on the 21 October 2011

Rob Wells  
Manager  
LTS Technical Standards

Report a Problem with this Page or Publication

DEP79

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP79

Issued

21 Oct 2011
[Skip to main content](#main-content-tt)

DEP80

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

10 Nov 2011

Residential Rental Property Chattels
====================================

Determination DEP 80 (2011) provides a new list of assets for the 'Residential Rental Property Chattels' industry category.

See also [QB 20/01: Can owners of existing residential rental properties claim deductions for costs incurred to meet Healthy Homes standards?](/questions-we-ve-been-asked/2020/qb-20-01)
 issued 17 June 2020

* * *

**Note to Determination DEP 80**  
Following the issue of _[Interpretation Statement 10/01: Residential Rental Properties - depreciation of items of depreciable property](/interpretation-statements/is1001-residential-rental-properties-depreciation-of-items-of-depreciable-property)
_ ("IS 10/01") in _Tax Information Bulletin_ Vol 22 No 4 (May 2010) the Commissioner has issued a general depreciation determination to provide a new list for the "Residential Rental Property Chattels" industry category. The list is consistent with the Commissioner’s position set out in IS 10/01 and includes items of depreciable property that are commonly found in residential properties.

Note: Some of these items cost less than $500.00 and under section EE 38 of the Income Tax Act 2007 low cost items (not part of any other property) may be treated as an expense item rather than separate depreciable property. Other items not common to residential rental properties have been removed but taxpayers may use a depreciation rate for a similar item in another industry or asset category. For example, depreciation rates for Spa pools/saunas that are listed in the "Leisure" industry category may be used.

* * *

### General Depreciation Determination DEP80

#### 1. Application

This determination applies to taxpayers who own depreciable property of the kind listed in the table below.

This determination applies from 1 April 2011, to the 2012 and subsequent income years.

#### 2. Determination

Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the economic rates to apply to the kind of items of depreciable property listed in the table below by:

*   Deleting from the "Residential Rental Property Chattels" industry category all the asset classes, estimated useful lives and depreciation rates listed under that category.
*   Inserting into the "Residential Rental Property Chattels" industry category, the following asset classes, estimated useful lives, diminishing value depreciation rates and straight line equivalent depreciation rates listed below:  
      
    
    | Asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
    | --- | --- | --- | --- |
    | Chattels (default class) | 5   | 40  | 30  |
    | Air conditioners and heat pumps (through wall or window type) | 10  | 20  | 13.5 |
    | Air ventilation systems (in roof cavity) | 10  | 20  | 13.5 |
    | Alarms (burglar/smoke, wired or wireless) | 6.66 | 30  | 21  |
    | Appliances (small) | 4   | 50  | 40  |
    | Awnings | 10  | 20  | 13.5 |
    | Bedding | 3   | 67  | 67  |
    | Blinds | 8   | 25  | 17.5 |
    | Carpets | 8   | 25  | 17.5 |
    | Clotheslines | 8   | 25  | 17.5 |
    | Crockery | 3   | 67  | 67  |
    | Curtains | 8   | 25  | 17.5 |
    | Cutlery | 3   | 67  | 67  |
    | Dehumidifiers (portable) | 4   | 50  | 40  |
    | Dishwashers | 6.66 | 30  | 21  |
    | Drapes | 8   | 25  | 17.5 |
    | Dryers (clothes, domestic type) | 6.66 | 30  | 21  |
    | Freezers (domestic type) | 8   | 25  | 17.5 |
    | Furniture (loose) | 10  | 20  | 13.5 |
    | Glassware | 3   | 67  | 67  |
    | Heaters (electric) | 3   | 67  | 67  |
    | Heaters (gas, portable and not flued) | 5   | 40  | 30  |
    | Lawn mowers | 4   | 50  | 40  |
    | Light shades/fashion items affixed to a standard light fitting\* | 10  | 20  | 13.5 |
    | Linen | 3   | 67  | 67  |
    | Mailboxes | 15  | 13  | 8.5 |
    | Microwave ovens | 4   | 50  | 40  |
    | Ovens | 8   | 25  | 17.5 |
    | Refrigerators (domestic type) | 8   | 25  | 17.5 |
    | Satellite receiving dishes | 12.5 | 16  | 10.5 |
    | Stereos | 5   | 40  | 30  |
    | Stoves | 8   | 25  | 17.5 |
    | Televisions | 5   | 40  | 30  |
    | Utensils (including pots and pans) | 3   | 67  | 67  |
    | Vacuum cleaners (domestic type) | 3   | 67  | 67  |
    | Washing machines (domestic type) | 6.66 | 30  | 21  |
    | Waste disposal units (domestic type) | 8   | 25  | 17.5 |
    | Water heaters (heat pump type) | 10  | 20  | 13.5 |
    | Water heaters (over-sink type) | 10  | 20  | 13.5 |
    | Water heaters (other eg, electric or gas hot water cylinders) | 15.5 | 13  | 8.5 |
    | Water heaters (solar type) | 10  | 20  | 13.5 |
    

\* Light fittings are connected to the electrical wiring and part of a residential rental building and without the function of lighting would not be considered complete.

#### 3.  Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed on 10 November 2011.

Rob Wells  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP80

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP80

Issued

10 Nov 2011
[Skip to main content](#main-content-tt)

DEP81

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

01 Mar 2012

Fertiliser storage facilities and remedial matters relating to the depreciation of buildings and grandparented structures
=========================================================================================================================

Determination DEP 81 (2012) concerns fertiliser storage facilities and remedial matters relating to the depreciation of buildings and grandparented structures.

#### Note to Determination DEP 81

On 30 April 2010, the Commissioner issued Interpretation Statement 10/02 _Meaning of "building" in the depreciation provisions_ ("IS 10/02"). IS 10/02 concluded that a building is a structure that has walls and a roof, is of considerable size, is meant to last a considerable period of time and is generally fixed to the land on which it stands. A building is a structure that can function independently of any other but is not necessarily a physically separate structure.

The effect of IS 10/02 is that some assets that were not previously regarded as buildings will now come within the meaning of "buildings". As identified in IS 10/02, these assets are:

*   Barns, including barns (drying);
*   Carparks (buildings and pads);
*   Chemical works;
*   Fertiliser works;
*   Powder drying buildings; and
*   Site huts.

Consequently, it is necessary to set new economic rates for these assets using the method applicable to "buildings" under subpart EE of the Income Tax Act 2007 ("ITA").

Consistent with IS 10/02, the asset classes "Carparks (buildings and pads)" and "Site huts" were reviewed, resulting in new asset classes being created to separate those assets that are considered "buildings" and those that are not. New economic rates have been set for those asset classes. See Determination DEP 79: _Remedial matters relating to the depreciation of buildings_, dated 21 October 2011.

DEP 81 sets general economic rates for the following residual assets using the formula in section EE 28 of the ITA to calculate economic rates for buildings:

*   Barns;
*   Barns (drying);
*   Chemical works;
*   Fertiliser works; and
*   Powder drying buildings.

#### Grandparented structures

On 30 July 2009, when the draft Interpretation Statement was released for consultation, the Minister of Revenue announced "grandparenting" provisions for certain items of depreciable property that may be affected by a finalised Interpretation Statement.

The effect of the grandparenting provisions is that despite the above listed assets now coming within the meaning of "buildings" under IS 10/02, those assets that were acquired, or a binding contract that was entered into for their purchase or construction, on or before 30 July 2009, will continue to be treated as structures for depreciation purposes. This treatment was confirmed by The Taxation (Budget Measures) Act 2010.

This determination clarifies that the existing rates continue to apply to the grandparented structures. Different rates of depreciation apply to the above listed buildings because of the varying formulae used to calculate the economic rates for "buildings" and "structures" contained in subpart EE of the Act.

#### Fertiliser storage facilities

In addition to the above remedial matters, the Commissioner is setting general depreciation rates for fertiliser storage facilities that are generally associated with fertiliser works, by adding a new asset class in the "Building and structures" asset category. The Commissioner considers that the fertiliser storage facilities are buildings within the definition of "building" in IS 10/02 and they have an estimated useful life of 33.3 years.

Fertiliser storage facilities are buildings at the fertiliser works used for the bulk storage of raw materials for the manufacture of fertilisers and depots (may or may not be on site of fertiliser works) used for the bulk storage of finished or partially finished fertiliser products ready for distribution. Taxpayers who own a building that is a fertiliser storage facility can depreciate that building using the rate under this determination from the 2011/12 income year.

This determination does not apply to buildings that are temporarily used as a fertiliser storage facility.

Where a relatively minor administration office area is attached to, or forms part of a fertiliser storage facility building, the Commissioner accepts that they may be treated as one asset for depreciation purposes.

This determination sets the economic rates for the asset class "Fertiliser storage facilities for the bulk storage of raw materials and fertiliser products (may or may not be at the site of fertiliser works)" acquired before 19 May 2005 and those acquired on or after 19 May 2005. Note that different rates of depreciation apply because of the different formulae used to calculate economic rates for buildings acquired before 19 May 2005 and on or after that date.

* * *

### General Depreciation Determination DEP 81

#### 1\. Application

This determination applies to taxpayers who own depreciable property of the kind listed in the table below.

This determination applies from the 2011-12 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAF of the Tax Administration Act 1994 the proposed general determination will apply to the kind of items of depreciable property listed in the table below by:

*   Deleting from the "Buildings and structures" asset category the general asset classes, estimated useful lives and diminishing value and straight-line depreciation rates listed below:

| Buildings and structures | Estimated  <br>useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
| --- | --- | --- | --- |
| Barns | 20  | 10  | 7   |
| Chemical works | 33.3 | 6   | 4   |
| Fertiliser works | 33.3 | 6   | 4   |

*   Deleting from the "Dairy plant" industry category the general asset class, estimated useful life and diminishing value and straight-line depreciation rates listed below:

| Dairy plant | Estimated  <br>useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
| --- | --- | --- | --- |
| Powder dryer buildings | 15.5 | 13  | 8.5 |

*   Deleting from the "Cigarette Manufacturing" industry category the general asset class, estimated useful life and diminishing value and straight-line depreciation rates listed below:

| Cigarette Manufacturing | Estimated  <br>useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
| --- | --- | --- | --- |
| Barns (drying) | 20  | 10  | 7   |

*   Adding into the category "Buildings and structures" asset category the general asset classes, estimated useful lives, and diminishing value and straight-line depreciation rates listed below:

| Buildings and structures | Estimated  <br>useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
| --- | --- | --- | --- |
| Barns, acquired on or before 30 July 2009 | 20  | 10  | 7   |
| Barns, acquired after 30 July 2009 | 20  | 8.5 | 5   |
| Barns (drying), acquired on or before 30 July 2009 | 20  | 10  | 7   |
| Barns (drying), acquired after 30 July 2009 | 20  | 8.5 | 5   |
| Chemical works, acquired on or before 30 July 2009 | 33.3 | 6   | 4   |
| Chemical works, acquired after 30 July 2009 | 33.3 | 4.5 | 3   |
| Fertiliser works, acquired on or before 30 July 2009 | 33.3 | 6   | 4   |
| Fertiliser works, acquired after 30 July 2009 | 33.3 | 4.5 | 3   |
| Powder dryer buildings, acquired on or before 30 July 2009 | 15.5 | 13  | 8.5 |
| Powder dryer buildings, acquired after 30 July 2009 | 15.5 | 11  | 6.5 |
| Fertiliser storage facilities for the bulk storage of raw materials and fertiliser products (may or may not be at the site of fertiliser works) (acquired before 19 May 2005) | 33.3 | 6   | 4   |
| Fertiliser storage facilities for the bulk storage of raw materials and fertiliser products (may or may not be at the site of fertiliser works) (acquired on or after 19 May 2005) | 33.3 | 4.5 | 3   |

*   Adding into the category "Dairy plant" industry category the general asset classes, estimated useful lives, and diminishing value and straight-line depreciation rates listed below:

| Dairy plant | Estimated  <br>useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
| --- | --- | --- | --- |
| Powder dryer buildings, acquired on or before 30 July 2009 | 15.5 | 13  | 8.5 |
| Powder dryer buildings, acquired after 30 July 2009 | 15.5 | 11  | 6.5 |

*   Adding into the category "Cigarette manufacturing" industry category the general asset classes, estimated useful lives, and diminishing value and straight-line depreciation rates listed below:

| Cigarette manufacturing | Estimated  <br>useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
| --- | --- | --- | --- |
| Barns (drying), acquired on or before 30 July 2009 | 20  | 10  | 7   |
| Barns (drying), acquired after 30 July 2009 | 20  | 8.5 | 5   |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed on the 1st day of March 2012.

Rob Wells  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP81

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP81

Issued

01 Mar 2012
[Skip to main content](#main-content-tt)

DEP82

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

18 Oct 2012

General depreciation rate for meal feeder - automated
=====================================================

Determination DEP 82 (2012) sets a depreciation rate for automated meal feeders used by primary producers to deliver supplementary dry and liquid feed to stock.

#### Note to Determination DEP 82

The Commissioner has set a general depreciation rate for "meal feeders, automated" by adding a new asset class in the "Agriculture, Horticulture and Aquaculture" industry category.

The Commissioner considers that the new asset class has an estimated useful life of 20 years.

#### What is the asset?

Automated meal feeders are used by primary producers (farmers) to deliver supplementary dry and liquid feed to stock. For example, to cows while they are being milked. Automated meal feeder systems may also be used in other farming activities such as poultry or fish farming.

Although there may be variations to the overall design to meet the customised requirements of each user, an automated meal feeder system generally consists of:

*   Meal feed pan
*   Galvanised steel silo to hold the feed until dispensing
*   Polyethylene tank to hold the liquid feed until dispensing
*   Galvanised steel silo which gives the ability to mix the feed being dispensed
*   Associated PVC pipework
*   An internal auger to move the dry feed and alkathene pipe which delivers the liquid feed, from the respective storage facilities
*   Pump which moves the liquid feed to the stainless feed pan
*   Motor or vibratory feeder, and
*   Control system.

* * *

### General Depreciation Determination DEP 82

#### 1\. Application

This determination applies to taxpayers who own depreciable property of the kind listed in the table below.

This determination applies from the 2012 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAF of the Tax Administration Act 1994 the general determination will apply to the kind of items of depreciable property listed in the table below by:

*   Adding into the "Agriculture, horticulture and aquaculture" industry category a new asset class, estimated useful life, and general diminishing value and straight line depreciation rates as listed below:

| Agriculture, horticulture and aquaculture | Estimated  <br>useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
| --- | --- | --- | --- |
| Meal feeders, automated | 20  | 10  | 7   |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed on the 18th day of October 2012.

Rob Wells  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP82

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP82

Issued

18 Oct 2012
[Skip to main content](#main-content-tt)

DEP83

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

03 Apr 2013

Depreciation Rates for machinery used for grading, sorting and packing produce
==============================================================================

Determination DEP 83 (Apr 2013) sets a depreciation rate for machinery used for grading, sorting and packing food and agricultural products.

#### Notes to Determination DEP 83

The Commissioner has been asked to set a depreciation rate for machinery used for grading, sorting and packing food and agricultural products.

These machines grade and sort a range of produce by scanning the items for defects such as size, colour and quality. The produce then passes further along the production line where they are weighed and packed into containers.

There is a range of machines, some more mechanically operated and some computerised and software dependent. Some of the machines are used in a person's own produce operation and some of the machines are hired on a short term basis.

The proposed new economic depreciation rates are aimed at covering the range of machines described above. We have also rationalised the Commissioner's table of depreciation rates by deleting those asset classes that are no longer necessary as they would come within the new asset classes.

* * *

This determination may be cited as "Determination DEP83: Machinery used for grading, sorting and packing produce".

#### 1\. Application

This determination applies to taxpayers who own items of depreciable property of the kind/s listed in the tables below:

The proposed new economic rates apply for the 2012 and subsequent income years. The rates being deleted continue to apply up to the date this determination is published in _the Gazette_.

#### 2\. Determination

Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the economic rate/s to apply to the kind/s of items of depreciable property listed in the table below by:

Deleting from the category AGRICULTURE, HORTICULTURE AND AQUACULTURE industry category, the assets class, estimated useful life and diminishing value rate and straight-line depreciation rate listed below:

| Asset class | Estimateduseful life(years) | DV rate(%) | SL rate (%) |
| --- | --- | --- | --- |
| Grading machinery | 15.5 | 13  | 8.5 |
| Grader (capsicums) | 8   | 25  | 17.5 |
| Graders (tomatoes) | 8   | 25  | 17.5 |
| Sorting machinery | 15.5 | 13  | 8.5 |

Adding into the category AGRICULTURE, HORTICULTURE AND AQUACULTURE industry category, the new provisional asset class, estimated useful life, and diminishing value rate and straight-line depreciation rate listed below:

| Asset class | Estimated useful life | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Grading machinery (computerised) | 8   | 25  | 17.5 |
| Grading machinery (non-computerised) | 15.5 | 13  | 8.5 |
| Sorting machinery (computerised) | 8   | 25  | 17.5 |
| Sorting machinery (non-computerised) | 15.5 | 13  | 8.5 |
| Packing machinery (computerised) | 8   | 25  | 17.5 |
| Packing machinery (non-computerised) | 15.5 | 13  | 8.5 |

Deleting from the category FOOD PROCESSING industry category, the assets class, estimated useful life and diminishing value rate and straight-line depreciation rate listed below:

| Asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Grader (capsicums) | 8   | 25  | 17.5 |
| Graders | 15.5 | 13  | 8.5 |
| Graders (tomatoes) | 8   | 25  | 17.5 |
| Sorters | 15.5 | 13  | 8.5 |
| Packing machines  <br>(not elsewhere specified) | 15.5 | 13  | 8.5 |

Adding into the category FOOD PROCESSING industry category, the new provisional asset class, estimated useful life, and diminishing value rate and straight-line depreciation rate listed below:

| Asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Grading machinery (computerised) | 8   | 25  | 17.5 |
| Grading machinery (non-computerised) | 15.5 | 13  | 8.5 |
| Sorting machinery (computerised) | 8   | 25  | 17.5 |
| Sorting machinery (non-computerised) | 15.5 | 13  | 8.5 |
| Packing machinery (computerised) (not elsewhere specified) | 8   | 25  | 17.5 |
| Packing machinery (non-computerised) (not elsewhere specified) | 15.5 | 13  | 8.5 |

Adding into the category HIRE EQUIPMENT (SHORT-TERM HIRE OF 1 MONTH OR LESS ONLY) asset category, the new provisional asset class, estimated useful life, and diminishing value rate and straight-line depreciation rate listed below:

| Asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Agriculture, horticulture and aquaculture machines for hire with a general DV rate based on an estimated useful life of 8 years | 5   | 40  | 30  |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on the 3rd day of April 2013.

**Rob Wells**

LTS Manager, Technical Standards

  
 

Report a Problem with this Page or Publication

DEP83

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP83

Issued

03 Apr 2013
[Skip to main content](#main-content-tt)

DEP85

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

10 Jul 2013

Buildings with reinforced concrete framing (default class), Buildings with steel or steel and timber framing (default class), Buildings with timber framing (default class)
===========================================================================================================================================================================

Determination DEP 85 (Jul 2013) sets general economic depreciation rates for buildings with reinforced concrete, steel/steel and timber, and timber framing.

#### Note to Determination DEP 85

The Commissioner has set general economic depreciation rates for various categories of buildings by adding new default asset classes to the "Building and Structures" asset category. The Commissioner has also deleted the asset classes for these same categories of buildings that are not default classes.

* * *

This determination may be cited as "Determination DEP85: Buildings with reinforced concrete framing (default class), Buildings with steel or steel and timber framing (default class), Buildings with timber framing (default class)"

#### 1\. Application

This determination applies to taxpayers who own depreciable property of the kind listed in the table below.

This determination applies from the 2012-13 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAG of the Tax Administration Act 1994 this determination will apply to the kind of items of depreciable property listed in the table below by:

Deleting from the "Building and structures" asset category the general asset classes, estimated useful lives, and general diminishing value and straight line depreciation rates as listed below:

| Buildings and structures | Estimated useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
| --- | --- | --- | --- |
| Buildings with reinforced concrete framing (before 2011-12 income year) | 50  | 3   | 2   |
| Buildings with reinforced concrete framing (from 2011-12 income year) | 50  | 0   | 0   |
| Buildings with steel or steel and timber framing (before 2011-12 income year) | 50  | 3   | 2   |
| Buildings with steel or steel and timber framing (from 2011-12 income year) | 50  | 0   | 0   |
| Buildings with timber framing (before 2011-12 income year) | 50  | 3   | 2   |
| Buildings with timber framing (from 2011-12 income year) | 50  | 0   | 0   |

Adding to the "Building and Structures" asset category the general asset classes, estimated useful lives, and general diminishing value and straight line depreciation rates as listed below:

| Buildings and structures | Estimated useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
| --- | --- | --- | --- |
| Buildings with reinforced concrete framing (default class) (before 2011-12 income year) | 50  | 3   | 2   |
| Buildings with reinforced concrete framing (default class) (from 2011-12 income year) | 50  | 0   | 0   |
| Buildings with steel or steel and timber framing (default class) (before 2011-12 income year) | 50  | 3   | 2   |
| Buildings with steel or steel and timber framing (default class) (from 2011-12 income year) | 50  | 0   | 0   |
| Buildings with timber framing (default class) (before 2011-12 income year) | 50  | 3   | 2   |
| Buildings with timber framing (default class) (from 2011-12 income year) | 50  | 0   | 0   |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on the 10th day of July 2013.

**Rob Wells**  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP85

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP85

Issued

10 Jul 2013
[Skip to main content](#main-content-tt)

DEP89

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

18 Aug 2014

Bench-top Pizza Ovens and Microwave Ovens (Commercial)
======================================================

Determination DEP89 (Aug 2014) sets a general depreciation rates for bench-top pizza ovens and microwave ovens.

#### Note to Determination DEP 89

The Commissioner has set general depreciation rates for bench-top pizza ovens and microwave ovens (commercial) by adding new asset classes to the "Hotels, motels, restaurants, cafes, taverns and takeaway bars" and "Shops" industry categories.

As loaned or hired assets tend to be handled and transported frequently and are not as well maintained as owned assets, a further asset class is provided for "pizza ovens (bench-top, for long-term loan or hire)", with a lesser estimated useful life. Note: Long-term loan or hire applies to a period greater than one month.

Commercial microwave ovens are very common in commercial kitchens and also in shops. These ovens are usually of a similar size to domestic microwave ovens but are constructed of better quality materials, and are not as large or long lasting as industrial microwave ovens used in food processing factories. A new asset class of "microwave ovens (commercial)" has been provided.

* * *

#### 1\. Application

This determination applies to taxpayers who own depreciable property of the kind listed in the table below.

This determination applies from the 2014 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAG of the Tax Administration Act 1994 the general determination will apply to the kind of items of depreciable property listed in the table below by:

*   adding into the "Hotels, motels, restaurants, cafes, taverns and takeaway bars" and "Shops" industry categories, new asset classes, estimated useful lives, and diminishing value and straight line depreciation rates as listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Pizza ovens (bench-top) | 6.66 | 30  | 21  |
| Pizza ovens (bench-top, for long-term loan or hire) | 5   | 40  | 30  |
| Microwave ovens (commercial) | 8   | 25  | 17.5 |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed on the 18th day of August 2014.

Rob Wells  
LTS Manager, Technical Standards  
 

Report a Problem with this Page or Publication

DEP89

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP89

Issued

18 Aug 2014
[Skip to main content](#main-content-tt)

DEP100

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

15 Jun 2017

Depreciation rate for rapid DC car charging stations
====================================================

Determination DEP100 (2017) sets a general depreciation rate for a new asset class 'Rapid DC car charging stations' in the Transportation category.

#### Note to Determination DEP100

The Commissioner has set a general depreciation rate for a new asset class "Rapid DC car charging stations", not currently provided for under the "Transportation" asset category, within the Commissioner's Table of Depreciation Rates.

Electric vehicles have a charger built in that converts the domestic alternating current (AC) into direct current (DC) for the car's battery. This onboard charger generally takes around 6-8 hours to fully charge a car. A rapid charger is a much larger, freestanding version than the onboard charger. It bypasses the vehicle's onboard charging device and supplies power directly to the vehicle's battery. It converts high power 3-phase AC into DC and significantly reduces the charging time - usually to less than 30 minutes.

* * *

### Determination DEP100: Tax Depreciation Rates General Determination Number 100

#### 1\. Application

This determination applies to taxpayers who own items of depreciable property of the kind listed in the table below:

This determination applies to the 2017 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAF of the Tax Administration Act 1994, the general determination will apply to the kind of items of depreciable property listed in the table below by:

*   Adding into the "Transportation" asset category, the new asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Rapid DC car charging stations | 10  | 20  | 13.5 |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed on the 15th day of June 2017.

Rob Wells  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP100

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP100

Issued

15 Jun 2017
[Skip to main content](#main-content-tt)

DEP101

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

06 Sep 2017

Tax Depreciation Rate for abrasive blasting booths (including media recovery/recycling, dust extraction and ventilation systems)
================================================================================================================================

Determination DEP101 (2017) sets a depreciation rate for abrasive blasting booths (including media recovery/recycling, dust extraction and ventilation systems).

#### Note to Determination DEP101

The Commissioner has recently been asked to consider what depreciation rate should apply for abrasive blasting booths.

The asset consists of the abrasive blasting chamber, including the in-floor media recovery system and the media reclaimer/recycler. It does not include the blast pot, the air compressor systems and any separate dust extraction system. This is because these are considered stand­alone assets for which depreciation rates already exist.

* * *

### Determination DEP101: Tax Depreciation Rates General Determination Number DEP101

This determination may be cited as "Determination DEP 101 Tax Depreciation Rates General Determination Number 101: Blasting booths (including media recovery/recycling, dust extraction and ventilation systems).

#### 1\. Application

This determination applies to taxpayers who own items of depreciable property of the kind listed in the tables below:

This determination applies for the 2016/17 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAF of the Tax Administration Act 1994, the general determination will apply to the kind of items of depreciable property listed in the table below by:

*   Adding into the "Cleaning, Refuse and Recycling" and "Engineering (including Automotive)" industry categories, the new asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Abrasive blasting booths (including media recovery/recycling, dust extraction and ventilation systems). | 12.5 | 16  | 10.5 |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on the 6th day of September 2017.

Rob Wells  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP101

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP101

Issued

06 Sep 2017
[Skip to main content](#main-content-tt)

DEP102

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

27 Sep 2017

Depreciation Rate for potato cool stores (climate controlled) structure only, excluding climate control plant
=============================================================================================================

Depreciation determination DEP102 (2017) adds an asset class for 'potato cool stores (climate controlled) structure only, excluding climate control plant'.

#### Note to Determination DEP102

The Commissioner has recently been asked to consider what depreciation rate should apply for potato cool stores.

Potato cool stores are specialist buildings that control humidity and temperature so that potatoes can be stored for long periods without spoilage occurring. These cool stores are fitted with refrigeration reticulation machinery, air transfer systems and associated electronic componentry (climate control plant).

In appearance, potato cool stores are dome-shaped tunnels. They are usually constructed of zinc coated galvanised steel (corrugated iron). The Commissioner accepts that these specialised buildings are exposed to a humid, corrosive environment that impacts the life of the building’s construction material.

For this reason the Commissioner is satisfied that the estimated useful life (EUL) of these specialised buildings is 33.3 years and has set a provisional depreciation rate for these assets accordingly.

It should be noted that it is the Commissioner’s view that the climate control plant is not attached to the potato cool store building; it can be easily removed without damaging either the plant or the building. This being so, the various items of climate control plant are separate items of depreciable property and (where appropriate) may be able to be separately depreciated. Further information, regarding whether items of depreciable property form part of a building, may be found in Interpretation Statement _IS 10/01 Residential Rental Properties – Depreciation of Items of Depreciable Property \[[1](#01)\
\]_.

* * *

### General Determination DEP102: Tax Depreciation Rates General Determination Number DEP102

This determination may be cited as "Determination DEP 102 Tax Depreciation Rates General Determination Number DEP102: Potato cool stores (climate controlled) structure only, excluding climate control plant".

#### 1\. Application

This determination applies to taxpayers who own items of depreciable property of the kind listed in the tables below:

This determination applies for the 2017/18 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the rate to apply to the kind of items of depreciable property listed in the table below by:

*   Adding into the "Buildings and Structures" asset category, the new asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Potato cool stores (climate controlled) structure only, excluding climate control plant | 33.3 | 4.5 | 3   |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on the 27th day of September 2017.

Rob Wells  
LTS Manager, Technical Standards

1Further information on this statement may be found at www.govt.nz (search term "10/01").

Report a Problem with this Page or Publication

DEP102

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP102

Issued

27 Sep 2017
[Skip to main content](#main-content-tt)

DEP103

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

14 Jun 2018

Depreciation Rate for skin therapy machines used for beauty treatments
======================================================================

This determination inserts a new asset class for skin therapy machines into the "Medical and Medical Laboratory" and "Shops" industry categories, that applies for the 2017-18 and subsequent income years.

#### Note to Determination DEP103

The Commissioner has recently been asked to consider what depreciation rate should apply for skin therapy machines used for beauty treatments. The beauty treatments include hair removal, reducing winkles, freckles, vascular lesions and pigmentation problems.

The asset uses intense light pulse (“IPL”) treatment supplemented by a Radio Frequency (“RF”) emitting mode, which radiates the follicles or skin cells with a shortwave or microwave radio frequency. In the RF mode, it is effectively operating as a diathermy machine (Diathermy is deep treatment of tissue by heat applied through RF or microwaves). The machine may include a handpiece which emits the light and/or RF that is waved over the skin and has a sapphire plate that touches the skin which is refrigerated by means of a circulating coolant to prevent overheating and burning.

* * *

### Determination DEP103: Tax Depreciation Rates General Determination Number 103

This determination may be cited as “Determination DEP103 Tax Depreciation Rates General Determination Number DEP103: Skin therapy machines used for beauty treatments”.

#### 1\. Application

This determination applies to taxpayers who own items of depreciable property of the kind listed in the table below:

This determination applies for the 2017/18 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAF of the Tax Administration Act 1994, the general determination will apply to the kind of items of depreciable property listed in the table below by:

*   Adding into the "Medical and Medical Laboratory" and "Shops" industry categories, the new asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| IPL, Laser, Ultrasound or RF emitting skin treatment or depilation equipment. | 8   | 25  | 17.5 |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by Vanessa Montgomery on the 14th day of June 2018.

Vanessa Montgomery  
Manager, Technical Standards, OCTC

Report a Problem with this Page or Publication

DEP103

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP103

Issued

14 Jun 2018
[Skip to main content](#main-content-tt)

DEP104

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

16 Aug 2019

Tax Depreciation Rate for lay-flat hoses
========================================

This determination sets a depreciation rate for lay flat hoses used for hire equipment business purposes.

* * *

**Note to draft Determination:**

The Commissioner has been asked to consider a depreciation rate for lay-flat hoses used for hire equipment business purposes.

Lay-flat hoses are generally viewed by the Commissioner as a component of a pump set and not a separate depreciable item. However, in the context of a hire equipment business, due to the variety of lengths that may be required, lay-flat hoses are often hired out as a piece of equipment separate to other equipment, so in these circumstances are viewed as separate depreciable property. The general determination will be available only to hire equipment businesses.

* * *

### Determination DEP104: Tax Depreciation Rates General Determination Number DEP104

1.  **Application**  
    This determination applies to taxpayers who own items of depreciable property of the kind listed in the tables below.  
    This determination applies for the 2018/19 and subsequent income years.
2.  **Determination**  
    Pursuant to section 91AAF of the Tax Administration Act 1994, the general determination will apply to the kind of items of depreciable property listed in the table below by:
    *   Adding into the "Hire Equipment" asset categories, the new asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below:  
         
        
        | Asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
        | --- | --- | --- | --- |
        | Lay-flat hoses | 3   | 67  | 67  |
        
3.  **Interpretation**  
    In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on the 16th day of August 2019.

**Rob Wells**  
Manager, Technical Standards, OCTC

Report a Problem with this Page or Publication

DEP104

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP104

Issued

16 Aug 2019
[Skip to main content](#main-content-tt)

DEP105

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

16 Oct 2019

Tax Depreciation Rate for pushrod/cable propelled pipeline camera inspection systems (not including pipeline crawlers)
======================================================================================================================

This determination sets a depreciation rate for pushrod/cable propelled pipeline camera inspection systems used to inspect pipework, for example domestic household sewer pipes or water pipes.

**Note to Determination DEP105:**

The Commissioner has been asked to consider what depreciation rate should apply for pushrod/cable propelled pipeline camera inspection systems used to inspect pipework, for example domestic household sewer pipes or water pipes.

The asset is basically a compact waterproof camera with an illumination source, capable of operation inside pipes, with rechargeable batteries or a mains supply cable. Push rods are provided with a self-levelling camera head and an iPad or similar device used as a monitor/control station. There is also a separate handheld locator device which picks up a beacon signal emitted from the camera, so that underground location and the layout of the pipe can be identified.

There appears to be a large range of pipeline camera inspection systems. This determination covers the simple pushrod/cable propelled pipeline camera inspection systems. The remote operated tractor/crawler vehicle type systems are treated as a separate asset class (“pipeline crawler”) in the “Dairy plant”, “Fishing”, “Oil and gas industry” industry categories and “Compressed air plant (where not industry specified)”, “Factory and other sundries”, “Reticulation systems, including power generation (excluding electrical, communications and gas reticulation)”, ‘Water and effluent treatment (where not industry specified)” asset categories.

* * *

### Determination DEP105: Tax Depreciation Rates General Determination Number 105

This determination may be cited as “Determination DEP105 Tax Depreciation Rates General Determination Number DEP105: Pushrod/cable propelled pipeline camera inspection systems (not including pipeline crawlers)”.

#### 1\. Application

This determination applies to taxpayers who own items of depreciable property of the kind listed in the tables below:

This determination applies for the 2018/19 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAF of the Tax Administration Act 1994, the general determination will apply to the kind of items of depreciable property listed in the table below by:

*   Adding into the “Dairy Plant”, “Fishing", Medical and Medical Laboratory", “Oil and Gas” industry categories, and the “Compressed Air Plant (where not industry specified)”, “Factory and Other Sundries”, “Reticulation Systems including Power Generation (excluding electrical, communications and gas reticulation)” and “Water and Effluent Treatment (where not industry specified)” asset categories, the new asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below:

| Asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Pushrod/cable propelled pipeline camera inspection systems (not including pipeline crawlers) | 4   | 50  | 40  |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on 16th day of October 2019.

Rob Falk  
National Advisor, Technical Standards

Report a Problem with this Page or Publication

DEP105

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP105

Issued

16 Oct 2019
[Skip to main content](#main-content-tt)

DEP54

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

27 Apr 2006

General Depreciation Determination DEP54
========================================

Determination DEP54 (Apr 2006) inserts diminishing value and straight-line depreciation rates into the depreciation tables for certain property.

This determination may be cited as "Determination DEP54: Tax Depreciation Rates General Determination Number 54".

1.  **Application**  
    This determination applies to taxpayers who own depreciable property of the kind referred to in paragraph 2 below and applies for income years corresponding to the 2005–06 and subsequent tax years.
2.  **Determination**  
    Pursuant to section 91AAF of the Tax Administration Act 1994, I hereby amend Determination DEP1: Tax Depreciation Rates General Determination Number 1 (as previously amended), hereinafter referred to as "DEP1", by inserting the diminishing value and straight-line economic depreciation rates as follows:
    *   In respect of the kinds of items of depreciable property for which the economic rate of depreciation is set under section EE 25B of the Income Tax Act 2004, and being a kind of item of depreciable property that is a general asset class as specified in DEP1 having an estimated useful life, applicable diminishing value banded depreciation rate and straight-line equivalent banded depreciation rate listed in columns 1, 2 and 3 respectively below, by inserting the respective diminishing value and straight-line depreciation rates listed in columns 4 and 5 below:

| 1   | 2   | 3   | 4   | 5   |
| --- | --- | --- | --- | --- |
| Estimated useful life (years) | DV banded dep'n rate (%) | SL equiv banded dep'n rate (%) | DEP54 DV banded dep'n rate (%) | DEP54 SL equiv banded dep'n rate (%) |
| 100 | 2   | 1.5 | 2   | 1.5 |
| 50  | 4   | 3   | 4   | 3   |
| 33.3 | 6   | 4   | 6   | 4   |
| 25  | 7.5 | 5.5 | 8   | 6   |
| 20  | 9.5 | 6.5 | 10  | 7   |
| 15.5 | 12  | 8   | 13  | 8.5 |
| 12.5 | 15  | 10  | 16  | 10.5 |
| 10  | 18  | 12.5 | 20  | 13.5 |
| 8   | 22  | 15.5 | 25  | 17.5 |
| 6.66 | 26  | 18  | 30  | 21  |
| 5   | 33  | 24  | 40  | 30  |
| 4   | 40  | 30  | 50  | 40  |
| 3   | 50  | 40  | 67  | 67  |
| 2   | 63.5 | 63.5 | 100 | 100 |
| 1   | 100 | 100 | 100 | 100 |

*   In respect of the kinds of items of depreciable property for which the economic rate of depreciation is set under section EE 25C of the Income Tax Act 2004, and being a kind of item of depreciable property that is a general asset class as specified in DEP1 having an estimated useful life, applicable diminishing value banded depreciation rate and straight-line equivalent banded depreciation rate listed in columns 1, 2 and 3 respectively below, by inserting the respective diminishing value and straight-line depreciation rates listed in columns 4 and 5 below

| 1   | 2   | 3   | 4   | 5   |
| --- | --- | --- | --- | --- |
| Estimated useful life (years) | DV banded dep'n rate (%) | SL equiv banded dep'n rate (%) | DEP54 DV banded dep'n rate (%) | DEP54 SL equiv banded dep'n rate (%) |
| 100 | 2   | 1.5 | 1.3 | 1   |
| 50  | 4   | 3   | 3   | 2   |
| 33.3 | 6   | 4   | 4.5 | 3   |
| 25  | 7.5 | 5.5 | 6.5 | 4   |
| 20  | 9.5 | 6.5 | 8.5 | 5   |
| 15.5 | 12  | 8   | 11  | 6.5 |
| 12.5 | 15  | 10  | 13.5 | 8   |

3.  **Interpretation**  
    In this determination, unless the context otherwise requires, expressions have the same meaning as in the Income Tax Act 2004.

This determination is signed by me on the 27th day of April 2006.

**Susan Price**  
Senior Tax Counsel

Report a Problem with this Page or Publication

DEP54

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP54

Issued

27 Apr 2006
[Skip to main content](#main-content-tt)

DEP55

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

27 Sep 2006

General depreciation determinations DEP55 to DEP59
==================================================

General depreciation determinations for psychological testing sets, metal speed humps, wintering pads, kiwifruit software and baby crayfish traps.

In _Tax Information Bulletin Volume 18_, No 7 (August 2006) on page 4 we advised of the availability of draft general depreciation determinations proposing the setting of general depreciation rates for the following items:

DDG0110: "Psychological testing sets" used in the medical industry  
DDG0111: "Metal speed humps"  
DDG0113: "Wintering pads (rubber)" used in the agriculture industry  
DDG0114: "Kiwiplus – Kiwifruit Software Package – designed for a specific year"  
DDG0115: "Peurulus (baby crayfish) traps" used in the fishing industry

We received no substantive submissions on these drafts.

We have now made the general depreciation determinations and they are reproduced below. The determinations include the rates applying to assets:

*   purchased before 1 April 2005, and
*   purchased on or after 1 April 2005.

The differing rates result from the enactment of the Taxation (Depreciation, Payment Dates Alignment, FBT, and Miscellaneous Provisions) Act 2006.

### Determination DEP55:

#### Tax Depreciation Rates General Determination Number 55

1.  **Application**  
    Pursuant to section 91AAG(6) of the Tax Administration Act 1994 this determination replaces Determination PROV2: Tax Depreciation Rates Provisional Determination Number 2 issued on 27 January 1995.  
      
    This determination applies to taxpayers who own assets in the class listed below.  
      
    This determination applies to "depreciable property" other than "excluded depreciable property" for the 2005/2006 and subsequent income years.
2.  **Determination**  
    Pursuant to section 91AAF of the Tax Administration Act 1994 I hereby amend Determination DEP1: Tax Depreciation Rates General Determination Number 1 (as previously amended) by inserting into the "Medical and Medical Laboratory" industry category, in the appropriate alphabetical order, the general asset class, estimated useful life, diminishing value depreciation rate and straight-line depreciation rate listed below. Columns 3 and 4 apply to items purchased prior to 1 April 2005. Columns 5 and 6 apply to items purchased on or after 1 April 2005:  
      
    
    | 1   | 2   | 3   | 4   | 5   | 6   |
    | --- | --- | --- | --- | --- | --- |
    | General asset class | Estimated useful life (years) | DV banded dep'n rate before 1/4/05 (%) | SL equiv banded dep'n rate before 1/4/05 (%) | DV banded dep'n rate from 1/4/05 (%) | SL equiv banded dep'n rate from 1/4/05 (%) |
    | Psychological testing sets | 10  | 18  | 12.5 | 20  | 13.5 |
    
3.  **Interpretation**  
    In this determination, unless the context otherwise requires, expressions have the same meaning as in the Income Tax Act 2004 and the Tax Administration Act 1994.  
      
    This determination is signed by me on the 27th day of September 2006

**Susan Price**  
Senior Tax Counsel

### Determination DEP56:

#### Tax Depreciation Rates General Determination Number 56

1.  **Application**  
    Pursuant to section 91AAG(6) of the Tax Administration Act 1994 this determination replaces Determination PROV3: Tax Depreciation Rates Provisional Determination Number 3 issued on 2 May 1995.  
      
    This determination applies to taxpayers who own assets in the classes listed below.  
      
    This determination applies to "depreciable property" other than "excluded depreciable property" for the 2005/2006 and subsequent income years.
2.  **Determination**  
    Pursuant to section 91AAF of the Tax Administration Act 1994 I hereby amend Determination DEP1: Tax Depreciation Rates General Determination Number 1 (as previously amended) by inserting into the "Building Fit-out" and "Transportation" asset categories, in the appropriate alphabetical order, the general asset class, estimated useful life, diminishing value depreciation rates and straight-line depreciation rates listed below. Columns 3 and 4 apply to items purchased prior to 1 April 2005. Columns 5 and 6 apply to items purchased on or after 1 April 2005:  
      
    
    | 1   | 2   | 3   | 4   | 5   | 6   |
    | --- | --- | --- | --- | --- | --- |
    | General asset class | Estimated useful life (years) | DV banded dep'n rate before 1/4/05 (%) | SL equiv banded dep'n rate before 1/4/05 (%) | DV banded dep'n rate from 1/4/05 (%) | SL equiv banded dep'n rate from 1/4/05 (%) |
    | Metal speed humps | 5   | 33  | 24  | 40  | 30  |
    
3.  **Interpretation**  
    In this determination, unless the context otherwise requires, expressions have the same meaning as in the Income Tax Act 2004 and the Tax Administration Act 1994.  
      
    This determination is signed by me on the 27th day of September 2006.

**Susan Price**  
Senior Tax Counsel

### Determination DEP57:

#### Tax Depreciation Rates General Determination Number 57

1.  **Application**  
    Pursuant to section 91AAG(6) of the Tax Administration Act 1994 this determination replaces Determination PROV5: Tax Depreciation Rates Provisional Determination Number 5 issued on 23 July 1996.  
      
    This determination applies to taxpayers who own assets in the class listed below.  
      
    This determination applies to "depreciable property" other than "excluded depreciable property" for the 2005/2006 and subsequent income years.
2.  **Determination**  
    Pursuant to section 91AAF of the Tax Administration Act 1994 I hereby amend Determination DEP1: Tax Depreciation Rates General Determination Number 1 (as previously amended) by inserting into the "Agriculture, Horticulture and Aquaculture" industry category, in the appropriate alphabetical order, the general asset class, estimated useful life, diminishing value depreciation rates and straight-line depreciation rates listed below. Columns 3 and 4 apply to items purchased prior to 1 April 2005. Columns 5 and 6 apply to items purchased on or after 1 April 2005:  
      
    
    | 1   | 2   | 3   | 4   | 5   | 6   |
    | --- | --- | --- | --- | --- | --- |
    | General asset class | Estimated useful life (years) | DV banded dep'n rate before 1/4/05 (%) | SL equiv banded dep'n rate before 1/4/05 (%) | DV banded dep'n rate from 1/4/05 (%) | SL equiv banded dep'n rate from 1/4/05 (%) |
    | Wintering pads (rubber) | 6.66 | 26  | 18  | 30  | 21  |
    
3.  **Interpretation**  
    In this determination, unless the context otherwise requires, expressions have the same meaning as in the Income Tax Act 2004 and the Tax Administration Act 1994.  
      
    This determination is signed by me on the 27th day of September 2006.

**Susan Price**  
Senior Tax Counsel

### Determination DEP58:

#### Tax Depreciation Rates General Determination Number 58

1.  **Application**  
    Pursuant to section 91AAG(6) of the Tax Administration Act 1994 this determination replaces Determination PROV6: Tax Depreciation Rates Provisional Determination Number 6 issued on 9 June 1997.  
      
    This determination applies to taxpayers who own assets in the class listed below.  
      
    This determination applies to "depreciable property" other than "excluded depreciable property" for the 2005/2006 and subsequent income years.
2.  **Determination**  
    Pursuant to section 91AAF of the Tax Administration Act 1994 I hereby amend Determination DEP1: Tax Depreciation Rates General Determination Number 1 (as previously amended) by inserting into the "Software" asset category, in the appropriate alphabetical order, the general asset class, estimated useful life, diminishing value depreciation rate and straight-line depreciation rate listed below. Columns 3 and 4 apply to items purchased prior to 1 April 2005. Columns 5 and 6 apply to items purchased on or after 1 April 2005:  
      
    
    | 1   | 2   | 3   | 4   | 5   | 6   |
    | --- | --- | --- | --- | --- | --- |
    | General asset class | Estimated useful life (years) | DV banded dep'n rate before 1/4/05 (%) | SL equiv banded dep'n rate before 1/4/05 (%) | DV banded dep'n rate from 1/4/05 (%) | SL equiv banded dep'n rate from 1/4/05 (%) |
    | Kiwiplus – Kiwifruit Software Package – designed for a specific year | 1   | 100 | 100 | 100 | 100 |
    
3.  **Interpretation**  
    In this determination, unless the context otherwise requires, expressions have the same meaning as in the Income Tax Act 2004 and the Tax Administration Act 1994.  
      
    This determination is signed by me on the 27th day of September 2006.

**Susan Price**  
Senior Tax Counsel

### Determination DEP59:

#### Tax Depreciation Rates General Determination Number 59

1.  **Application**  
    Pursuant to section 91AAG(6) of the Tax Administration Act 1994 this determination replaces Determination PROV7: Tax Depreciation Rates Provisional Determination Number 7 issued on 23 June 1998.  
      
    This determination applies to taxpayers who own assets in the class listed below.  
      
    This determination applies to "depreciable property" other than "excluded depreciable property" for the 2005/2006 and subsequent income years.
2.  **Determination**  
    Pursuant to section 91AAF of the Tax Administration Act 1994 I hereby amend Determination DEP1: Tax Depreciation Rates General Determination Number 1 (as previously amended) by inserting into the "Fishing" industry category, in the appropriate alphabetical order, the general asset class, estimated useful life, diminishing value depreciation rate and straight-line depreciation rate listed below. Columns 3 and 4 apply to items purchased prior to 1 April 2005. Columns 5 and 6 apply to items purchased on or after 1 April 2005:  
      
    
    | 1   | 2   | 3   | 4   | 5   | 6   |
    | --- | --- | --- | --- | --- | --- |
    | General asset class | Estimated useful life (years) | DV banded dep'n rate before 1/4/05 (%) | SL equiv banded dep'n rate before 1/4/05 (%) | DV banded dep'n rate from 1/4/05 (%) | SL equiv banded dep'n rate from 1/4/05 (%) |
    | Peurulus (baby crayfish) traps | 1   | 100 | 100 | 100 | 100 |
    
3.  **Interpretation**  
    In this determination, unless the context otherwise requires, expressions have the same meaning as in the Income Tax Act 2004 and the Tax Administration Act 1994.  
      
    This determination is signed by me on the 27th day of September 2006.

**Susan Price**  
Senior Tax Counsel

Report a Problem with this Page or Publication

DEP55

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP55

Issued

27 Sep 2006
[Skip to main content](#main-content-tt)

DEP60

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

20 Nov 2006

Tax Depreciation Rates General Depreciation Determination
=========================================================

Determination DEP60 (Nov 2006) sets a general depreciation rate for builders' planks (wooden).

This determination may be cited as "Determination DEP60: Tax Depreciation Rates General Determination Number 60".

1.  **Application**  
      
    This determination applies to taxpayers who own the asset class listed below.  
      
    This determination applies to "depreciable property" other than "excluded depreciable property" for the 2006/2007 and subsequent income years.  
    
2.  **Determination**  
      
    Pursuant to section 91AAF of the Tax Administration Act 1994 I hereby amend Determination DEP 1: Tax Depreciation Rates General Determination Number 1 (as previously amended).  
      
    

*   Inserting into the "Contractors, builders, and quarrying" industry category the general asset class, estimated useful life, and diminishing value and straight-line depreciation rate listed below:

  

| Contractors, building and quarrying | Estimated useful life(years) | DV banded dep'n rate(%) | SL equivalent banded dep'n rate(%) |
| --- | --- | --- | --- |
| Builders' planks (wooden) | 3   | 67  | 67  |

  
7.  **Interpretation**  
      
    In this determination, unless the context otherwise requires, expressions have the same meaning as in the Tax Administration Act 1994 and the Income Tax Act 2004.

This determination is signed by me on the 20th day of November 2006.

**Susan Price**  
Senior Tax Counsel

Report a Problem with this Page or Publication

DEP60

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP60

Issued

20 Nov 2006
[Skip to main content](#main-content-tt)

DEP61

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

19 Jun 2007

Child restraints (capsules and car seats) for hire
==================================================

Determination DEP61 (2007) sets a depreciation rate for child restraints (capsules and car seats) for hire/rental.

In _Tax Information Bulletin, Volume 19, No. 4_ (May 2007) on page 4, we advised that a draft general depreciation determination proposing the setting of a general depreciation rate for "Rental car seats" was available for comment. The one submission we received on the draft agreed with the rates we proposed.

The Commissioner has now issued the determination. It is reproduced below and may be cited as "Determination DEP61: Tax Depreciation Rates Determination General Determination No. 61". The determination inserts a new asset class "Child restraints (capsules and car seats) for hire" into the "Transportation" asset category. It is based on an estimated useful life (EUL) for the assets of 5 years.

* * *

This determination may be cited as "Determination DEP61: Tax Depreciation Rates General Determination Number 61"

1.  **Application**  
      
    This determination applies to taxpayers who own assets in the "Transportation" asset category that are in the asset classes set out below.  
      
    This determination applies to "depreciable property" other than "excluded depreciable property" for the 2005-06 and subsequent income years.  
      
    
2.  **Determination**  
      
    Pursuant to section 91AAG(4) of the Tax Administration Act 1994 I hereby amend Determination DEP1: Tax Depreciation Rates General Determination Number 1 (as previously amended) by inserting into the "Transportation" asset category, the general asset class, estimated useful life, and diminishing value and straight-line depreciation rates listed below. Columns 3 and 4 apply to items purchased prior to 1 April 2005. Columns 5 and 6 apply to items purchased on or after 1 April 2005:  
      
    
    | 1   | 2   | 3   | 4   | 5   | 6   |
    | --- | --- | --- | --- | --- | --- |
    | General asset class | Estimated useful life (years) | DV banded dep'n rate before 1/4/05 (%) | SL equiv banded dep'n rate before 1/4/05 (%) | DV banded dep'n rate from 1/4/05 (%) | SL equiv banded dep'n rate from 1/4/05 (%) |
    | Child restraints (capsules and car seats) for hire | 5   | 33  | 24  | 40  | 30  |
    
      
    
3.  **Interpretation**  
      
    In this determination, unless the context otherwise requires, expressions have the same meaning as in the Income Tax Act 2004 and the Tax Administration Act 1994.

This determination is signed by me on the 19th day of June 2007.

**Susan Price**  
(Senior Tax Counsel)

Report a Problem with this Page or Publication

DEP61

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP61

Issued

19 Jun 2007
[Skip to main content](#main-content-tt)

DEP62

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

27 Jun 2007

Buildings and structures
========================

Determination DEP62 (2007) amends the 'Building and structures' rate following legislation changing the methods for calculating depreciation rates.

This determination results from the depreciation changes in the Taxation (Depreciation, Payment Dates Alignment, FBT, and Miscellaneous Provisions) Act 2006. This legislation changed the methods for calculating depreciation rates for items of depreciable property. The depreciation rates for certain items that are not buildings, acquired on or after 1 April 2005 are calculated using the double declining balance method (i.e. the diminishing value rate), with a straight-line equivalent. The depreciation rate for buildings, acquired on or after 19 May 2005 is calculated using a straight-line formula, with a diminishing value equivalent.  
  
As a result of these legislative amendments, this determination amends the "Buildings and Structures (not specified)" asset class in the "Buildings and Structures" asset category in Determination DEP1: Tax Depreciation Rates General Determination Number 1. This is because the buildings and structures economic rates are calculated using different provisions and also because not all structures are buildings.  
  
There are two parts to this determination. The first part applies to structures and to buildings acquired before 19 May 2005. It separates out structures from the "Buildings and structures (not specified)" asset class to create two separate classes: the "Buildings (not specified) (acquired before 19 May 2005)" asset class and the "Structures (not specified)" asset class. The second part of the determination inserts a new asset class: the "Buildings (not specified) (acquired on or after 19 May 2005)" asset class.

### Tax Depreciation Rates General Determination Number 62

This determination may be cited as "Determination DEP62: Tax Depreciation Rates General Determination Number 62".

### 1.   Application

This determination applies to taxpayers who own items of depreciable property of the kind referred to in the asset classes listed below.

There are two parts to this determination. Part A of the determination applies to structures and to buildings acquired before 19 May 2005. Part B of the determination applies to buildings acquired on or after 19 May 2005.

### 2.   Determination

Pursuant to section 91AAF of the Tax Administration Act 1994 I hereby amend Determination DEP1: Tax Depreciation Rates General Determination Number 1 (as previously amended) by:

#### Part A

*   Amending the "Buildings and Structures (not specified)" asset class in the "Buildings and Structures" asset category by removing the words "and structures" and changing the asset class as listed below:  
      
    
    | Asset class | Estimated Useful life (years) | DV banded depn rated (%) | SL equiv. banded depn rate (%) |
    | --- | --- | --- | --- |
    | Buildings (not specified) (acquired before 19 May 2005) | 50  | 4   | 3   |
    
      
      
    
*   Inserting into the "Buildings and Structures" asset category the general asset class, estimated useful life, and diminishing value and straight-line depreciation rates listed below:  
      
    
    | Asset class | Estimated Useful life (years) | DV banded depn rated (%) | SL equiv. banded depn rate (%) |
    | --- | --- | --- | --- |
    | Structures (not specified) | 50  | 4   | 3   |
    

#### Part B

*   Inserting into the "Buildings and Structures" asset category the general asset class, estimated useful life, and diminishing value and straight-line depreciation rates listed below:  
      
    
    | Asset class | Estimated Useful life (years) | DV banded depn rated (%) | SL equiv. banded depn rate (%) |
    | --- | --- | --- | --- |
    | Buildings (not specified) (acquired on or after 19 May 2005) | 50  | 3   | 2   |
    

### 3.   Interpretation

In this determination, unless the context otherwise requires, expressions have the same meaning as in the Income Tax Act 2004.

This determination is signed by me on the 27th day of June 2007.

**Susan Price**  
Senior Tax Counsel, Public Rulings

Report a Problem with this Page or Publication

DEP62

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP62

Issued

27 Jun 2007
[Skip to main content](#main-content-tt)

DEP66

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

04 Mar 2008

Tax Depreciation Rates General Determination Number 66
======================================================

Determination DEP66 (2008) sets a general depreciation rate for set-top boxes without hard drives and personal video recorders without hard drives.

### Application

This determination applies to taxpayers who own items of depreciable property of the kinds listed in the tables below that have been acquired on or after 1 April 2005.

This determination applies for the 2005/2006 and subsequent income years.

### Determination

Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the economic rates to apply to the kinds of items of depreciable property listed in the tables below by:

*   Adding into the "Hotels, Motels, Restaurants, Cafe's, Taverns and Takeaway Bars", "Residential Rental Property Chattels", and "Telecommunications" industry categories the general asset class, estimated useful life, and diminishing value and straight-line depreciation rates listed in the table below.
    
    | **General asset class** | **Estimated useful life (years)** | **DV rate (%)** | **SL rate (%)** |
    | --- | --- | --- | --- |
    | Set-top boxes without hard drive and personal video recorders (PVRs) without hard drive | 5   | 40  | 30  |
    
*   Adding into the "Hotels, Motels, Restaurants, Cafés, Taverns and Takeaway Bars", and "Residential Rental Property Chattels" industry categories the general asset classes, estimated useful lives, and diminishing value and straight-line depreciation rates listed in the table below.
    
    | **General asset class** | **Estimated useful life (years)** | **DV rate (%)** | **SL rate (%)** |
    | --- | --- | --- | --- |
    | Digital versatile disc (DVD) recorders with hard drive | 4   | 50  | 40  |
    | Digital versatile disc (DVD) recorders without hard drive | 5   | 40  | 30  |
    

### Interpretation

In this determination, unless the context otherwise requires, expressions have the same meaning as in the Income Tax Act 2004 and the Tax Administration Act 1994.

This determination is signed by me on the 4th day of March 2008.

**Susan Price**  
Senior Tax Counsel

Report a Problem with this Page or Publication

DEP66

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP66

Issued

04 Mar 2008
[Skip to main content](#main-content-tt)

DEP68

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

09 May 2008

General Depreciation Determination DEP68
========================================

Determination DEP68 (2008) sets a depreciation rate and amends the 'Telecommunications' industry category relating to satellites.

This determination may be cited as "Determination DEP68: Tax Depreciation Rates General Determination Number 68".

### 1\.  Application

This determination applies to taxpayers who own items of depreciable property of the kinds listed in the table below that have been acquired on or after 1 April 2008.

This determination applies for the 2008/09 and subsequent income years.

### 2\.  Determination

Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the economic rates to apply to the kinds of items of depreciable property listed in the table below by:

*   Inserting into the "Telecommunications" industry category the general asset classes, estimated useful lives, and diminishing value and straight-line depreciation rates listed below:
    
    | **Telecommunications** | **Estimated useful life (years)** | **DV banded dep'n rate (%)** | **SL equiv** **banded dep'n** **rate (%)** |
    | --- | --- | --- | --- |
    | Satellites (geosynchronous orbit) | 15  | 13  | 8.5 |
    

  

### 3\.  Consequential change

As a consequence of this determination, an existing general asset class is no longer required and so it is necessary to:

*   Delete from the "Telecommunications" industry category the general asset class, estimated useful life and diminishing value and straight-line depreciation rates listed below:
    
    | **Telecommunications** | **Estimated useful life (years)** | **DV banded dep'n rate (%)** | **SL equiv** **banded dep'n** **rate (%)** |
    | --- | --- | --- | --- |
    | Satellites | 5   | 33  | 24  |
    

  

### 4\.  Interpretation

In this determination, unless the context otherwise requires, expressions have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on the 9th day of May 2008.

**Susan Price**  
Senior Tax Counsel  
Public Rulings

Report a Problem with this Page or Publication

DEP68

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP68

Issued

09 May 2008
[Skip to main content](#main-content-tt)

DEP69

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

30 May 2008

General Depreciation Determination DEP69
========================================

Determination DEP69 (May 2008) sets a general depreciation rate for flight simulators.

This determination may be cited as "Determination DEP69: Tax Depreciation Rates General Determination Number 69".

##### Note to determination DEP69:

This determination applies both to the 2007/2008 income year, and the 2008/2009 and subsequent income years and is issued pursuant to section 91AAF of the Tax Administration Act 1994, having regard to the application of section ZA 2(2) of the Income Tax Act 2007.

### 1.  Application

This determination applies to taxpayers who own items of depreciable property of the kinds listed in the table below.

This determination applies for the 2007/2008 and subsequent income years.

### 2\.  Determination

Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the economic rates to apply to the kinds of items of depreciable property listed in the table below by:

*   Adding into the "Transportation" asset category the general asset classes, estimated useful lives, and diminishing value and straight-line depreciation rates listed in the table below.
    
    | General asset class | Estimated useful life | DV rate (acquired before 1/4/05) (%) | SL rate (acquired before 1/4/05) (%) | DV rate (acquired on or after 1/4/05 (%) | SL rate (acquired on or after 1/4/05 (%) |
    | --- | --- | --- | --- | --- | --- |
    | Flight Simulators (FTD and FNPT Certifiable) Aircraft Specific (full-motion) | 15.5 | 12  | 8   | 13  | 8.5 |
    | Flight Simulators (FTD and FNPT Certifiable) Aircraft Specific (non-motion) | 8   | 22  | 15.5 | 25  | 17.5 |
    | Flight Simulators (FTD and FNPT Certifiable) Upgradeable/ Multi Aircraft (non-motion) | 15.5 | 12  | 8   | 13  | 8.5 |
    | Flight Simulators (Non-Certifiable) (non-motion) | 4   | 40  | 30  | 50  | 40  |
    
*   Adding into the "Leisure" industry category the general asset classes, estimated useful lives, and diminishing value and straight-line depreciation rates listed in the table below.
    
    | General asset class | Estimated useful life | DV rate (acquired before 1/4/05) (%) | SL rate (acquired before 1/4/05) (%) | DV rate (acquired on or after 1/4/05) (%) | SL rate (acquired on or after 1/4/05) (%) |
    | --- | --- | --- | --- | --- | --- |
    | Flight Simulators (FTD and FNPT Certifiable) Aircraft Specific (non-motion) | 8   | 22  | 15.5 | 25  | 17.5 |
    | Flight Simulators (FTD and FNPT Certifiable) Upgradeable/ Multi Aircraft (non-motion) | 15.5 | 12  | 8   | 13  | 8.5 |
    | Flight Simulators (Non-Certifiable) (non-motion) | 4   | 40  | 30  | 50  | 40  |
    

### 3\.  Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on the 30th day of May 2008.

**Susan Price**  
Senior Tax Counsel, Public Rulings

Report a Problem with this Page or Publication

DEP69

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP69

Issued

30 May 2008
[Skip to main content](#main-content-tt)

DEP70

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

06 Jun 2008

General Depreciation Determination DEP70
========================================

Determination DEP70 (2008) sets a depreciation rate for plant supports (hanging retractable wire) in the 'Agriculture, Horticulture, and Aquaculture' category.

Determination DEP70: Tax Depreciation Rates General Determination Number 70

##### Note to determination DEP70:

This determination applies both to the 2007/2008 income year, and the 2008/2009 and subsequent income years and is issued pursuant to section 91AAF of the Tax Administration Act 1994, having regard to the application of section ZA 2(2) of the Income Tax Act 2007.

### 1. Application

This determination applies to taxpayers who own items of depreciable property of the kind listed in the table below that have been acquired on or after 1 April 2005.

This determination applies for the 2007/2008 and subsequent income years.

### 2. Determination

Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the economic rates to apply to the kind of items of depreciable property listed in the table below by:

*   Adding into the "Agriculture, Horticulture, and Aquaculture" industry category the general asset class, estimated useful life, and diminishing value and straight-line depreciation rates listed in the table below.
    
    | General asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
    | --- | --- | --- | --- |
    | Plant supports (hanging retractable wire) | 5   | 40  | 30  |
    

### 3.  Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on the 6th day of June 2008.

**Susan Price**  
Director

Report a Problem with this Page or Publication

DEP70

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP70

Issued

06 Jun 2008
[Skip to main content](#main-content-tt)

DEP74

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

31 Mar 2010

Tax Depreciation Rates General Determination Number 74
======================================================

Determination DEP74 sets a general economic depreciation rate for automated dairy drafting systems including gates, hardware and software and installation costs.

* * *

### Automated dairy drafting systems - Depreciation

The Commissioner has set a general economic depreciation rate for automated dairy drafting systems. These systems consist of a series of computer controlled drafting gates, opened or closed by hydraulic or vacuum powered rams. Its components include gates, rams, computer hardware and software, cabling and installation costs.

**Expense items**

The systems work by attaching programmable ear tags to the cows. The tag is read by an electronic sensor as the animal approaches the drafting gate so that the animal can be directed left or right for treatment, or allowed to go straight down the race and be returned to the paddock. The electronic ear tags are single use and are not recovered from the animal before it is culled. The Commissioner considers the ear tags to be consumable aids and should be expensed.

* * *

This determination may be cited as "Determination DEP 74: Tax Depreciation Rates General Determination Number 74".

1.  **Application**

*   This determination applies to taxpayers who own items of depreciable property of the kind listed in the table below that have been acquired during the 2009/2010 and subsequent income years.

2.  **Determination**

*   Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination, the economic rates to apply to the kind of items of depreciable property listed in the table below by:  
      
    *   Adding into the "Agriculture, Horticulture and Aquaculture" industry category the asset class, estimated useful life and diminishing values and straight-line rates listed below:
    *     
        
        | Asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
        | --- | --- | --- | --- |
        | Automated dairy drafting systems | 6.6 | 30  | 21  |
        

3.  **Interpretation**

*   In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on the 31st day of March 2010.

Rob Wells  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP74

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP74

Issued

31 Mar 2010
[Skip to main content](#main-content-tt)

DEP75

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

10 Sep 2010

Tax Depreciation Rates General Determination Number 75
======================================================

Determination DEP75 (2010) sets a depreciation rate for Marine Fender Systems, which are attached to wharves for protection of the wharf and vessels.

#### Marine Fender Systems - Depreciation Determination

* * *

The Commissioner has set a general economic depreciation rate for Marine Fender Systems. Marine Fender Systems are attached to wharves.

Their function is to absorb large amounts of kinetic energy and to protect the wharf and vessels moored or being moored to the wharf from being damaged should the vessel collide with the wharf.

The Marine Fender Systems consist of a series of steel box frames with plastic or rubber fenders behind. These are mounted on a structural steel frame and may be further supported by chains. They may also use high strength plastic tanks as pneumatic buffers.

* * *

### Determination DEP75 : Tax Depreciation Rates General Determination Number 75

This determination may be cited as "Determination DEP 75: Tax Depreciation Rates General Determination Number 75".

1.  **Application**

*   This determination applies to taxpayers who own items of depreciable property of the kind listed in the table below that have been acquired during the 2009/2010 and subsequent income years.

2.  **Determination**

*   Pursuant to section 91AAF of the Tax Administration Act 1994, I set in this determination the economic rate to apply to the kind of items of depreciable property listed in the table below by:  
      
    *   Adding into the "Building and Structures" asset category the asset class, estimated useful life and diminishing value and straight-line depreciation rates listed below:
    *     
        
        | Asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
        | --- | --- | --- | --- |
        | Marine Fender Systems | 20  | 10  | 7   |
        

3.  **Interpretation**

*   In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed on the 10th day of September 2010.

Rob Wells  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP75

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP75

Issued

10 Sep 2010
[Skip to main content](#main-content-tt)

DEP76

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

23 Dec 2010

Tax Depreciation Rates General Determination Number 76
======================================================

Determination DEP76 (Dec 2010) introduces Motorhomes as a new asset class description.

* * *

**Note to determination DEP76:**

This determination applies to the 2010/11 income year and subsequent income years and is issued pursuant to section 91AAF of the Tax Administration Act 1994.

This determination introduces Motorhomes as a new asset class description.  The Commissioner considers that Motorhomes have previously been included within the Campervan asset class description. Motorhomes acquired before 2010/11 income year should continue to be depreciated using the appropriate depreciation rate for Campervans.

For Campervans and Motorhomes that are exclusively available for hire for periods longer than 1 month, the rates in section EE 29 of the Income Tax Act 2007 apply (30% D.V. or 21% S.L.).

For Campervans and Motorhomes that are not available exclusively for hire for periods longer than 1 month, there are three different depreciation rates that may apply depending on when the campervan or motorhome was acquired. The different rates apply to the following:

*   Campervans and Motorhomes acquired in the 2010/11 and later income year;
*   Campervans and Motorhomes acquired after 1 April 2005, but prior to the 2010/11 income year; and
*   Campervans and Motorhomes acquired prior to 1 April 2005

For Campervans and Motorhomes acquired in the 2010/11 and later income years, the depreciation rates are set under section EE 30 of the Income Tax Act 2007 (Economic rate for plant, equipment, or building, with high residual value). These are new depreciation rates.

For Campervans and Motorhomes acquired prior to the 2010/11 income year, the depreciation rates are set under sections EZ 23 and EE 27 respectively.  These rates remain unchanged. The asset class descriptions have been updated to take into account the new depreciation rates and to make it clear the Campervan asset class included Motorhomes.

* * *

### Determination DEP76: Tax Depreciation Rates General Determination Number 76

This determination may be cited as "Determination DEP 76: Tax Depreciation Rates Determination Number 76".

1.  **Application**  
    This determination applies to taxpayers who own items of depreciable property of the kind listed in the table below that have been acquired during the 2010/11 and later income years.
2.  **Determination**  
    Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the economic rates to apply to the kind of items of depreciable property listed in the table below by:
    *   Adding into the "Leisure" industry category and the "Hire Equipment" and "Transportation" asset categories the general asset classes, estimated useful lives, and diminishing value and straight-line depreciation rates listed in the table below:  
          
        
        | General asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
        | --- | --- | --- | --- |
        | Campervans\* acquired during or after the 2010/11 income year | 8   | 18  | 12.5 |
        | Motorhomes\* acquired during or after the 2010/11 income year | 8   | 18  | 12.5 |
        
          
        \* Under section EE 30 (Economic rate for plant, equipment, or building, with high residual value) residual value estimated at 20%.
3.  **Consequential changes**  
    As a consequence of this determination, the existing general asset classes for "Campervans" in the "Leisure" industry category and the "Transportation" asset category are amended as follows:  
      
    
    | General asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
    | --- | --- | --- | --- |
    | Campervans (including Motorhomes) acquired before 1 April 2005 | 10  | 18  | 12.5 |
    | Campervans (including Motorhomes) acquired on or after 1 April 2005 but prior to the 2010/11 income year | 10  | 20  | 13.5 |
    
      
    The above change does not represent a change of depreciation rates. The only change is that the asset class description has been clarified.  
    
4.  **Interpretation**  
    In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed on the 23rd day of December 2010.

**Rob Wells**  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP76

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP76

Issued

23 Dec 2010
[Skip to main content](#main-content-tt)

DEP77

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

24 Mar 2011

Motor vehicles rented for short-term periods of 1 month or less Depreciation Determination Number 77
====================================================================================================

Determination DEP77 (Mar 2011) amends the provisional depreciation rate for motor vehicles rented for short-term periods of 1 month or less.

* * *

### Note to determination DEP77

In _Tax Information Bulletin_ Vol 10, No 6 (June 1998) we published a general depreciation determination, "Determination DEP34: Tax Depreciation Rates General Determination Number 34" for certain classes of motor vehicles and trailers when they are rented for short-term hire periods of 1 month or less.

The determination added those asset classes to both the "Transportation" and "Hire Equipment (Where on short-term hire of 1 month or less only)" asset categories. We have been advised that some taxpayers, referring only to the "Transportation" asset category, have been using the depreciation rates set for "short-term" hire even though the assets in question may have been hired for periods longer than 1 month (in this context, 1 month refers to a calendar month).

We have therefore issued a new depreciation determination deleting the old asset classes set out in DEP 34 from the "Transportation" asset category, and inserting new asset classes making it clear that the higher depreciation rates that may be used for motor vehicles and trailers used for short-term hire apply only to those assets that are hired only for periods of one month or less. The depreciation rates, however, are unchanged.

We have also been asked to clarify whether or not the asset category could be used for assets that are used for both short-term (1 month or less) and longer term hire (periods of longer than 1 month). This issue arises where taxpayers generally hire the motor vehicles / trailers for short-term (1 month or less) periods, but may occasionally hire them for a longer term.

It is the Commissioner's view that the higher depreciation rates available for assets that are used for short-term hire periods should only be used for assets that are exclusively hired for short-term periods. Taxpayers who hire assets for both short and longer terms should not use the depreciation rates that apply for short-term periods.

* * *

### General Depreciation Determination DEP77

This determination may be cited as "Determination DEP77: Tax Depreciation Rates General Determination Number 77".

### 1\. Application

This determination applies to taxpayers who own items of depreciable property of the kinds listed in the table below.

This determination applies for the 2010/11 and subsequent income years.

### 2\. Determination

Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the economic rate/s to apply to the kind/s of items of depreciable property listed in the table below by:

*   Deleting from the "Transportation" asset category the general asset classes, estimated useful lives and diminishing value and straight-line depreciation rates listed below:

| Transportation | Estimated useful life (years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Motor vehicles – Class NA (for transporting light goods that have a gross vehicle mass not exceeding 3.5 tonnes and used for short-term hire). | 6.66 | 30  | 21  |
| Motor vehicles – Class NB (for transporting medium goods that have a gross vehicle mass exceeding 3.5 tonnes but not exceeding 12 tonnes and used for short-term hire). | 8   | 25  | 17.5 |
| Motor vehicles – class NC (for transporting heavy goods that have a gross vehicle mass exceeding 12 tonnes and used for short-term hire). | 6.66 | 30  | 21  |
| Trailers – Class TA and TB (for transporting very light and light goods that have a gross vehicle mass not exceeding 3.5 tonnes and used for short-term hire) excluding domestic trailers. | 10  | 20  | 13.5 |
| Trailers – Class TC (for transporting medium goods that have a gross vehicle mass exceeding 3.5 tonnes but not exceeding 10 tonnes and used for short-term hire). | 12.5 | 16  | 10.5 |
| Trailers – Class TD (for transporting heavy goods that have a gross vehicle mass exceeding 10 tonnes and used for short-term hire). | 10  | 20  | 13.5 |
| Trailers – domestic.  Not exceeding 1 tonne.  Used for short-term hire | 6.66 | 30  | 21  |
| Motor vehicles (for transporting people, up to and including 12 seats and used for short-term hire). | 4   | 50  | 40  |
| Forklift trucks (8 tonnes and over used for short-term hire) | 8   | 25  | 17.5 |
| Forklift trucks (under 8 tonnes used for short-term hire). | 6.66 | 30  | 21  |

*   Adding into the category "Transportation" asset category the general asset classes, estimated useful lives, and diminishing value and straight-line depreciation rates listed below:

| Transportation | Estimated useful life (years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Motor vehicles – Class NA (for transporting light goods which have a gross vehicle mass not exceeding 3.5 tonnes and are used for short-term hire of 1 month or less only). | 6.66 | 30  | 21  |
| Motor vehicles – Class NB (for transporting medium goods which have a gross vehicle mass exceeding 3.5 tonnes but not exceeding 12 tonnes and used for short-term hire of 1 month or less only). | 8   | 25  | 17.5 |
| Motor vehicles – class NC (for transporting heavy goods which have a gross vehicle mass exceeding 12 tonnes and used for short-term hire of 1 month or less only). | 6.66 | 30  | 21  |
| Trailers – Class TA and TB (for transporting very light and light goods which have a gross vehicle mass not exceeding 3.5 tonnes and used for short-term hire of 1 month or less only) excluding domestic trailers. | 10  | 20  | 13.5 |
| Trailers – Class TC (for transporting medium goods which have a gross vehicle mass exceeding 3.5 tonnes but not exceeding 10 tonnes and used for short-term hire of 1 month or less only). | 12.5 | 16  | 10.5 |
| Trailers – Class TD (for transporting heavy goods which have a gross vehicle mass exceeding 10 tonnes and used for short-term hire of 1 month or less only). | 10  | 20  | 13.5 |
| Trailers – domestic.  Not exceeding 1 tonne.  Used for short-term hire of 1 month or less only. | 6.66 | 30  | 21  |
| Motor vehicles (for transporting people, up to and including 12 seats and used for short-term hire of 1 month or less only). | 4   | 50  | 40  |
| Forklift trucks (8 tonnes and over used for short-term hire of 1 month or less only). | 8   | 25  | 17.5 |
| Forklift trucks (under 8 tonnes used for short-term hire of 1 month or less only). | 6.66 | 30  | 21  |

### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed on the 24th day of March 2011

Rob Wells  
Manager  
LTS Technical Standards

Report a Problem with this Page or Publication

DEP77

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP77

Issued

24 Mar 2011
[Skip to main content](#main-content-tt)

DEP86

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

05 Nov 2013

Tax Depreciation Rates General Determination Number 86
======================================================

General Determination DEP86: Depreciation Rate for frost fans (mobile) used to protect crops from frost conditions and hot temperatures.

* * *

**Note to determination DEP86:**

The Commissioner has set a general depreciation rate for Frost Fans (mobile) by adding a new asset class to the “Agriculture, Horticulture and Aquaculture” industry category.

Frost Fans (mobile) are used to protect crops from frost conditions and hot temperatures.

* * *

### Determination DEP86: Tax Depreciation Rates General Determination Number 86

1.  **Application**  
    This determination applies to taxpayers who own depreciable property of the kind listed in the table below.  
    This determination applies from the 2013/14 and subsequent income years.
2.  **Determination**  
    Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the economic rates to apply to the kind of items of depreciable property listed in the table below by:
    *   Adding into the “Agriculture, Horticulture and Aquaculture” industry category new asset class, estimated useful life, and general diminishing value and straight line depreciation rates as listed below:  
         
        
        | Agriculture, horticulture and aquaculture | Estimated useful life (years) | DV rate (%) | SL rate (%) |
        | --- | --- | --- | --- |
        | Frost Fan (mobile) | 15.5 | 13  | 8.5 |
        
3.  **Interpretation**  
    In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed on the 5th day of November 2013.

**Rob Wells**  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP86

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP86

Issued

05 Nov 2013
[Skip to main content](#main-content-tt)

DEP87

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

28 Apr 2014

Depreciation rate for tablet computers and electronic media storage devices (including smartphones and MP3 players and similar devices)
=======================================================================================================================================

DEP87 (2014) sets a depreciation rate for tablet computers and electronic media storage devices (including smartphones and MP3 players and similar devices).

This determination may be cited as "Determination DEP87: Tablet computers and electronic media storage devices (including smartphones and MP3 players and similar devices)".

* * *

#### 1\. Application

This determination applies to taxpayers who own items of depreciable property of the kind listed in the tables below.

This determination applies from the 2013/14 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the economic rate to apply to the kind of items of depreciable property listed in the table below by:

*   Adding into the "Computers" asset category, the new asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below:

| Asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Tablet computers and electronic media storage devices (including smartphones, MP3 players and similar devices) | 3   | 67  | 67  |

*   Adding into the "Leisure" industry category, the new asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below:

| Asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| MP3 and similar devices, such as iPods and the like | 3   | 67  | 67  |

*   Deleting from the "Office Equipment and Furniture" asset category, the asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below:

| Asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Telephone (mobile) | 3   | 67  | 67  |

*   Adding into the "Office Equipment and Furniture" asset category, the new asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below:

| Asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Mobile telephones, including smartphones | 3   | 67  | 67  |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed on the 28th day of April 2014.

Sharyn Rea  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP87

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP87

Issued

28 Apr 2014
[Skip to main content](#main-content-tt)

DEP88

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

07 May 2014

Depreciation rate for pet grooming and cleaning equipment
=========================================================

Determination DEP88 (2014) sets a depreciation rate for pet grooming and cleaning equipment.

#### Note to Determination DEP88

The Commissioner has set general depreciation rates for pet grooming and cleaning equipment by adding a new asset category of "Pet grooming and cleaning equipment". The new asset category applies only to services provided for the grooming and cleaning of domestic animals (including horses).

As the determination shows, the pet grooming and cleaning equipment consists of a number of components that have different useful lives. To date we have identified:

*   Pet washers (portable);
*   Pet dryer units (portable);
*   Pet/animal vacuum clipper units;
*   Pet/animal clippers.

An asset category default rate is also set, to provide for other equipment used for pet grooming and cleaning not listed above.

* * *

### Determination DEP88: Tax Depreciation Rates General Determination Number 88

#### 1\. Application

This determination applies to taxpayers who own depreciable property of the kind listed in the table below.

This determination applies from the 2014 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAG of the Tax Administration Act 1994 the general determination will apply to the kind of items of depreciable property listed in the table below by:

*   Adding a new "Pet grooming and cleaning equipment" asset category, new asset classes, estimated useful lives, and diminishing value and straight line depreciation rates as listed below:

| Asset class | Estimated useful life (years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Pet washers (portable) | 8   | 25  | 17.5 |
| Pet dryer units (portable) | 5   | 40  | 30  |
| Pet/animal vacuum clipper units | 5   | 40  | 30  |
| Pet/animal clippers | 5   | 40  | 30  |
| Pet grooming and cleaning equipment (default class) | 8   | 25  | 17.5 |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on the 7th day of May 2014.

Sharyn Rea  
Manager, LTS, Technical Standards

Report a Problem with this Page or Publication

DEP88

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP88

Issued

07 May 2014
[Skip to main content](#main-content-tt)

DEP90

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

10 Feb 2015

Depreciation Rate for drones and integrated accessories including remote controllers and software, used for photography, surveillance and video/movie production
================================================================================================================================================================

Determination DEP90 (2015) sets a depreciation rate for drones and accessories used for photography, surveillance and video/movie production.

#### Note to Determination DEP 90

The Commissioner has recently been asked to consider what depreciation rate should apply for drones when used for photography, surveillance and video/movie production.  

The Commissioner considers that the asset includes the remote controller, software and carrying case – and where the asset also includes a camera which is built into and fully integrated into the drone, the camera will be part of the asset.

On the other hand, where the drone merely provides an aerial platform onto which a camera may be mounted, the drone and the camera will be regarded as separate assets which should be depreciated separately.

Similarly, the asset does not include items such as computers or laptops where these are used in conjunction with the drone.

* * *

### General Determination DEP90: Depreciation Rate for drones and integrated accessories including remote controllers and software, used for photography, surveillance and video/movie production.

This determination may be cited as "Determination DEP90: Drones and integrated accessories including remote controllers and software, used for photography, surveillance and video/movie production".

#### 1\. Application

This determination applies to taxpayers who own items of depreciable property of the kind listed in the tables below:

This determination applies for the 2013/14 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the provisional rate to apply to the kind of items of depreciable property listed in the table below by:

*   adding into the "Audio and Video Recording Studios and Professional Photography" asset category, the new asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Drones and integrated accessories including remote controllers and software, used for photography, surveillance and video/movie production | 4   | 50  | 40  |

*   adding into the "Leisure" industry category, the new asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Drones and integrated accessories including remote controllers and software, used for photography, surveillance and video/movie production | 4   | 50  | 40  |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on the 10th day of February 2015.

Rob Wells  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP90

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP90

Issued

10 Feb 2015
[Skip to main content](#main-content-tt)

DEP91

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

15 Mar 2015

Depreciation Rate for gas detectors (hand-held) and gas detectors (fixed)
=========================================================================

Determination DEP91 (2015) sets general depreciation rates for gas detectors that are battery operated hand-held types or wired/fixed to plant and machinery.

#### Note to Determination DEP 90

The Commissioner sets general depreciation rates for gas detectors that are battery operated hand-held types or wired/fixed to plant and machinery.

Gas detectors are used by many industries that use gas or work in enclosed spaces.  Although the hand-held type of gas detector may come within the existing asset class for "Instruments hand-held" under the "Scientific and laboratory equipment (excluding equipment used in a medical laboratory)" asset category, many business users may not identify the asset class of "instruments hand-held" as applicable to hand-held gas detectors used in other industries.  Consequently, this determination adds two new gas detector asset classes to the "Factory and other sundries", "Refrigeration", "Scientific and laboratory equipment (excluding equipment used in a medical laboratory)" and "Water and effluent treatment (where not industry specified)" asset categories, to provide more certainty for taxpayers when considering the depreciation treatment of gas detectors.

* * *

### Determination DEP91: Tax Depreciation Rates General Determination Number DEP91

#### 1\. Application

This determination applies to taxpayers who own depreciable property of the kind listed in the table below.

This determination applies from the 2015 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAG of the Tax Administration Act 1994 the general determination will apply to the kind of items of depreciable property listed in the table below by:

*   Adding into the "Factory and other sundries", "Refrigeration", "Scientific and laboratory equipment (excluding equipment used in a medical laboratory)" and "Water and effluent treatment (where not industry specified)" asset categories, new asset classes, estimated useful lives, and diminishing value and straight line depreciation rates as listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Gas detectors (hand-held) | 5   | 40  | 30  |
| Gas detectors (fixed) | 10  | 20  | 13.5 |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by me on the 16th day of March 2015.

Rob Wells  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP91

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP91

Issued

15 Mar 2015
[Skip to main content](#main-content-tt)

DEP92

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

19 Mar 2015

Depreciation Rate for wool/shearing sheds
=========================================

General Determination DEP92 (Mar 2015) sets a general depreciation rate for wool/shearing sheds.

#### Note to Determination DEP92

The Commissioner sets a specific general depreciation rate for wool/shearing sheds by adding new asset class to the "Agricultural, horticulture and aquaculture" industry category and the "Buildings and structures" asset category.

The introduction of a specific asset class is to clarify the treatment of wool/shearing sheds for depreciation purposes.  There is concern that since the changes to the depreciation rules announced in the May 2010 Budget, that there is no specific asset class for wool/shearing sheds has seen taxpayers treating these assets inconsistently for depreciation purposes.  Some taxpayers have categorised wool/shearing shed buildings as "barns" and continued to claim depreciation on the basis these buildings are "barns" with an estimated useful life of 20 years.

Prior to the May 2010 Budget, the generally accepted view has been (although not published) that wool/shearing sheds are buildings with timber and/or steel framing, with an estimated useful life of 50 years.

Wool/shearing shed design is specialised, usually incorporating covered holding pens (sheep must be dry and have evacuated bowels for shearing), filling and catching pens, a raised shearing board (where shearing takes place), release pens and counting out pens.  Wool rooms (where the wool is sorted and baled) are also included.  Pens have grated floors so that the sheep droppings fall through and do not contaminate the wool.  Wool/shearing sheds experience only seasonal use (the main shearing period) although they may be used for crutching (shearing the crutch area to prevent fly-strike) several times during the warmer months.

It is suggested that taxpayers who have incorrectly claimed depreciation for wool/shearing sheds on the basis of those purpose-built buildings are "barns" was never a legitimate option, and they may like to make a voluntary disclosure to correct their tax position.

The application date for the specific asset class for "wool/shearing sheds", will be from the 2015 and subsequent income years. Prior to the 2015 income year, affected taxpayers should have been using the "buildings with steel or steel and timber framing" asset default class for wool/shearing sheds, with an estimated useful life of 50 years.

* * *

### Determination DEP92: Tax Depreciation Rates General Determination Number 92

#### 1\. Application

This determination applies to taxpayers who own depreciable property of the kind listed in the table below.

This determination applies from the 2015 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAG of the Tax Administration Act 1994 the general determination will apply to the kind of items of depreciable property listed in the table below by:

*   Adding into the "Agricultural, horticulture and aquaculture" industry category and the "Buildings and structures" asset category, a new asset class, estimated useful life, and diminishing value and straight line depreciation rates as listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Wool/shearing shed | 50  | 0   | 0   |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed on the 19th day of March 2015.

Rob Wells  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP92

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP92

Issued

19 Mar 2015
[Skip to main content](#main-content-tt)

DEP93

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

09 Jul 2015

Depreciation Rate for portable fencing (galvanised steel)
=========================================================

General Determination DEP93 (Jul 2015) sets general depreciation rates for 'Portable fencing (galvanised steel)'.

#### Note to Determination DEP93

The Commissioner of Inland Revenue sets general depreciation rates for "Portable fencing (galvanised steel)". New asset classes are added into the “Contractors, builders and quarrying” industry category and “Hire equipment” asset category, as set out below.

Portable fencing that is available for short-term hire (one month or less) will also fall within the asset class of "Contractors, building and quarrying equipment for hire with a general DV rate based on an estimated useful life of 8 years" in the "Hire equipment (short-term hire of one month or less only)" asset category.

Portable fencing is short-term, easily movable fencing consisting of lightweight panels, weighted feet and clamps. It is easy to store, transport, erect and remove.

Portable fencing generally has an estimated useful life of 8 years. However, portable fencing that is hired out to be used by others has an estimated useful life of 5 years.

* * *

### Determination DEP93: Tax Depreciation Rates General Determination Number 93

#### 1\. Application

This determination applies to taxpayers who own depreciable property of the kind listed in the table below.

This determination applies from the 2015 and subsequent income years. Taxpayers who have filed their income tax return prior to this determination being issued may request amended assessments pursuant to section 113 of the Tax Administration Act 1994.

#### 2\. Determination

Pursuant to section 91AAG of the Tax Administration Act 1994, the general determination will apply to the kind of items of depreciable property listed in the table below by:

*   adding into the "Contractors, builders and quarrying" industry category, a new asset class with the estimated useful life and diminishing value and straight line depreciation rates as listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
| --- | --- | --- | --- |
| Portable fencing (galvanised steel) | 8   | 25  | 17.5 |

*   adding into the "Hire equipment" asset category, a new asset class with the estimated useful life and diminishing value and straight line depreciation rates as listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
| --- | --- | --- | --- |
| Portable fencing (galvanised steel) | 5   | 40  | 30  |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by Rob Wells on the 9th day of July 2015.

**Rob Wells**  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP93

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP93

Issued

09 Jul 2015
[Skip to main content](#main-content-tt)

DEP94

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

04 Aug 2015

Depreciation Rate for carports (freestanding or lean-to)
========================================================

General Determination DEP94 (Aug 2015) sets a general depreciation rate for a new asset class, 'Carports (freestanding or lean-to)'.

#### Note to Determination DEP94

The Commissioner has set a general depreciation rate for a new asset class “Carports (freestanding or lean-to)”, under the “Buildings and structures” asset category, within the Commissioner’s Table of Depreciation Rates.

A carport is a simple lean-to structure that is attached to an external wall of a building for support or may be freestanding supported by columns. Most carports may be distinguished from buildings because (whilst they obviously have a roof) they do not have four walls, or if they have walls, they are usually not completely enclosed and/or are not weather-tight.

Lean-to carports, although attached to a wall of a building for support, can be easily removed from a building without damage to the building. In addition, a reasonable person could easily distinguish a carport as a separate structure from a building. A lean-to carport would not be viewed as part of the fabric of a building, therefore is viewed as a separate structure.

Carports designed as an open sided extension of a building roof structure, would not be easily removed without damage to the common roof structure. A reasonable person would not easily distinguish a carport as a separate structure from a building, which is more likely to be viewed as being an extension of the building and form part of the fabric of a building. Carports that are an extension of a building roof structure are not viewed as a separate asset and form part of a building.

If the structure used to shelter cars comprises a roof and four complete, weather-tight walls, then the structure is a building. If the structure to provide shelter for vehicles has a roof, three weather-tight walls and an open front (presence or absence of a door in the opening is irrelevant) it is therefore a building.

* * *

### Determination DEP94: Tax Depreciation Rates General Determination Number 94

#### 1\. Application

This determination applies to taxpayers who own depreciable property of the kind listed in the table below.

This determination applies from the 2015 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAG of the Tax Administration Act 1994, the general determination will apply to the kind of items of depreciable property listed in the table below by:

*   adding into the “Buildings and structures” asset category, a new asset class, estimated useful life, and diminishing value and straight line depreciation rates as listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
| --- | --- | --- | --- |
| Carports (freestanding or lean-to) | 33.3 | 6   | 4   |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by Rob Wells on the 4th day of August 2015.

**Rob Wells**  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP94

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP94

Issued

04 Aug 2015
[Skip to main content](#main-content-tt)

DEP95

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

04 Aug 2015

Depreciation Rate for rail passenger service electric multiple units
====================================================================

Determination DEP95 (2015) sets depreciation rate for a new asset class 'Rail passenger service electric multiple units' under the Transportation asset category.

#### Note to Determination DEP95

The Commissioner has set a general depreciation rate for a new asset class “Rail passenger service electric multiple units” (EMUs), under the “Transportation” asset category, within the Commissioner’s Table of Depreciation Rates.

An EMU consists of a self-propelled passenger carriage semi-permanently linked to a passenger trailer carriage (not motorised). There is no separate locomotive as the electric traction motors and drive wheels are incorporated into one or more of the carriages. EMUs are used to provide rail commuter passenger services and are usually formed from two or more semi-permanently coupled carriages, with a drive cab and motor at each end.

* * *

### Determination DEP95: Tax Depreciation Rates General Determination Number 95

#### 1\. Application

This determination applies to taxpayers who own depreciable property of the kind listed in the table below.

This determination applies from the 2015 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAG of the Tax Administration Act 1994, the general determination will apply to the kind of items of depreciable property listed in the table below by:

*   adding into the “Transportation” asset category, a new asset class, estimated useful life, and diminishing value and straight line depreciation rates as listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
| --- | --- | --- | --- |
| Rail passenger service electric multiple units | 25  | 8   | 6   |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by Rob Wells on the 4th day of August 2015.

**Rob Wells**  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP95

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP95

Issued

04 Aug 2015
[Skip to main content](#main-content-tt)

DEP96

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

28 Sep 2015

Depreciation Rate for specialised oil and gas industry equipment
================================================================

Determination DEP96 (2015) sets a depreciation rate for specialised oil and gas industry equipment used to evaluate and repair existing wellbores.

#### Note to Determination

The Commissioner has set general depreciation rates for several items of specialised equipment used by oil and gas industry support specialists to evaluate, repair or stimulate the performance of existing wellbores, not currently provided for under the "Oil and Gas Industry" category, within the Commissioner’s Table of Depreciation Rates.

The asset class for "Tools, downhole" includes shifting tools, fishing tools, tungsten stembars, pulling tools, gauge rings, broaches and centering tools.  The asset class does not include perforating guns which are made by several shaped explosives charges within the gun.  As most retrievable perforating guns can be used once only as they distort when fired and are weakened, the Commissioner considers these items are consumable items and be treated as revenue expenditure items.

Mobile steel tanks, usually constructed of welded mild steel to store or distribute water and other liquids, are viewed by the Commissioner to generally have an estimated useful life of 20 years.  However, a new asset class of "Mobile storage tanks (mild steel, welded)" has been added to the "Oil and gas industry" category with an estimated useful life of 15.5 years due to harsh environmental conditions.  In addition, some tanks are used to hold and distribute corrosive acid or alkali and under those circumstances are viewed to have a shorter life of 10 years, as provided for in this determination.

* * *

### Determination DEP96: Tax Depreciation Rates General Determination Number 96

#### 1\. Application

This determination applies to taxpayers who own depreciable property of the kind listed in the table below.

This determination applies from the 2014 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAG of the Tax Administration Act 1994 the general determination will apply to the kind of items of depreciable property listed in the table below by:

*   Adding into the "Oil and gas industry" category, new asset classes, estimated useful lives, and diminishing value and straight line depreciation rates as listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate  <br>(%) | SL rate  <br>(%) |
| --- | --- | --- | --- |
| Tools, downhole  <br>(perforating guns excluded; to be treated as consumables, and revenue expense items) | 5   | 40  | 30  |
| Treating irons | 10  | 20  | 13.5 |
| Coiled tubing units | 12.5 | 16  | 10.5 |
| Wireline units | 12.5 | 16  | 10.5 |
| Slickline units | 12.5 | 16  | 10.5 |
| Mobile steel tanks (mild steel, welded)  <br>\- If affected by acid or alkali | 15.5  <br>10 | 13  <br>20 | 8.5  <br>13.5 |
| Stuffing boxes and lubricator/riser pipes | 10  | 20  | 13.5 |
| Slickline floor sheaves | 10  | 20  | 13.5 |
| Spools | 10  | 20  | 13.5 |
| Pumping units | 10  | 20  | 13.5 |
| Nitrogen pumping units | 10  | 20  | 13.5 |
| Nitrogen generating units | 10  | 20  | 13.5 |

#### 3\. Interpretation

In this draft determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed by Rob Wells on the 28th day of September 2015.

**Rob Wells**  
LTS Manager, Technical Standards

Report a Problem with this Page or Publication

DEP96

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP96

Issued

28 Sep 2015
[Skip to main content](#main-content-tt)

DEP98

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

11 May 2017

Kiwifruit overhead mesh shelters
================================

General determination DEP98 (2017) inserts an asset class for 'Kiwifruit overhead mesh shelters' into the depreciation tables.

**Note to Determination DEP98:** The Commissioner has issued depreciation rate determination for kiwifruit overhead mesh shelters.

This asset consists of a self-supporting frame and wires that support an overhead mesh shelter that protects the fruit from weather events (wind, hail, UV ) and bird and pests.

1.  **Application**  
    This determination applies to taxpayers who own items of depreciable property of the kind listed in the tables below:  
      
    This determination applies for the 2017 and subsequent income years.
2.  **Determination**  
    Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the rate to apply to the kind of items of depreciable property listed in the table below by
    
    *   Adding into the "Buildings and Structures" asset category, the new asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below
    
    | Asset class | Estimated useful life (years) | DV rate % | SL rate % |
    | --- | --- | --- | --- |
    | Kiwifruit overhead mesh shelters | 12.5 | 16  | 10.5 |
    
3.  **Interpretation**  
    In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.  
      
    This determination is signed by me on the 11th day of May 2017.

Vanessa Montgomery  
Acting Manager, LTS Technical Standards

Report a Problem with this Page or Publication

DEP98

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP98

Issued

11 May 2017
[Skip to main content](#main-content-tt)

DEP99

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Issued

01 Jun 2017

Campervans and Motorhomes
=========================

General Determination DEP99 corrects the depreciation rate for Campervans and Motorhomes for the 2010/11 and subsequent income years.

#### Note to Determination DEP99

This determination corrects the applicable depreciation rate for Campervans and Motorhomes, for the 2010/11 and subsequent income years. The item also clarifies the Commissioner's view that these assets are:

*   considered to have a high residual value (20% residual value)
*   assets acquired during or after the 2010/11 income year are viewed as having an estimated useful life of 8 years,
*   assets acquired prior to the 2010/11 income year were viewed as having an estimated useful life of 10 years.

Taxpayers impacted by the retrospective depreciation rate change can ask for an adjustment to assessments for past years in terms of section 113 of the Tax Administration Act 1994[1](#01)
, to the extent that legislation permits a refund to be made under Subpart RM of the Income Tax Act 2007. Alternatively, other taxpayers may choose to simply begin to use the new depreciation rate prospectively and make the appropriate depreciation recovery adjustment upon disposal of a campervan or motorhome..

* * *

### Determination DEP99: Tax Depreciation Rates General Determination Number DEP99

#### 1\. Application

This determination applies to taxpayers who own items of depreciable property of the kind listed in the table below:

This determination applies to the 2010/11 and subsequent income years.

#### 2\. Determination

Pursuant to section 91AAF of the Tax Administration Act 1994 I set in this determination the rate to apply to the kind of items of depreciable property listed in the table below by:

*   deleting from the "Leisure" industry category and the "Hire equipment" and "Transportation" asset categories, the asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Campervans acquired during or after the 2010/11 income year | 8   | 18  | 12.5 |
| Motorhomes acquired during or after the 2010/11 income year | 8   | 18  | 12.5 |

*   deleting from the "Leisure" industry category, the asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Campervans (including Motorhomes) acquired before 1 April 2005 | 10  | 18  | 12.5 |
| Campervans (including Motorhomes) acquired on or after 1 April 2005 but prior to the 2010/11 income year | 10  | 20  | 13.5 |

*   adding into the "Hire equipment" and "Transportation" asset categories, the new asset class, estimated useful life, and general diminishing value and straight-line depreciation rates listed below:

| Asset class | Estimated useful life  <br>(years) | DV rate (%) | SL rate (%) |
| --- | --- | --- | --- |
| Campervans acquired between 1 April 2005 and prior to the 2010/11 income year | 10  | 20  | 13.5 |
| Campervans acquired during or after the 2010/11 income year (residual value estimated at 20%) | 8   | 20  | 13.5 |
| Motorhomes acquired between 1 April 2005 and prior to the 2010/11 income year | 10  | 20  | 13.5 |
| Motorhomes acquired during or after the 2010/11 income year (residual value estimated at 20%) | 8   | 20  | 13.5 |

#### 3\. Interpretation

In this determination, unless the context otherwise requires, words and terms have the same meaning as in the Income Tax Act 2007 and the Tax Administration Act 1994.

This determination is signed on the 1st day of June 2017.

Rob Wells  
LTS Manager, Technical Standards

#### Footnote

\[1\] More information regarding section 113 can be found in Standard Practice Statement _[SPS 16/01: Requests to amend assessments](/standard-practice-statements/investigations/sps-1601-requests-to-amend-assessments "SPS 16/01: Requests to amend assessments")
._

Report a Problem with this Page or Publication

DEP99

[Determinations](/publications#f-ttTypeFacet=Determinations%7CAIM,Determinations%7CCOVID-19%20variations,Determinations%7CCRS%7CExclusions,Determinations%7CCRS%7CJurisdictions,Determinations%7CDepreciation%7CGeneral,Determinations%7CDepreciation%7CProvisional,Determinations%7CEmergency%20Events,Determinations%7CFinancial%20arrangements%7CGeneral,Determinations%7CFinancial%20arrangements%7CSpecial,Determinations%7CForeign%20currency%7CApprovals,Determinations%7CForeign%20currency%7CCFCs%20and%20FIFs,Determinations%7CInternational%20tax%7CCFCs,Determinations%7CInternational%20tax%7CDisclosure%20exemptions,Determinations%7CInternational%20tax%7CForeign%20investment%20funds,Determinations%7CLivestock%7CAverage%20market%20value,Determinations%7CLivestock%7CStandard%20costs,Determinations%7CMiscellaneous,Determinations%7CStandard-cost%20household%20service%7CBoarding%20service%20providers,Determinations%7CStandard-cost%20household%20service%7CChildcare%20providers,Determinations%7CStandard-cost%20household%20service%7CHome%20share%20care%20providers,Determinations%7CStandard-cost%20household%20service%7CShort-stay%20accommodation&sort=%40irscttissuedatetime%20descending&numberOfResults=25)
 / Depreciation / General

Reference

DEP99

Issued

01 Jun 2017
