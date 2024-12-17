---
summary: Explore how to obtain various reports in OutSystems 11 (O11) through the LifeTime troubleshooting interface.
tags: lifetime, troubleshooting, infrastructure management, support case assistance
locale: en-us
guid: 27d0fb71-1ef7-4574-a8ca-bd1126b29976
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=3327:499
audience:
  - platform administrators
  - infrastructure managers
  - full stack developers
outsystems-tools:
  - lifetime
coverage-type:
  - unblock
---

# LifeTime reports

You need [Manage Infrastructure and Users](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_IT_Teams/About_Permission_Levels) permission to get these reports. If you don’t have this permission, contact your infrastructure manager.

## LifeTime Report { #lifetime-report }
To get the Lifetime report, follow these steps:

### Get LifeTime report in OutSystems 11

1. Access the page `https://<LifeTime_server>/lifetime/troubleshoot.aspx`

1. Click the link **Download Infrastructure report** to save the file.

    ![Screenshot highlighting the 'Download Infrastructure report' link in the OutSystems LifeTime troubleshooting page.](images/get-logs-4.png "Download Infrastructure Report Link")

If you are getting this report by request of OutSystems Support, fetch the file you saved from the local download folder and **attach it to your support case**.

### Get LifeTime report in OutSystems 10

1. Go to the LifeTime console, `https://<LifeTime_server>/lifetime`

1. Click the **Send us your feedback** icon at the upper right corner.

    ![Screenshot showing the 'Send us your feedback' icon in the upper right corner of the OutSystems LifeTime console.](images/get-logs-5.png "Send Us Your Feedback Icon")

1. Click the **here** link to save the file.

    ![Screenshot of the feedback popup with a highlighted link to 'Click here to download the report' in OutSystems LifeTime.](images/get-logs-6.png "Feedback Report Download Link")

If you are getting this report by request of OutSystems Support, fetch the file you saved from the local download folder and **attach it to your support case**.

## Staging Report
To get the staging report, follow these steps:

### Get the staging report in OutSystems 11

1. Access the page `https://<LifeTime_server>/lifetime/troubleshoot.aspx` to see the **Deployment/Staging** list.

1. In the Stagings list, identify the staging you need to troubleshoot. You can filter by the staging date or environments.

1. In the row of the identified staging, click the link **Download staging report** to save the file.

    ![Screenshot highlighting the 'Download staging report' link in the Deployment/Staging section of the OutSystems LifeTime troubleshooting page.](images/get-logs-7.png "Download Staging Report Link")

If you are getting this report by request of OutSystems Support, fetch the file you saved from the local download folder and **attach it to your support case**.

### Get the staging report in OutSystems 10

1. Go to the LifeTime console, `https://<LifeTime_server>/lifetime`

1. In the **Applications** page, click the name of the target environment and choose **View Change Log** from the drop-down menu.

    ![Screenshot showing the 'View Change Log' option in a dropdown menu for an environment in the OutSystems LifeTime console.](images/get-logs-8.png "View Change Log Option")

1. Take note of the deployment plan number for the deployment you want to troubleshoot.

    ![Screenshot of the Change Log for an environment in OutSystems LifeTime, with the deployment plan number highlighted.](images/get-logs-9.png "Change Log with Deployment Plan Number")

1. Using that deployment plan number, access the following page:
 `https://<LifeTime_server>/lifetime/DebugStaging.aspx?StagingId=<deployment plan number>`

     For the Java stack, use: `https://<LifeTime_server>/lifetime/DebugStaging.jsf?StagingId=<deployment plan number>`.

1. Click **download the staging report** to save the file.

If you are getting this report by request of OutSystems Support, fetch the file you saved from the local download folder and **attach it to your support case**.

## User Permissions Report
To get the user permissions report, follow these steps.

### Get the user permissions report in OutSystems 11

1. Access the page `https://<LifeTime_server>/lifetime/troubleshoot.aspx`

1. Click the link **Download the user permissions report** to save the file.

    ![Screenshot highlighting the 'Download the user permissions report' link in the OutSystems LifeTime troubleshooting page.](images/get-logs-10.png "Download User Permissions Report Link")

If you are getting this report by request of OutSystems Support, fetch the file you saved from the local download folder and **attach it to your support case**.

### Get the user permissions report in OutSystems 10

1. Access the page `https://<LifeTime_server>/lifetime/DebugPermissions.aspx`

     For the Java stack, use `https://<LifeTime_server>/lifetime/DebugPermissions.jsf`

1. Click the link **download the user permissions report** to save the file.

    ![Screenshot showing the 'download the user permissions report' link in the OutSystems LifeTime DebugPermissions page.](images/get-logs-11.png "User Permissions Report Download Link")
