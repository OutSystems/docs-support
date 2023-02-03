---
summary: OutSystems logs information that helps the troubleshooting of problems. Learn how to get the troubleshooting information from the different OutSystems components and other system components.
tags:
locale: en-us
guid: 0ffec091-70df-4b3c-9c4b-0a274efd1541
app_type: traditional web apps, mobile apps, reactive web apps
---
# Getting logs for troubleshooting purposes

This article explains how to get the logs and report files from several OutSystems components and other system components.

In the context of a support case, OutSystems Support might require that you provide some of these files so they can troubleshoot the issues you are experiencing. In this situation, you should get the required files as described in this article and **attach them to your support case**.

Troubleshooting logs allow you to understand the probable cause of slowness in your applications, or what is happening at the moment of a certain action. Below are some of the most used logs for troubleshooting. 

**Service Center Logs**: The [logs for the runtime of the platform](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Monitor_and_Troubleshoot/View_the_Environment_Logs_and_Status#monitoring-area) are available in the **Service Center** console of each environment - application and LifeTime environments. These logs can be helpful when trying to debug a specific feature or behavior and understanding exactly what is happening within that process. You can access the following reports from Service Center:

 * Errors
 * General logs
 * Web requests
 * Mobile requests
 * Service Actions
 * Integrations
 * Extensions
 * Timers
 * Emails

[Click here](service-center-logs.md) to learn how to get Service Center Logs. 

**Mobile App Generation Logs**: OutSystems logs the generation steps of a mobile app package, including the stack trace with additional details in case of an error. These logs help us understand which steps were taken while generating the mobile application, and in case of failures, where the generation failed exactly.

[Click here](mabs-logs.md) to learn how to get mobile app generation logs. 

**Service Studio Report**: The Service Studio report has all the actions performed inside Service studio within an active session as well as all unhandled exceptions.

[Click here](service-studio-report.md) to learn how to get a Service Studio Report. 

**Lifetime Logs**: From the LifeTime console, you can obtain the following reports:

 * LifeTime report
 * Staging report
 * User permissions report

[Click here](lifetime-logs.md) to learn how to get these reports. 

**Event Viewer Logs**: The Windows Event Viewer shows a log of application and system messages, including errors, information messages, and warnings.
 * Application Section: In the Application section, you'll find OutSystems services messages. OutSystems Services will log their startup and shutdown information messages here, as well as more severe errors that prevent them from starting or functioning correctly. The value in the Source column will be `OutSystems <service name>`.

 * System Section: In the System section, you’ll also find IIS messages. Examples are application pool recycling events or crash of processes. Application pool recycles are logged as WAS (for Windows Application Server) in the Source column.
    
[Click here](event-viewer-logs.md) to learn how to get Event Viewer logs. 
    
**Android and iOS Device Logs**: These logs are vital to understanding what's happening at the moment of a certain action or logic point when trying to debug or find a specific cause for an erroneous state (for example, an application crash). The Android device logs list all the actions happening on an Android device such as:
 * Faulty actions that lead to errors
 * Unhandled exceptions
 * Other information that can be used for debugging purposes

[Click here](android-device-logs.md) to learn how to get Android Device logs.

[Click here](ios-device-logs.md) to learn how to get iOS Device logs. 

**BPT Utils Troubleshooting Logs**: [BPT Utils](https://www.outsystems.com/forge/component-overview/1313/bpt-utils) is a Forge component that provides information about BPT Processes, including a troubleshooting report.

If you haven’t done it yet, you must install BPT Utils component in your LifeTime environment. Follow the steps given below to install:

1. Download [BPT Utils](https://www.outsystems.com/forge/component-versions/1313) from OutSystems Forge. You will get an OutSystems application file (.oap). There is one version available for OutSystems 9.1, 10 and 11. Make sure to download the version corresponding to your LifeTime environment.

1. Go to the Service Center console of your LifeTime environment (`https://<LifeTime_server>/ServiceCenter`).

1. Go to **Factory** » **Applications**.

1. Click the **Publish an Application** link.

1. Click **Choose File** and select the .oap file you downloaded from Forge.

1. Click **1-Click Publish**.

BPT Utils is now installed in your LifeTime environment.

[Click here](bpt-report.md) to learn how to get the BPT Utils troubleshooting report.
    
**Network HAR File**: HAR is the short form for **HTTP Archive Format**, which tracks all the logging of web browser's interaction with a site. You may need this file if you encounter the following issues:
  * Performance issues: slow page load, a timeout when performing a certain task, etc.
  * Page rendering: incorrect page format, missing information, etc.

[Click here](har-file.md) to learn how to get the HAR file from different browsers.
    
**IIS Manager Logs**: IIS logs are meant to record data from Internet Information Services, web pages, and apps. While IIS itself contributes to the scalability and flexibility of web resources, the log files contain specific statistics about the websites, user data, site visits, IPs, and queries. These files can help you detect a problem a specific call between your server and another external server or service and understand if there are any underlying network issues.

[Click here](iis-logs.md) to learn how to get IIS logs. 

**Java Server Logs**: These logs represent various moments during an application execution in a Java context. With these logs we can understand which methods or functions are being called within a Java application during runtime. 

[Click here](java-logs.md) to learn how to get Java Stack specific logs. 
    
**Platform Service Logs**: The Service logs are the logs for the OutSystems services, such as the Scheduler or the Deployment service. These logs help us understand in more detail what is happening within the OutSystems services actions and logic being run during normal operations, such as running timers, compiling modules or synchronizing environments. [Click here](`https://success.outsystems.com/Support/Troubleshooting/Application_lifecycle/Change_OutSystems_platform_logging_levels_-_OSTrace`) to read more about Platform Logs.
    
**Database - AWR and ADDM Report**: The AWR and ADDM reports are database reports detailing important information about the performance of the database. 

[Click here](database-logs.md) to learn how to get database reports. 
