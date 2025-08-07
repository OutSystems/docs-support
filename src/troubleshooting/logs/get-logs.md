---
summary: Learn how to obtain and utilize various logs for troubleshooting in OutSystems 11 (O11) by accessing detailed instructions for each component.
tags: troubleshooting, logging, support and maintenance, technical support, debugging
locale: en-us
guid: 0ffec091-70df-4b3c-9c4b-0a274efd1541
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - frontend developers
  - full stack developers
  - platform administrators
outsystems-tools:
  - service center
coverage-type:
  - unblock
---

# Getting logs for troubleshooting purposes

This article explains how to get the logs and report files from several OutSystems components and other system components. 

In the context of a support case, OutSystems Support might require that you provide some of these files so they can troubleshoot the issues you are experiencing. In this situation, you should get the required files as described in this article and **attach them to your support case**.

Troubleshooting logs allow you to understand the probable cause of slowness in your applications, or what is happening at the moment of a certain action. Below are some of the most used logs for troubleshooting.

## Service Center logs

The [logs for the runtime of the platform](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Monitor_and_Troubleshoot/View_the_Environment_Logs_and_Status#monitoring-area) are available in the **Service Center** console of each environment - application and LifeTime environments. These logs can be helpful when trying to debug a specific feature or behavior and understanding exactly what is happening within that process. You can access the following logs from Service Center:

 * Errors
 * General
 * Traditional Web requests
 * Screen requests
 * Service Actions
 * Integrations
 * Extensions
 * Timers
 * Emails
 * Processes
 * Mobile Apps

<div class="info" markdown="1">

When troubleshooting errors REST and SOAP integrations it may be useful to [adjust the logging level](https://www.outsystems.com/tk/redirect?g=c215f526-4e79-416f-a7ae-4789e0a26a8c).

</div>

[Click here](service-center-logs.md) to learn how to get Service Center Logs.

When you can’t export Service Center logs due to large data volumes, even after reducing the time interval, you may encounter timeouts. To avoid this, the best solution is to extract the logs directly from the database by querying the OSLOG_xxx tables.

## Mobile app generation logs

OutSystems logs the generation steps of a mobile app package, including the stack trace with additional details in case of an error. These logs help us understand which steps were taken while generating the mobile application, and in case of failures, where the generation failed exactly.

[Click here](mabs-logs.md) to learn how to get mobile app generation logs.

## Service Studio logs

The Service Studio report has all the actions performed inside Service Studio within an active session as well as all unhandled exceptions.

In some cases, it's not possible to collect the **Diagnostics Report** or the same does not contain enough information in order to understand the root cause of the misbehavior/error. An example of this is when Service Studio suffers an unrecoverable crash and the **Submit Feedback** pop-up doesn't show up. For such cases, enhanced logging may be necessary.

[Click here](service-studio-logs.md) to learn how to get a Service Studio Report and perform enhanced logging.  

## LifeTime logs

From the LifeTime console, you can obtain the following reports:

 * LifeTime report
 * Staging report
 * User permissions report

[Click here](lifetime-logs.md) to learn how to get these reports.

## Event Viewer logs

The Windows Event Viewer shows a log of application and system messages, including errors, information messages, and warnings.

 * Application Section: In the Application section, you'll find OutSystems services messages. OutSystems Services will log their startup and shutdown information messages here, as well as more severe errors that prevent them from starting or functioning correctly. The value in the Source column will be `OutSystems <service name>`.

 * System Section: In the System section, you’ll also find IIS messages. Examples are application pool recycling events or crash of processes. Application pool recycles are logged as WAS (for Windows Application Server) in the Source column.

[Click here](event-viewer-logs.md) to learn how to get Event Viewer logs.

## Android and iOS device logs

These logs are vital to understanding what's happening at the moment of a certain action or logic point when trying to debug or find a specific cause for an erroneous state (for example, an application crash). The Android device logs list all the actions happening on an Android device such as:
 * Faulty actions that lead to errors
 * Unhandled exceptions
 * Other information that can be used for debugging purposes

[Click here](android-device-logs.md) to learn how to get Android Device logs.

[Click here](ios-device-logs.md) to learn how to get iOS Device logs.

## BPT Utils troubleshooting logs

[BPT Utils](https://www.outsystems.com/forge/component-overview/1313/bpt-utils) is a Forge component that provides information about BPT Processes, including a troubleshooting report.

You'll need the BPT Utils component in your environment. Follow the steps below to install:

1. Download [BPT Utils](https://www.outsystems.com/forge/component-versions/1313) from OutSystems Forge. You will get an OutSystems application file (.oap). There is one version available for OutSystems 9.1, 10 and 11. Make sure to download the version corresponding to your environment.

1. Go to the Service Center console of your environment (`https://<server>/ServiceCenter`).

1. Go to **Factory** » **Applications**.

1. Click the **Publish an Application** link.

1. Click **Choose File** and select the .oap file you downloaded from Forge.

1. Click **1-Click Publish**.

BPT Utils is now installed in your LifeTime environment.

[Click here](bpt-report.md) to learn how to get the BPT Utils troubleshooting report.
    
## Network HAR file

HAR is the short form for **HTTP Archive Format**, which tracks all the logging of web browser's interaction with a site. You may need this file if you encounter the following issues:
  * Performance issues: slow page load, a timeout when performing a certain task, etc.
  * Page rendering: incorrect page format, missing information, etc.

[Click here](har-file.md) to learn how to get the HAR file from different browsers.

## IIS Manager logs

IIS logs are meant to record data from Internet Information Services, web pages, and apps. While IIS itself contributes to the scalability and flexibility of web resources, the log files contain specific statistics about the websites, user data, site visits, IPs, and queries. These files can help you detect a problem in a specific call between your server and another external server or service and understand if there are any underlying network issues.

[Click here](iis-logs.md) to learn how to get IIS logs.

## Java server logs

These logs represent various moments during an application execution in a Java context. With these logs we can understand which methods or functions are being called within a Java application during runtime.

[Click here](java-logs.md) to learn how to get Java stack specific logs.

## OutSystems service logs

These are the logs for the OutSystems services, such as the Scheduler or the Deployment service. These logs help us understand in more detail what is happening within the OutSystems services actions and logic being run during normal operations, such as running timers, compiling modules or synchronizing environments. [Click here](change-logging-levels.md) to read more about changing the logging level for the OutSystems services.

## Database - AWR and ADDM Report

The AWR and ADDM reports are database reports detailing important information about the performance of the database.

[Click here](database-logs.md) to learn how to get database reports.