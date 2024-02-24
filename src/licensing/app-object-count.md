---
summary: Application Object counting and licensing in OutSystems 11 and OutSystems Developer Cloud.
tags:
locale: en-us
guid: cd994c70-9dcc-46ed-b423-84099beac39a
app_type: traditional web apps, mobile apps, reactive web apps
helpids: 30497, 30455
platform-version: o11, odc
figma:
---

# Application Objects

An Application Object (AO) is a measurement of the complexity of your applications on the OutSystems platform. Each **screen**, **entity/database table**, **API method**, and **Event** in your apps count as 1 AO. AOs are counted the same in OutSystems 11 and OutSystems Developer Cloud, except where noted below.

## Details on AO counting for Screens
* Web screens, email screens, and mobile web screens each count as 1 AO. 
* Web blocks are components that exist within a screen, so they don't contribute to the AO count. 
* Tabs and pop-up windows in your Reactive web apps are implemented within an existing screen, so they don't contribute to the AO count either. 
* Tabs and pop-up windows created as distinct screens in Service Studio, such as with traditional web apps, count as 1 AO for each screen. 
* Tooltips don't contribute to the AO count.

## Details on AO counting for Entities/Database tables

* Entities you create within OutSystems (both normal [entities](https://success.outsystems.com/Documentation/11/Developing_an_Application/Use_Data/Data_Modeling/Entities) and [static entities](https://success.outsystems.com/Documentation/11/Developing_an_Application/Use_Data/Data_Modeling/Static_Entities)) each count as 1 AO.
* Entities you import from external databases (for example, a table or a view) for use in your app each count as 1 AO.
* Entities using local storage, such as for use with mobile apps, each count as 1 AO.
* Static entities included in a library each count as 1 AO.
* Tables created by the OutSystems platform, such as the Users table where end user information is stored, don't contribute to the AO count.

## Details on AO counting for API methods

* Each API method you *create* ([REST](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/REST/Expose_REST_APIs) or [SOAP Web Service](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Exposing_SOAP_Web_Services/Expose_a_SOAP_Web_Service)) counts as 1 AO. 
* Each API method you *consume* ([REST](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/REST/Consume_REST_APIs), [SOAP Web Service](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Consuming_SOAP_Web_Services), SAP BAPI, etc.) within each app counts as 1 AO.
* API methods included in a library each count as 1 AO.
* APIs that are within a C#-based extension don't contribute to the AO count.

## Details on AO counting for Entities/Database tables

* Entities you create within OutSystems (both normal [entities](https://success.outsystems.com/Documentation/11/Developing_an_Application/Use_Data/Data_Modeling/Entities) and [static entities](https://success.outsystems.com/Documentation/11/Developing_an_Application/Use_Data/Data_Modeling/Static_Entities)) each count as 1 AO.
* Entities you import from external databases (for example, a table or a view) for use in your app each count as 1 AO.
* Entities using local storage, such as for use with mobile apps, each count as 1 AO.
* Static entities included in a library each count as 1 AO.
* Tables created by the OutSystems platform, such as the Users table where end user information is stored, don't contribute to the AO count.

## Details on AO counting for Events

* Each Event you configure within OutSystems Developer Cloud counts as 1 AO.
* Events in OutSystems 11 function differently, and do not contribute to the AO count.

## Other scenarios relating to AO counting

* Within the same runtime environment, each entity and each API method only count as 1 AO, even when used by multiple apps within this same runtime.
* Disabled applications continue to contribute to the AO count until they're deleted.
* Components sourced from [OutSystems Forge](https://www.outsystems.com/forge/) also contribute to the AO count.
* In OutSystems Developer Cloud, you can deploy multiple versions of the same library. Only the version with the highest number of AOs contributes to the AO count.
* In OutSystems 11, libraries that are published to the development runtime environment contribute to the AO count, even when they are not referenced by any applications in that runtime. Unreferenced libraries that are deployed to non-production or production runtimes also contribute to the AO count. In OutSystems Developer Cloud, unreferenced libraries do not contribute to the AO count.
* With libraries, the AO count contributed includes all API methods and static entities in the library, even when not all are referenced or used by apps.

## AO limits

OutSystems subscriptions typically include rights to run applications up to a specified number of AOs, with options for upgrading AO capacity that vary by subscription. With OutSystems 11, you can review your AO limits within the Customer Portal and you can see the current AO usage displayed for each runtime environment within Service Center. With OutSystems Developer Cloud, you can review these within the Subscription section of the ODC Portal.

AO limits only apply to production runtimes. Development and non-production/QA runtimes allow unlimited AOs, but cannot be used for running apps for production use.

### Subscriptions with one production runtime

For subscriptions with one production runtime, you're entitled to run up to the AO limit shown within each runtime, which is the AO capacity licensed on your subscription. When you need to exceed this, you need to upgrade to remain in compliance with the license terms. Please contact your OutSystems sales representative for assistance. 

### Subscriptions with multiple production runtimes

For subscriptions with multiple production runtimes, the AO limit shown represents the total AO capacity licensed on your subscription. You're entitled to run up to this total number of AOs across all production runtimes, so you'll sum the AO usage from each production runtime to determine your total production AO usage. Please contact your OutSystems sales representative for assistance upgrading your AO capacity when needed.
