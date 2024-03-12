---
summary: Learn how to troubleshoot LifeTime deployment issues.
tags:
locale: en-us
guid: c7ebcb0a-6852-4222-9286-9fa6bc5d0675
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=620:48
---
# Unable to deploy applications using LifeTime

There are some situations that might prevent you from using LifeTime to deploy your applications from a **source** to a **target** environment (for example, from Development to QA).

Some examples:

* LifeTime is incorrectly considering the dependencies are incompatible.
* LifeTime isn't showing the version last published in the source environment.
* The deployment gets stuck in one of the steps.
* The synchronization of the source or target environment [is stuck](lifetime-sync-stuck.md).

## Troubleshooting

When you aren't able to use LifeTime to deploy your applications, follow the validations below to troubleshoot a potential issue.

### Check the network connectivity between environments (on-premises only)

If you have on-premises environments, make sure there is bidirectional communication between LifeTime and both source and target environments:

1. [Test the connectivity](../../infrastructure-management/test-env-connectivity.md) from **LifeTime** to the **source environment**.

1. [Test the connectivity](../../infrastructure-management/test-env-connectivity.md) from the **source environment** to **LifeTime**.

1. [Test the connectivity](../../infrastructure-management/test-env-connectivity.md) from **LifeTime** to the **target environment**.

1. [Test the connectivity](../../infrastructure-management/test-env-connectivity.md) from the **target environment** to **LifeTime**.

### Check the antivirus configuration in LifeTime server (on-premises only)

You can confirm if antivirus or other third party software is interfering with the deployment. When that's the case, the deployment fails, check the details at [Publish error: the process cannot access the file](https://www.outsystems.com/tk/redirect?g=1305808c-05bc-4f19-939b-09877f5681c1).

### Check the status of OutSystems services

Check the status of the OutSystems services in both **source** and **target** environments to guarantee they're working correctly:

1. Go to the Service Center console of the **source** environment (`https://<source_server>/ServiceCenter`).

1. Go to **Monitoring** » **Environment Health**. A green checkmark means the service is working correctly.

1. Do the same for the **target** environment.

![Screenshot of the Environment Health section in the OutSystems Service Center showing green checkmarks indicating all services are operational.](images/lifetime-deploy-unable-1.png "Environment Health Status in Service Center")

### Check the status of LifeTime Processes

Environments synchronization in LifeTime is based on [OutSystems Business Process Technology](https://www.outsystems.com/tk/redirect?g=ce023611-1cbc-4c61-a778-2a66167bc7ba).

Check the status of the Processes for potential issues:

1. Go to the Service Center console of your LifeTime environment (`https://<LifeTime_server>/ServiceCenter`).

1. Go to **Monitoring** » **Processes**. You should have **no Suspended Instances** and **no Active Instances with Errors**. If you get any of these, [open a support case](https://www.outsystems.com/SupportPortal/CaseOpen/) to get help from OutSystems Support.

![Screenshot of the Process Monitoring page in the OutSystems Service Center displaying a list of processes with their status, showing no suspended instances or active instances with errors.](images/lifetime-process-monitor-sc.png "Process Monitoring in Service Center")

## Still having problems?

If the above validations didn't help you to solve the issue and you need further assistance, [open a support case](https://www.outsystems.com/SupportPortal/CaseOpen/) to get help from OutSystems Support.

If you have a critical need to deploy an application to an environment, you can try to [deploy the application through Service Center](../deploy-apps-sc.md) as a workaround.
