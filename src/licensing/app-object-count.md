---
summary:
tags:
locale: en-us
guid: cd994c70-9dcc-46ed-b423-84099beac39a
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# Application Objects

An Application Object (AO) is a measurement of the complexity of your applications on the OutSystems platform. Each **screen**, **entity/database table**, and **API method** in your apps count as 1 AO. AOs are counted the same in OutSystems 11 and OutSystems Developer Cloud, except where noted below.

## Details on AO counting for Screens
* Web screens, email screens, and mobile web screens each count as 1 AO. 
* Web blocks are components that exist within a screen, so they don't contribute to the AO count. 
* Tabs and pop-up windows in your Reactive web apps are implemented within an existing screen, so they don't contribute to the AO count either. 
* Tabs and pop-up windows created as distinct screens in Service Studio, such as with traditional web apps, count as 1 AO for each screen. 
* Tooltips don't contribute to the AO count.

## Details on AO counting for Entities/Database tables

* Entities you create within the OutSystems platform database (each [entity](https://success.outsystems.com/Documentation/11/Developing_an_Application/Use_Data/Data_Modeling/Entities) or [static entity](https://success.outsystems.com/Documentation/11/Developing_an_Application/Use_Data/Data_Modeling/Static_Entities) is a database table) each count as 1 AO.
* Entities you import from external databases (for example, a table or a view) for use in your app each count as 1 AO.
* Entities using local storage, such as for use with mobile apps, each count as 1 AO.
* Tables created by the OutSystems platform, such as the Users table where end user information is stored, don't contribute to the AO count.

## Details on AO counting for API methods

* Each API method you *create* ([REST](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/REST/Expose_REST_APIs) or [SOAP Web Service](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Exposing_SOAP_Web_Services/Expose_a_SOAP_Web_Service)) counts as 1 AO. 
* Each API method you *consume* ([REST](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/REST/Consume_REST_APIs), [SOAP Web Service](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Consuming_SOAP_Web_Services), SAP BAPI, etc.) within each app counts as 1 AO.
* APIs that are within a C#-based extension don't contribute to the AO count.

## Other scenarios relating to AO counting

* Within the same runtime environment, each database table and API method only counts as 1 AO, even when used by multiple apps within this same runtime.
* Disabled applications continue to contribute to the AO count until they're deleted.
* Components sourced from [OutSystems Forge](https://www.outsystems.com/forge/) also contribute to the AO count.
* In OutSystems Developer Cloud, you can deploy multiple versions of the same library. Only the version with the highest number of AOs contributes to the AO count.

## AO limits

OutSystems subscriptions typically include rights to run applications up to a specified number of AOs, with options for upgrading AO capacity that vary by subscription. You can review your AO limits within the Customer Portal and you can see the current AO usage displayed for each runtime environment within Service Center. For subscriptions with one production runtime, you are entitled to run up to the AO limit shown within each runtime, which is the AO capacity licensed on your subscription. When you need to exceed this, you need to upgrade to remain in compliance with the license terms. Please contact your OutSystems sales representative for assistance. 

For subscriptions with multiple production runtimes, the AO limit shown represents the total AO capacity licensed on your subscription. You are entitled to run up to this total number of AOs across all production runtimes, so you'll sum the AO usage from each production runtime to determine your total production AO usage. Any AO limits shown in non-production also represent the total AO capacity licensed on your subscription. When you have multiple non-production runtimes that deploy to the same production runtime (i.e., that are part of the same CI/CD pipeline), it is only necessary to include the non-production runtime with the highest AO count from each pipeline in determining the total non-production AO usage. This way you don't double count AOs for the same set of apps that progress through one non-production runtime for system testing and then another for User Acceptance Testing. When your total production or non-production AO usage exceeds the AO limits shown, you need to upgrade to remain in compliance with the license terms. Please contact your OutSystems sales representative for assistance.
