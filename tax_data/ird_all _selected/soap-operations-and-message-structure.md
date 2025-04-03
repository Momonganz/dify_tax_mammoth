[Skip to main content](#main-content-wrapper)

**Rotorua office temporarily closed** | Our Rotorua office will be closed from 12pm 17 January 2025 until 30 January 2025. For anything urgent, you can call our contact centre.

[Search tips](/about-this-site/search-tips)

Ngā whakahaerenga SOAP me te hanganga karere SOAP operations and message structure
==================================================================================

Our SOAP web services operations contain requests and responses with common structure and fields. These are used across different schemas and tax types for reusable service design architecture.

XSD schema structure
--------------------

The XSD schema structure for gateway services are:

*   Common.xsd
*   ServiceCommon.xsd
*   SpecificProduct.xsd

All schemas for different services import a common.xsd which has some data types specific to Inland Revenue.

This common.xsd will be used in other gateway services outside of the //namespace and must be kept up to date.

You can view and download the operations, schemas and data definitions for each service in our services catalogue.

[Services catalogue](/digital-service-providers/services-catalogue)

SOAP messages structure
-----------------------

All messages require a header containing the **Action:** parameter. The body must contain a structured XML payload.

Refer to the WSDL for the correct addresses. Refer to samples or the WSDL element wsdl:binding/soap12:operation/soapAction for the URL to use.

The online WSDLs for gateway services define an 'any' XML request and response structure, which then relies on a group of XSDs to define the data structure of those requests and responses.

Each request and response type will define a lower, 'wrapper' element. To simplify analysis and code generation, a development-oriented version of the WSDL and XSDs is provided with the build pack that has the 'any' elements replaced with relevant types.

Schema (XSD) validations
------------------------

When you send structured XML through gateway this will be checked against our published XSDs.

This is partially a late binding validation, performed after an authentication review. The message structure of these services is a simple request/response.

The XML request will be checked for well-formed XML before the schema validation. Responses to these requests will be in XML format and defined by the same schemas as requests.

Any XML submissions in the body that do not match the provided schemas will not be accepted. Incorrect namespaces will also fail validation against the published schemas.

Any malformed XML will instantly be rejected before any schema validation.

Show all

Example SOAP request structure

**<soap:Envelope** xmlns:soap="http://www.w3.org/2003/05/soap-envelope"

xmlns:sft="https://services.ird.govt.nz/GWS/SoftwareIntermediation/"

xmlns:gcl="https://services.ird.govt.nz/GWS/SoftwareIntermediation/:types/RetrieveClientListRequest"

**xmlns:a**\="http://www.w3.org/2005/08/addressing">

     **<soap:Header>**

 **<a:Action>**https://services.ird.govt.nz/GWS/SoftwareIntermediation/SoftwareIntermediation/_Operation_**</a:Action>** 

     **</soap:Header>**

     **<soap:Body>**

<sft:RetrieveClientList>

     <sft:RetrieveClientListRequestMsg>

         <rcl:RetrieveClientListRequestWrapper>

             <RetrieveClientListRequest xmlns:xsi…

                <…XML payload…>

             </RetrieveClientListRequest>

         </rcl:RetrieveClientListRequestWrapper>

     </sft:RetrieveClientListRequestMsg>

</sft:RetrieveClientList>

     **</soap:Body>**

**</soap:Envelope>**

Example SOAP response structure

**<s:Envelope** xmlns:s="http://www.w3.org/2003/05/soap-envelope"  xmlns:a=[http://www.w3.org/2005/08/addressing](http://www.w3.org/2005/08/addressing)

xmlns:si=http://services.ird.govt.nz/GWS/SoftwareIntermediation/

xmlns:b=http://services.ird.govt.nz/GWS/SoftwareIntermediation/:types/RetrieveClientListResponse

xmlns:i=[http://www.w3.org/2001/XMLSchema-instance](http://www.w3.org/2001/XMLSchema-instance)

xmlns:cmn\="urn:www.ird.govt.nz/GWS:types/Common.v1"\>

      **<s:Header>**

**<a:Action** s:mustUnderstand="1">

https://services.ird.govt.nz/GWS/SoftwareIntermediation/SoftwareIntermediation/RetrieveClientListResponse

**</a:Action>**

      **</s:Header>**

      **<s:Body>**

            <si:RetrieveClientListResponse >

 <si:RetrieveClientListResult>

        <b:RetrieveClientListResponseWrapper>

             <cmn:RetrieveClientListResponse\>

                <cmn:statusMessage>

                    <cmn:statusCode>0</statusCode>

                    <cmn:errorMessage/>

                </cmn:statusMessage>

             </cmn:RetrieveClientListResponse>

                     </b:RetrieveClientListResponseWrapper>

               </si:RetrieveClientListResult>

           </si:RetrieveClientListResponse>

       **</s:Body>**

**</s:Envelope>**

#### Tasks

*   [Getting started](/digital-service-providers/guides-and-docs/getting-started "Getting started")
    

#### Topics

*   [Services catalogue](/digital-service-providers/services-catalogue "Services catalogue")
    
*   [Gateway services architecture](/digital-service-providers/guides-and-docs/gws-architecture "Gateway services architecture")
    
*   [What you need to know to integrate with us](/digital-service-providers/guides-and-docs/what-you-need-to-know-to-integrate-with-us "What you need to know to integrate with us")
    

#### Other Sites

*   [Log in to gateway customer support portal](https://gws.ird.govt.nz/gws)
    
*   [Register organisation for gateway services](https://gws.ird.govt.nz/gws?id=sn_user_registration&sys_id=c11dff9997b44a501ed6344ef053af51)