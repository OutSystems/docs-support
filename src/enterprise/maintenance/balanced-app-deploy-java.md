---
summary: This article describes the steps to deploy an application into a highly loaded OutSystems farm environment in Java stack. 
tags: 
---

# Balanced Application Deployment on Highly Loaded OutSystems Farms for Java

This article describes the steps to deploy an application into a highly loaded OutSystems farm environment in Java stack. The deployment process is balanced throughout the existing front-ends, guaranteeing no downtime for the applications.

![Highly loaded farm environment](images/balanced-app-deploy-1.png?width=700)

This operation applies only to **on-premises** or **private cloud** installations.

Check [this article](balanced-app-deploy.md) to have an overview of the process.

## Prerequisites

For the execution of this procedure, the following requirements must be met:

* Have an **on-premises** or **private cloud** installation.

* Have a **network load balancing mechanism** for distributing the application traffic between the front-ends.

* The operation is performed by a user with **administrative privileges** at Service Center and operating system level (in the services management console).

* All servers must be running OutSystems Platform Server **version 4.2.4.74 or higher**.

## Deploying applications in a highly loaded farm environment  

Follow the steps below to execute a balanced application deployment.

**Step 1. Disable the OutSystems Scheduler Service in all front-ends (Updating and Loaded front-ends)**

Do the following on each front-end server:

1. ​In a command line, as user **root**, run the following command:  
    `# /opt/outsystems/platform/serviceconfigurator.sh -interactive`
1. Disable the **OutSystems Scheduler Service**: reply `Y` to the services that must be enabled; reply `N` to all services that must be disabled, including the OutSystems Scheduler Service.
1. The **OutSystems Scheduler Service** will stop automatically. Run the following command to confirm that the service is stopped:  
    `# service outsystems status SCHEDULER`

    The output must be similar to:  
    `OutSystems Scheduler Service  -  DISABLED`

<div class="info" markdown="1">
 
Don’t start the OutSystems Scheduler Service until instructed to do so.
 
</div>

**Step 2. In the Load Balancer, set the traffic to the Loaded front-ends**

1. Access your **Load Balancer** management tool.
1. Remove the application traffic from the **Updating front-ends**. The **Loaded front-ends** must be the only ones receiving traffic from end-users.

![Set traffic to loaded front-ends](images/balanced-app-deploy-4.png?width=700)

**Step 3. Disable deployment in the Loaded front-ends**

1. Access the **environment’s Service Center** (eg. `https://<dev_environment>/ServiceCenter`).
1. Log in with administrative privileges.
1. Go to **Administration » Servers**. For each **Loaded front-end**, access its details and press the **Disable** button. This action disables the deployment service, while the IIS keeps running and the applications are available to the end-users.

**Step 4. Publish your application to the Updating front-ends**

1. Access the **Service Center** console directly through one of the **Updating front-ends** (eg. `https://<front-end server>/ServiceCenter`).
1. Log in with publishing privileges.
1. Go to the **Factory** section and choose **Applications** / **Modules** / **Solutions**, depending on the file you want to publish (.oap, .oml or .osp).
1. Upload and publish your file.
1. Wait until the publishing finishes successfully.

Any updates in the database caused by the new application version are executed during this publishing. The updated code will be automatically deployed to the remaining **Updating front-ends**.

**Step 5. Test your application on the Updating front-ends**

Do the following on each **Updating front-end** server:

1. Access the application directly through the **Updating front-end** (eg. `https://<front-end server>/<Application>`).
1. Confirm the application is available and updated.

**Step 6. In the Load Balancer, set the traffic to the Updating front-ends**

1. Access your **Load Balancer** management tool.
1. Set the **Updating front-ends** to start receiving application traffic.
1. Remove the application traffic from the **Loaded front-ends**. This time, the **Updating front-ends** must be the only ones receiving traffic from end-users.

![Set traffic to updating front-ends](images/balanced-app-deploy-5.png?width=700)

**Step 7. Start the OutSystems Scheduler Service in the Updating front-ends**

Do the following on each **Updating front-end** server:

1. In a command line, as user **root**, run the following command:  
    `# /opt/outsystems/platform/serviceconfigurator.sh -interactive`
1. Enable the **OutSystems Scheduler Service**: reply `Y` to the services that must be enabled, including the OutSystems Scheduler Service; reply `N` to all services that must be disabled.
1. Run the following command to start the OutSystems Scheduler Service:  
    `# service outsystems start SCHEDULER`
1. Run the following command to confirm that the service is started:  
    `# service outsystems status SCHEDULER`

    The output must be similar to:  
    `OutSystems Scheduler Service - RUNNING`

**Step 8. Restart the OutSystems Deployment Services in the Loaded front-ends**

By restarting the OutSystems Deployment Services, you ensure all applications are immediately deployed to the **Loaded front-ends**.

Do the following on each **Loaded front-end** server:

1. In a command line, as user **root**, run the following command:  
    `# service outsystems restart DEPLOYER`

**Step 9. Check the deployment process status**

1. Access the **environment’s Service Center** (eg. `https://<dev_environment>/ServiceCenter`).
1. Log in with administrative privileges.
1. Go to **Monitoring » Environment Health**.
1. For each **Loaded front-end**, click the detail link for the **Deployment** service to check the status of its threads. Wait until the status of all threads is `Idle` or `Sleeping`. When this happens, the deployment process to the **Loaded front-ends** has finished.

**Step 10.  In the Load Balancer, reset the traffic to all front-ends**

1. Access your **Load Balancer** management tool.
1. Set the **Loaded front-ends** to start receiving application traffic again.

**Step 11. Start the OutSystems Scheduler Service in the Loaded front-ends**

Do the following on each **Loaded front-end** server:

1. In a command line, as user **root**, run the following command:  
    `# /opt/outsystems/platform/serviceconfigurator.sh -interactive`
1. Enable the **OutSystems Scheduler Service**: reply `Y` to the services that must be enabled, including the OutSystems Scheduler Service; reply `N` to all services that must be disabled.
1. Run the following command to start the **OutSystems Scheduler Service**:  
    `# service outsystems start SCHEDULER`
1. Run the following command to confirm that the service is started:  
    `# service outsystems status SCHEDULER`
    
    The output must be similar to:  
    `OutSystems Scheduler Service - RUNNING`
