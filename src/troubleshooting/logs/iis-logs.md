---
summary: This guide explains how to retrieve IIS Manager logs for OutSystems 11 (O11) environments.
tags:
locale: en-us
guid: 71ebf09d-b6ac-4453-8c92-e4e86204ed8a
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=3327:544
---
# IIS Manager logs

To get the IIS Manager logs for a specific environment, follow these steps:

1. Connect to the server using Remote Desktop.

1. Launch the Internet Information Services (IIS) Manager application.

1. On the tree to the left, select your website.

1. Double-click **Logging**.

    ![Screenshot of the Internet Information Services (IIS) Manager showing the Features View with various options like Authentication, Directory Browsing, and Logging highlighted.](images/get-logs-14.png "IIS Manager Features View")

1. Check the Directory where the log files are stored.

    ![Close-up of the Logging settings in IIS Manager with the Directory field highlighted, showing the path to the log files.](images/get-logs-15.png "IIS Manager Logging Settings")

1. Use the File Explorer to navigate to the logs directory.
1. Zip all the directory content to attach to your support case.

