---
summary: OutSystems logs information that helps the troubleshooting of problems. Learn how to get the troubleshooting information from the different OutSystems components and other system components.
tags:
---
# How to get logs for troubleshooting purposes

This article explains how to get the logs and report files from the several OutSystems components and other system components.

In the context of a support case, OutSystems Support might require that you provide some of these files so they can troubleshoot the issues you are experiencing. In this situation, you should get the required files as described in this article and attach them to your support case.

## Get Service Studio Report

When an **unexpected error** occurs in Service Studio, you will get an Unexpected Error window. In this window, you can obtain the error report to send to OutSystems Support.

Do the following to obtain the report:

1. Click **You can help us fix this…** to expand the window, if it’s not expanded.

     ![](images/get-logs-1.png?width=500)

1. Click **View diagnostics report** to open the report in a text editor. In OutSystems 10, use the link **View report**.

     ![](images/get-logs-2.png?width=600)

1. Save the report as a text file. If you need help from OutSystems support but you don’t have an open support case yet, you can use the link **open a support case** to go to Support Portal.

1. Click **Continue** to close the window. In OutSystems 10, use the link **Cancel**.

If you are getting this report by request of OutSystems Support, **attach the file you saved to your support case**.

## Get Service Center Logs

### Runtime Logs

The [logs for the runtime of the platform](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Monitor_and_Troubleshoot/Monitor_Environments#View_Logs) are available in the **Service Center** console of each environment - application and LifeTime environments:

* Errors
* General logs
* Web requests
* Mobile requests
* Service Actions
* Integrations
* Extensions
* Timers
* Emails

To get these logs, do the following:

1. In the Service Center console of the environment you want to obtain the logs from (`https://<your_server>/ServiceCenter`), go to the **Monitoring** section.

1. Choose the type of logs you want to get (e.g., **Errors** or **General**).

1. Click **Reset** to remove any potential filter.

1. Click **Export to excel** to save the file.

![](images/get-logs-3.png)

If you are getting these logs by request of OutSystems Support, fetch all the files you saved from the local download folder and **attach them to your support case**.

### Mobile App Generation Logs

OutSystems logs the generation steps of a mobile app package, including the stack trace with additional details in case of error.

To get this mobile app package generation log, do the following:

1. If you are in Service Studio, go to the details page of the mobile app and click **Application Management...** to open the mobile app's page in Service Center console. The page opens in a separate browser.

    ![](images/get-logs-16.png?width=600)

    Otherwise, open the Service Center console of the environment (`https://<your_server>/ServiceCenter`), go to **Factory** » **Applications**, and click the mobile app name to go to the app details page.

1. Go to the **Native Platforms** tab. You will see the information about the latest mobile app package generation for each mobile platform.

    ![](images/get-logs-17.png?width=800)

1. Click the Log File icon to save the file.

If you are getting this log by request of OutSystems Support, fetch the file you saved from the local download folder and **attach it to your support case**.

## Get LifeTime Reports

From the LifeTime console, you can obtain the following reports:

* LifeTime report
* Staging report
* User permissions report

You need [Manage Infrastructure and Users](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_IT_Teams/About_Permission_Levels) permission to get these reports. If you don’t have this permission, contact your infrastructure manager.

### LifeTime Report

#### Get LifeTime Report in OutSystems 11

In OutSystems 11, do the following to get the LifeTime report:

1. Access the page `https://<LifeTime_server>/lifetime/troubleshoot.aspx`.

1. Click the link **Download Infrastructure report** to save the file.

    ![](images/get-logs-4.png?width=900)

If you are getting this report by request of OutSystems Support, fetch the file you saved from the local download folder and **attach it to your support case**.

#### Get LifeTime Report in OutSystems 10

In OutSystems 10, do the following to get the LifeTime report:

1. Go to the LifeTime console, `https://<LifeTime_server>/lifetime`.

1. Click the **Send us your feedback** icon at the upper right corner.

    ![](images/get-logs-5.png?width=900)

1. Click the **here** link to save the file.

    ![](images/get-logs-6.png?width=600)

If you are getting this report by request of OutSystems Support, fetch the file you saved from the local download folder and **attach it to your support case**.

### Staging Report

#### Get the Staging Report in OutSystems 11

In OutSystems 11, do the following to get the staging report:

1. Access the page `https://<LifeTime_server>/lifetime/troubleshoot.aspx` to see the **Deployment/Staging** list.

1. In the Stagings list, identify the staging you need to troubleshoot. You can filter by the staging date or environments.

1. In the row of the identified staging, click the link **Download staging report** to save the file.

    ![](images/get-logs-7.png?width=900)

If you are getting this report by request of OutSystems Support, fetch the file you saved from the local download folder and **attach it to your support case**.

#### Get the Staging Report in OutSystems 10

In OutSystems 10, do the following to get the staging report:

1. Go to the LifeTime console, `https://<LifeTime_server>/lifetime`.

1. In the **Applications** page, click the name of the target environment and choose **View Change Log** from the drop-down menu.

    ![](images/get-logs-8.png?width=400)

1. Take note of the deployment plan number for the deployment you want to troubleshoot.

    ![](images/get-logs-9.png?width=800)

1. Using that deployment plan number, access the following page:
 `https://<LifeTime_server>/lifetime/DebugStaging.aspx?StagingId=<deployment plan number>`.

     For the Java stack, use: `https://<LifeTime_server>/lifetime/DebugStaging.jsf?StagingId=<deployment plan number>`.

1. Click **download the staging report** to save the file.

If you are getting this report by request of OutSystems Support, fetch the file you saved from the local download folder and **attach it to your support case**.

### User Permissions Report

#### Get the User Permissions Report in OutSystems 11

In OutSystems 11, do the following to get the user permissions report:

1. Access the page `https://<LifeTime_server>/lifetime/troubleshoot.aspx`.

1. Click the link **Download the user permissions report** to save the file.

    ![](images/get-logs-10.png?width=900)

If you are getting this report by request of OutSystems Support, fetch the file you saved from the local download folder and **attach it to your support case**.

#### Get the User Permissions Report in OutSystems 10

In OutSystems 10, do the following to get the User permissions report:

1. Access the page `https://<LifeTime_server>/lifetime/DebugPermissions.aspx`.

     For the Java stack, use `https://<LifeTime_server>/lifetime/DebugPermissions.jsf`.

1. Click the link **download the user permissions report** to save the file.

    ![](images/get-logs-11.png?width=800)


If you are getting this report by request of OutSystems Support, fetch the file you saved from the local download folder and **attach it to your support case**.

## Get BPTUtils Troubleshooting Report

[BPT Utils](https://www.outsystems.com/forge/component-overview/1313/bpt-utils) is a Forge component that provides information about BPT Processes, including a troubleshooting report.

If you haven’t done it yet, you must install BPT Utils component in your LifeTime environment (you need “Full Control” permissions in the environment):

1. Download [BPT Utils](https://www.outsystems.com/forge/component-versions/1313) from OutSystems Forge. You will get an OutSystems application file (.oap). There is one version available for OutSystems 9.1, 10 and 11. Make sure to download the version corresponding to your LifeTime environment.

1. Go to the Service Center console of your LifeTime environment (`https://<LifeTime_server>/ServiceCenter`).

1. Go to **Factory** » **Applications**.

1. Click the **Publish an Application** link.

1. Click **Choose File** and select the .oap file you downloaded from Forge.

1. Click **1-Click Publish**.

BPT Utils is now installed in your LifeTime environment.

To obtain the BPTUtils troubleshooting report, do the following:

1. In the BPT Utils application (`https://<LifeTime_server>/BPTUtils/`), go to **Troubleshooting Processes**.

1. Click **Download Troubleshooting Report** to save the file.

    ![](images/get-logs-12.png?width=800)

If you are getting this report by request of OutSystems Support, fetch the file you saved from the local download folder and **attach it to your support case**.

## .Net Stack Specific Logs

### Windows Event Logs

To obtain the Windows event logs for a specific environment, do the following:

1. Connect to the server using Remote Desktop.

1. Launch the Windows Event Viewer application.

1. Expand the **Windows Logs** folder.

1. Select the logs category, such as **Application**, **Security**, or **System**.

1. Click **Save All Events As…** on the right panel to save the file.

    ![](images/get-logs-13.png?width=700)

If you are getting these logs by request of OutSystems Support, fetch the file you saved from the local download folder and **attach it to your support case**.

### IIS Manager Logs

To obtain the IIS Manager logs for a specific environment, do the following:

1. Connect to the server using Remote Desktop.

1. Launch the Internet Information Services (IIS) Manager application.

1. On the tree to the left, select your website.

1. Double-click the Logging feature.

    ![](images/get-logs-14.png?width=700)

1. Check the Directory where the log files are stored.

    ![](images/get-logs-15.png?width=600)

1. Use the File Explorer to navigate to the logs directory.
1. Zip all the directory content to attach to your support case.

If you are getting these logs by request of OutSystems Support, zip all the content of the logs directory and **attach the zip file to your support case**.

## Java Stack Specific Logs

### JBoss Logs

To obtain the JBoss logs for a specific environment, do the following:

1. Connect to the server.

1. Find the log files at:
     * JBoss 5: /opt/jboss-5.1.0.GA/server/outsystems/log
     * JBoss 7: /opt/jboss-as-7.1.1.Final/standalone/log

If you are getting these logs by request of OutSystems Support, zip all the files and **attach the zip file to your support case**.

### WildFly Logs

To obtain the WildFly logs for a specific environment, do the following:

1. Connect to the server.

1. Find the log files at:
     * WildFly 8.2: /opt/wildfly-8.2.0.Final/<wbr/>standalone/log

If you are getting these logs by request of OutSystems Support, zip all the files and **attach the zip file to your support case**.

### WebLogic Logs

To obtain the WebLogic logs for a specific environment, do the following:

1. Connect to the server.

1. Find the log files at:
     * Admin Server logs: /opt/Oracle/Middleware/user_projects/domains/outsystems_domain/servers/AdminServer/logs
     * Managed Server logs: /opt/Oracle/Middleware/user_projects/domains/outsystems_domain/servers/`<ManagedServerName>`/logs

If you are getting these logs by request of OutSystems Support, zip all the files and **attach the zip file to your support case**.
