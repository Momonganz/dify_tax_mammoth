[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Ngā panoni ki te Common Reporting Standard for 2021 Changes to the Common Reporting Standard for 2021
=====================================================================================================

There are some new technical changes happening to the CRS for 2021. These may have an impact on reporting New Zealand financial institutions (NZFIs).

Important

These changes relate to the technical requirements of the data, as prescribed by the CRS XML schema. They do not impact the reporting or due diligence requirements for NZFIs.

The OECD has published an updated ‘Common Reporting Standard XML Schema User Guide for Tax Administrators – Version 3.0’ that provides guidance on the new XML schema (XML schema 2.0) which reflects the new reporting standard.  The new XML schema files have also been published online by the OECD.

Timeline for implementing changes
---------------------------------

From 1 February 2021, all reporting for CRS will need to conform with the new schema, including any corrections to prior reporting periods.

Important

For NZFIs, this means that CRS reporting for the 31 March 2021 year, due to be filed with Inland Revenue by 30 June 2021, will need to comply with the new standard.

Impact for NZFIs
----------------

NZFIs that file using XML will need to ensure that their XML files conform with the new XML schema for the 31 March 2021 reporting year.

NZFIs that use Excel will need to ensure that they are using an up-to-date Excel template. This will be available in myIR from 1 February 2021.

NZFIs that use the online form can continue to do so.

### Changes for all NZFI filers

The following changes apply to all filing methods.

| Change | Details |
| --- | --- |
| Update to country and currency lists | The latest schema has been aligned to the latest updates to the standards set by the International Organization for Standardization. This includes the country code 'XK' for Kosovo. |
| Maximum and minimum length for all string elements | All string (text) elements now have a minimum length of 1 character and a maximum of 200 characters.<br><br>Where the element is required data, a value must be provided for the report to be complete.<br><br>For optional elements, where there is no value, these elements must be omitted. |

### Additional changes for XML filers

In addition to the changes above, NZFIs that file using XML will need to ensure their files comply with the following changes and be aware of the new validation errors.

| Change | Details |
| --- | --- |
| 'Message Type Indicator' now mandatory | The element 'MessageTypeIndic' which indicates if an XML file is new data or corrected/deleted data will now be required to pass validation under the new schema. This was previously an optional element. |
| Schema 'version' attribute now mandatory | The attribute ‘version’ for the root element CRS\_OECD will now be mandatory. This attribute will need to be set to “2.0” for the new schema. The new root element for the XML should be similar (but may differ in namespaces) to the following:<br><br><crs:CRS\_OECD xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:iso="urn:oecd:ties:isocrstypes:v1" xmlns:cfc="urn:oecd:ties:commontypesfatcacrs:v2" xmlns:crs="urn:oecd:ties:crs:v2" xmlns:ftc="urn:oecd:ties:fatca:v1" xmlns:stf="urn:oecd:ties:crsstf:v5" version="2.0"> |

More information and guidance
-----------------------------

If you have any questions about these changes or any other CRS queries, ask us at:

[\[email protected\]](/cdn-cgi/l/email-protection#c6a1aaa9a4a7aae8a7a3a9af86afb4a2e8a1a9b0b2e8a8bc)

You can find the new XML schema files and user guide on the OECD's website.

[Common Reporting Standard User Guide and XML Schema (OECD)](https://www.oecd.org/tax/automatic-exchange/common-reporting-standard/schema-and-user-guide/#d.en.345315)