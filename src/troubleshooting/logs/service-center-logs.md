---
summary: Explore how to retrieve and export Service Center logs in OutSystems 11 (O11) using the monitoring section.
tags: log management, troubleshooting, outsystems service center, exporting data, system monitoring
locale: en-us
guid: 85487f8d-7eb3-4c11-98b5-03706c741c57
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=3327:509
audience:
  - platform administrators
  - backend developers
  - full stack developers
outsystems-tools:
  - service center
coverage-type:
  - unblock
---

# Service Center logs

To get Service Center logs, follow these steps:

1. In the Service Center console of the environment you want to obtain the logs from (`https://<your_server>/ServiceCenter`), go to the **Monitoring** section.

1. Choose the type of logs you want to get (for example, **Errors** or **General**).

1. Click **Reset** to remove any potential filter.

1. Click **Export to excel** to save the file.

![Screenshot of Service Center showing steps to export Error Logs, with Monitoring, Errors, Reset, and Export to excel highlighted.](images/get-logs-sc.png "Service Center Error Log Export")

<div class="info" markdown="1">

You can only view the last two weeks of logs in Service Center. Older logs are available directly in the database within the retention period. For detailed information, refer to [The rotation of logs](https://success.outsystems.com/documentation/11/monitoring_and_troubleshooting_apps/logging_database_and_architecture/the_log_tables_and_views/#the-rotation-of-the-logs).

</div>
