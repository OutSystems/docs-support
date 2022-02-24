---
summary:
tags:
---

# Application Objects

An Application Object (AO) is a measurement of the complexity of the applications you run on the OutSystems platform. Each **screen**, **database table**, and **API method** in your apps count as 1 AO. 

## Details on AO counting for Screens
* Web screens, email screens, and mobile web screens each count as 1 AO. 
* Web blocks are components that exist within a screen, so they don't contribute to the AO count. 
* Tabs and pop-up windows in your Reactive web apps are implemented within an existing screen, so they don't contribute to the AO count either. 
* Tabs and pop-up windows created as distinct screens in Service Studio, such as with traditional web apps, count as 1 AO for each screen. 
* Tooltips do not contribute to the AO count.

## Details on AO counting for Database Tables
* Tables you create within the OutSystems platform database each count as 1 AO.
* Tables you import from external databases for use in your app each count as 1 AO.
* Entities using local storage, such as for use with mobile apps, each count as 1 AO.
* Tables created by the OutSystems platform, such as the Users table where end user information is stored, do not contribute to the AO count.

## Details on AO counting for API Methods
* Each API method you *create* ([REST](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/REST/Expose_REST_APIs) or [SOAP Web Service](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Exposing_SOAP_Web_Services/Expose_a_SOAP_Web_Service)) counts as 1 AO. 
* Each API method you *consume* ([REST](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/REST/Consume_REST_APIs), [SOAP Web Service](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Consuming_SOAP_Web_Services), SAP BAPI, etc.) within each app counts as 1 AO.
* APIs that are within a C#-based extension do not contribute to the AO count.

## Other Scenarios relating to AO counting
* Within the same runtime environment, each database table and API method only counts as 1 AO, even when used by multiple apps within this same environment.
* Disabled applications continue to contribute to the AO count until they are deleted.
* Components sourced from [OutSystems Forge](https://www.outsystems.com/forge/) also contribute to the AO count.

## AO Limits
OutSystems subscriptions typically include rights to run applications up to a specified number of AOs, with options for upgrading AO capacity that vary by subscription. You can review your AO limit within the Customer Portal and you can see the current AO count displayed for each runtime environment within Service Center. If you have multiple production runtime environments, you'll sum the AO counts for each to determine your total AO count. When your AO count exceeds the AO limit specified in your subscription, you need to upgrade to remain in compliance with the license terms. Please contact your OutSystems sales representative for assistance.

In the past, when customers exceeded their AO limit, functionality in the OutSystems Platform could be degraded. This is no longer the case with current versions of the platform. It was previously customary for customers to allocate a portion of their total AO limit to each production runtime environment (when they had multiple) so that each would have a sufficient AO limit for the apps running in that environment. Given the changes in the platform, this practice is no longer necessary.
