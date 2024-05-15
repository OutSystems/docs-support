---
summary: Learn failover procedures for activating passive front-ends and moving roles in OutSystems 11 (O11) installations.
locale: en-us
guid: a981ba0b-3a4d-4a75-b410-b38be75bea82
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# OutSystems Platform Server failover procedures

This guide describes three procedures to execute during failover scenarios:

* Activate a passive front-end in installations with active and passive servers;
* Move Controller and Front-end roles to a different server;
* Move Controller roles and RabbitMQ to a different server.

## Activate a passive front-end in active/passive installations

An active/passive OutSystems installation is an installation where two or more front-ends grouped in:

* An active group (the front-ends which are executing requests, timers and asynchronous logic) and,
* a passive group (the front-ends in standby should failover be required).

The following procedure presents the steps required switch the front-ends from the passive to the active group.

1. On the OutSystems active Server(s) that should be deactivated, **stop and disable OutSystems Scheduler Service.**
    * In .NET stack
        1. Right-click on the **OutSystems Scheduler Service** and chose **Stop**.
        1. Right-click it again and chose **Properties**.
        1. to **Start** > **Services**.
        1. In the **Startup type** dropdown, choose **Disabled**. Click **OK** at the bottom.
    * In Java stack:
        1. Use the command `service outsystems stop SCHEDULER` to stop the service.
        1. Disable the service with the command `./serviceconfigurator.sh -interactive
        1. Use the command `service outsystems stop SCHEDULER` to stop the service.
        1. Disable the service with the command `./serviceconfigurator.sh -interactive`
1. On the OutSystems inactive Server(s) that should be activated, **start service OutSystems Scheduler Service and set as automatic:**
    * In .NET stack:
        1. Go to **Start** > **Services**.
        1. Right-click on the **OutSystems Scheduler Service** and chose **Start**.
        1. Right-click it again and chose **Properties**
        1. In the **Startup type** dropdown, choose **Automatic**. Click **OK** at the bottom.
1. On every OutSystems server, 	**start service OutSystems Deployment Service and set it as automatic.**
    * In .NET stack:
        1. Go to **Start** > **Services**.
        1. Right-click on the **OutSystems Deployment Service** and chose **Start**.
        1. Right-click it again and choose **Properties**
        1. In the **Startup type** dropdown, chose **Automatic**. Click **OK** at the bottom.
    * In Java stack:
        1. Use the command `./serviceconfigurator.sh -interactive` to activate Deployment (if needed).
        1. Enter the command `service outsystems start DEPLOYER`.

## Move controller and front-end roles to a different server

If the server with the Deployment Controller role fails, publishing becomes unavailable. Applications continue to run but cache invalidation mechanisms won't be operational.

<div class="info" markdown="1">

If your application is highly dependent on cache invalidation, to ensure full functionality, it's extremely important to immediately recover a Controller after a failure to regain full functionality of the Platform Server.
</div>

The following procedure presents the required steps to recover the Controller by moving it's role to another front-end in the same environment farm.

1. On old OutSystems Deployment Controller servers, **stop and disable Deployment Controller service.**
    * In .NET stack:
        1. Go to **Start** > **Services**.
        1. Right-click on the **OutSystems Deployment Controller Service** and choose **Stop**.
        1. Right-click it again and choose **Properties**
        1. In the **Startup type** dropdown, choose **Disabled**. Click **OK** at the bottom.
    * In Java stack:
        1. Use the command `service outsystems stop CONTROLLER`.
        1. Disable the service with the command `./serviceconfigurator.sh -interactiv`.
1. On New OutSystems Deployment Controller servers, **start service Deployment Controller service and set as automatic**.
    * In .NET stack:
        1. Go to **Start** > **Services**.
        1. Right-click on the **OutSystems Deployment Controller Service** and choose **Start**.
        1. Right-click it again and choose **Properties**.
        1. In the **Startup type** dropdown, choose **Automatic**. Click **OK** at the bottom.
    * In Java stack:
        1. Use the command `./serviceconfigurator.sh -interactive` to activate Deployment Controller service.
        1. Start the service with `service outsystems start CONTROLLER`.
1. On all front-ends of this environment, starting with the Controller, **update location of Controller in OutSystems configurations**. The value written for this setting must be equal in all front-ends of the environment.
    * In .NET stack:
        1. Run Configuration Tool from the Start menu.
        1. In the **Controller** tab on the **Deployment Controller Server** field, enter the IP address of the new Deployment Controller server (the one used in step 2).
        1. Click Apply and Exit.
        1. Accept the restart of all OutSystems services.
        1. Answer **No** when a pop-up asks you to run the Service Center installation.
    * In Java stack:
        1. Run the Configuration Tool with the command `./configurationtool.sh`.
        1. Set the **Deployment Controller Server** option with the IP address of the new Deployment Controller (the server used in step 2).
        1. Continue running the options and accept the restart of all OutSystems services. When prompted, **don't** run Service Center installation.
1. On the deployment Controller server, run **Service Center Installation**.
    * In .NET stack:
        1. Run the Configuration Tool from the Start menu.
        1. Click **Apply and Exit**.
        1. Answer **Yes** when a pop-up asks you to run Service Center installation.
    * In Java stack:
        1. Run the Configuration Tool with the command `./configurationtool.sh`
        1. Keep the values for all options.
        1. When prompted, run Service Center installation.
1. In the licensing portal, **obtain a new license (optional)**. After moving the Controller role to another machine your license may become invalid. If you don't have the license file for the new Controller you need to request one. Check the following instructions:
    * [Free up an existing environment in licensing](../licensing/manage/free-up-environment.md)
    * [Get a license file for an environment](../licensing/manage/get-license-for-env.md)
1. In Service Center, **install the new OutSystems license**. Check the instructions at [How to install a license file](../licensing/manage/howto-install-license.md).
1. In Service Center, **republish all applications**.
    1. Access Service Center.
    1. Login with a Service Center administration account.
    1. Access **Factory** > **Solutions**.
    1. Locate an all-content Solution, ensure it carries all the modules of the environment and publish the current running version. If none exists, skip to the next step.
    1. Create a new Solution and add all the eSpaces and Extensions to it. Publish the current running version. (execute this step only if you skipped step 4).

In case you need assistance [contact OutSystems Support](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/01_Contact_OutSystems_technical_support#Contact_Channels).

## Move controller roles and RabbitMQ to a different server

Both the controller roles and RabbitMQ need to be executed at the same times.

<div class="info" markdown="1">

Applies to OutSystems 11 only.

</div>

The following procedure presents the required steps to move controller roles and RabbitMQ to a different server.

1. On the old OutSystems Deployment Controller server, **Stop and disable Deployment Controller service**. 
    1. Go to **Start** > **Services**.
    1. Right-click on the **OutSystems Deployment Controller Service** and choose **Stop**. Right-click it again and choose **Properties**
    1. In the **Startup type** dropdown, choose **Disabled**. Click **OK** at the bottom.
1. **Stop and disable RabbitMQ service**.
    1. Go to **Start** > **Services**.
    1. Right-click on the **RabbitMQ Service** and choose **Stop**. Right-click it again and choose **Properties**
    1. In the **Startup type** dropdown, choose **Disabled**. Click **OK** at the bottom.
1. On the new OutSystems Deployment Controller server, **Set OutSystems Deployment Controller Startup Type as Automatic**. 
        1. Go to **Start** > **Services**.
        1. Right-click on the **OutSystems Deployment Controller Service** and choose **Properties**
        1. In the **Startup type** dropdown, choose **Automatic**. Click **OK** at the bottom.
1. On all front-ends of this environment, starting with the new Controller, **Update location of Controller and RabbitMQ in OutSystems configurations**. The value written for this setting must be equal in all front-ends of the environment.
    1. Run Configuration Tool from the Start menu.
    1. In the **Controller** tab, enter the IP address of the new Deployment Controller server
    1. In the **Cache** tab, enter the address of the new New OutSystems Deployment Controller server and, if needed, reconfigure the Port, Virtual Host, and Credentials values.
    1. Click **Create/Upgrade Service**.
    1. Click **Test Connection** to validate if the service creation was successful.
    1. Click **Apply** and **Exit**.
    1. Accept the restart of all OutSystems services.
    1. Answer **No/Cancel** when a pop-up asks you to run the Service Center installation and Prepare Modules.
    1. Close the Configuration Tool and **Save** the configuration
    1. Run **install.bat** as Administrator from OutSystems Platform Server installation directory
    1. Repeat steps 1-7 from this list in remaining Front-Ends
1. In the licensing portal, **obtain a new license (optional)**. After moving the Controller role to another machine your license may become invalid. If you don't have the license file for the new Controller you need to request one. Check the following instructions:
    * [Free up an existing environment in licensing](../licensing/manage/free-up-environment.md)
    * [Get a license file for an environment](../licensing/manage/get-license-for-env.md)
1. In Service Center, **install the new OutSystems license**. Check the instructions at [How to install a license file](../licensing/manage/howto-install-license.md).
1. In Service Center, **republish all applications**.
    1. Access Service Center.
    1. Login with a Service Center administration account.
    1. Access **Factory** > **Solutions**.
    1. Locate an all-content Solution, ensure it carries all the modules of the environment and publish the current running version. If none exists, skip to the next step.
    1. Create a new Solution and add all the eSpaces and Extensions to it. Publish the current running version. (execute this step only if you skipped step 4).

In case you need assistance [contact OutSystems Support](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/01_Contact_OutSystems_technical_support#Contact_Channels).

## More information

Check the [OutSystems Platform installation guide](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems#Install_OutSystems_Platform_Server) to learn more about the steps to follow for your specific stack.
