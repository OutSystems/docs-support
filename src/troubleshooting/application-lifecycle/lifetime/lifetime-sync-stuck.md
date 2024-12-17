---
summary: Troubleshoot stuck environment synchronization in OutSystems 11 (O11) LifeTime by checking updates, connectivity, and process statuses.
tags: outsystems lifetime, environment synchronization, platform server, troubleshooting, connectivity issues
locale: en-us
guid: e6d30ec2-fd7a-4214-921b-12f021aab323
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=620:53
audience:
  - platform administrators
  - infrastructure managers
outsystems-tools:
  - lifetime
  - platform server
coverage-type:
  - unblock
---

# LifeTime synchronization is stuck

## Symptom

Environment synchronization in LifeTime is taking longer than expected.

![Screenshot showing the LifeTime synchronization status with a notification that data may be outdated.](images/lifetime-sync-stuck-1.png "LifeTime Synchronization Status")

## Troubleshooting

When the synchronization of an environment in LifeTime is stuck, follow the validations below to troubleshoot a potential issue.

### Verify that you are running the latest version of LifeTime and Platform Server

Keep **LifeTime** and **Platform Server** updated to take advantage of the latest improvements in synchronization procedures.

### Check the connectivity between environments (self-managed only)

If you have self-managed environments, make sure there is bidirectional communication between LifeTime and the synchronizing environment:

1. [Test the connectivity](../../infrastructure-management/test-env-connectivity.md) from **LifeTime** to the **synchronizing environment**.

1. [Test the connectivity](../../infrastructure-management/test-env-connectivity.md) from the **synchronizing environment** to **LifeTime**.

### Check the servers timezone (self-managed only)

If you have self-managed environments, make sure the database server and the application environment servers (controller and front-ends) are set with the same [Timezone](https://support.microsoft.com/en-us/help/4026213/windows-how-to-set-your-time-and-time-zone), as described in [OutSystems Timezone considerations](../../../enterprise/maintenance/timezone-considerations.md).

### Check the status of LifeTime Processes

Environments synchronization in LifeTime is based on [OutSystems Business Process Technology](https://success.outsystems.com/Documentation/11/Developing_an_Application/Use_Processes_(BPT)).

Check the status of the Processes for potential issues:

1. Go to the Service Center console of your LifeTime environment (`https://<LifeTime_environment>/ServiceCenter`).

1. Go to **Monitoring** » **Processes**. You should have **no Suspended Instances** and **no Active Instances with Errors**. If you get any of these, [open a support case](https://www.outsystems.com/SupportPortal/CaseOpen/) to get help from OutSystems Support.

![Screenshot of the OutSystems Service Center's Process Monitoring page displaying various processes and their statuses.](images/lifetime-process-monitor-sc.png "LifeTime Process Monitoring")

## Still having problems?

If the above validations didn't help you to solve the issue and you need further assistance, [open a support case](https://www.outsystems.com/SupportPortal/CaseOpen/) to get help from OutSystems Support.

If you have a critical need to deploy an application to that environment, you can try to [deploy the application through Service Center](../deploy-apps-sc.md) as a workaround.

If your infrastructure is self-managed (not required for OutSystems Cloud), make sure to attach the following information to your support case:

* [**Error**, **General**, and **Integrations** log files](../../logs/service-center-logs.md) from the Service Center console of the **synchronizing environment**

* [**Error**, **General**, and **Integrations** log files](../../logs/service-center-logs.md) from the Service Center console of your **LifeTime environment**

* [LifeTime Report](../../logs/lifetime-logs.md#lifetime-report)

* [BPTUtils Troubleshooting Report](../../logs/bpt-report.md)
