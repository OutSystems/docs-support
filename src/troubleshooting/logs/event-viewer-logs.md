---
summary: OutSystems 11 (O11) provides a guide on retrieving Windows event logs for specific environments using Remote Desktop and Windows Event Viewer.
tags: windows event viewer, server troubleshooting, logging, application performance monitoring
locale: en-us
guid: c281aa1d-be12-415d-82c1-c9e186039f7f
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=3327:522
audience:
  - platform administrators
  - full stack developers
  - tech leads
  - infrastructure managers
outsystems-tools:
  - none
coverage-type:
  - unblock
---

# Windows Event Viewer logs

To get the Windows event logs for a specific environment, follow these steps:

1. Connect to the server using Remote Desktop.

1. Launch the Windows Event Viewer application.

1. Expand the **Windows Logs** folder.

1. Select the logs category, such as **Application**, **Security**, or **System**.

1. Click **Save All Events As…** on the right panel to save the file.

    ![Screenshot of Windows Event Viewer with an arrow pointing to 'Application' under Windows Logs and the 'Save All Events As...' option highlighted in the Actions panel.](images/get-logs-13.png "Windows Event Viewer Save Option")

