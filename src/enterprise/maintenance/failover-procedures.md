---
summary: Describes the procedure to activate a passive front-end and move the Deployment Controller role to a different server. It can be used to recover from a server failure by activating standby servers.
locale: en-us
guid: a981ba0b-3a4d-4a75-b410-b38be75bea82
---

# OutSystems Platform Server failover procedures

This guide describes two procedures to execute during failover scenarios:

* Activate a passive front-end in installations with active and passive servers;
* Move Controller and Front-end roles to a different server.

## Activate a passive front-end in active/passive installations

An active/passive OutSystems installation is an installation where two or more front-ends grouped in:

* An active group (the front-ends which are executing requests, timers and asynchronous logic) and,
* a passive group (the front-ends in standby should failover be required).

The following table presents the steps required switch the front-ends from the passive to the active group. 

| Step | Description | Server |
|------|-------------|--------|
| 1    | **Stop and disable OutSystems Scheduler Service**: <ul><li>In .NET stack: <ol><li>Go to **Start** > **Services**.</li> Right click on the **OutSystems Scheduler Service** and chose **Stop**. <li>Right click it again and chose **Properties**</li><li>In the **Startup type** dropdown, chose **Disabled**. Click **OK** at the bottom.</li></ol></li></ul><ul><li>In Java stack: <ol><li>Use the command `service outsystems stop SCHEDULER` to stop the service.</li><li> Disable the service with the command `./serviceconfigurator.sh -interactive`</li></ol></li></ul> | OutSystems active Server(s) that should be deactivated |
| 2    | **Start service OutSystems Scheduler Service and set as automatic**: <ul><li>In .NET stack:<ol><li>Go to **Start** > **Services**.</li> Right click on the **OutSystems Scheduler Service** and chose **Start**. <li>Right click it again and chose **Properties**</li><li>In the **Startup type** dropdown, chose **Automatic**. Click **OK** at the bottom.</li></ol></li></ul><ul><li> In Java stack:<ol><li> Use the command `./serviceconfigurator.sh -interactive` to activate Scheduler</li><li>Start Scheduller with the command `service outsystems start SCHEDULER`</li></ol></li></ul> | OutSystems inactive Server(s) that should be activated |
| 3    | **Start service OutSystems Deployment Service and set it as automatic**: <ul><li>In .NET stack:<ol><li>Go to **Start** > **Services**.</li> Right click on the **OutSystems Deployment Service** and chose **Start**. <li>Right click it again and chose **Properties**</li><li>In the **Startup type** dropdown, chose **Automatic**. Click **OK** at the bottom.</li></ol></li><li>In Java stack: <ol><li>Use the command `./serviceconfigurator.sh -interactive` to activate Deployment (if needed) </li><li>Enter the command `service outsystems start DEPLOYER`</li></ol></li></ul> | Every OutSystems Server |

## Move controller and front-end roles to a different server

If the server with the Deployment Controller role fails, publishing becomes unavailable. Applications continue to run but cache invalidation mechanisms won't be operational. 

<div class="info" markdown="1">

If your application is highly dependent on cache invalidation, to ensure full functionality, it's extremely important to immediately recover a Controller after a failure to regain full functionality of the Platform Server.
</div>

The following table presents the required steps to recover the Controller by moving it's role to another front-end in the same environment farm.
                                
| Step | Description | Server |
|------|-------------|--------|
| 1    | **Stop and disable Deployment Controller service**:<ul><li>In .NET stack: <ol><li>Go to **Start** > **Services**.</li> Right click on the **OutSystems Deployment Controller Service** and chose **Stop**. <li>Right click it again and chose **Properties**</li><li>In the **Startup type** dropdown, chose **Disabled**. Click **OK** at the bottom.</li></ol></li><li>In Java stack:<ol><li>Use the command `service outsystems stop CONTROLLER`</li><li>Disable the service with the command `./serviceconfigurator.sh -interactive`</li></ol></li></ul> | Old OutSystems Deployment Controller server |
| 2    | **Start service Deployment Controller service and set as automatic**: <ul><li>In .NET stack:<ol><li>Go to **Start** > **Services**.</li> Right click on the **OutSystems Deployment Controller Service** and chose **Start**. <li>Right click it again and chose **Properties**</li><li>In the **Startup type** dropdown, chose **Automatic**. Click **OK** at the bottom.</li></ol></li><li>In Java stack:<ol><li>Use the command `./serviceconfigurator.sh -interactive` to activate Deployment Controller service.</li><li>Stat the service with `service outsystems start CONTROLLER`</li></ol></li></ul> | New OutSystems Deployment Controller server |
| 3    | **Update location of Controller in OutSystems configurations**.<br/>  The value written for this setting must be equal in all front-ends  of the environment. <ul><li>In .NET stack:<ol><li>Run Configuration Tool from the Start menu.</li><li>In the **Controller** tab on the **Deployment Controller Server** field, enter the IP address of the new Deployment Controller server (the one used in step 2).</li><li> Click Apply and Exit.</li><li>Accept the restart of all OutSystems services.</li><li>Answer **No** when a pop-up asks you to run the Service Center installation.</li></ol></li><li>In Java stack:<ol><li>Run the Configuration Tool with the command `./configurationtool.sh`</li><li>Set the **Deployment Controller Server** option with the IP address of the new Deployment Controller (the server used in step 2).</li><li>Continue running the options and accept the restart of all OutSystems services. When prompted, **don't** run Service Center installation.</li></ol></li></ul> | All front-ends of this environment. Starting with the Controller |
| 4    | **Service Center Installation**<ul><li>In .NET stack:<ol><li>Run the Configuration Tool from the Start menu.</li><li>Click **Apply and Exit**.</li><li>Answer **Yes** when a pop-up asks you to run Service Center installation.</li></ol></li><li>In Java stack:<ol><li>Run the Configuration Tool with the command `./configurationtool.sh`</li><li>Keep the values for all options.</li><li>When prompted, run Service Center installation.</li></ol></li></ul> | Deployment Controller server |
| 5    | **Obtain a new license (optional)**.<br/>After moving the Controller role to another machine your license may become invalid. If you don't have the license file for the new Controller you need to request one. Check the following instructions:<ul><li>[Free up an existing environment in licensing](../licensing/manage/free-up-environment.md)</li><li>[Get a license file for an environment](../licensing/manage/get-license-for-env.md)</li></ul>In case you need assistance [contact OutSystems Support](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/01_Contact_OutSystems_technical_support#Contact_Channels). | [Licensing Portal](https://www.outsystems.com/licensing) |
| 6    | **Install the new OutSystems license**.<br/>Check the instructions at [How to install a license file](../licensing/manage/howto-install-license.md) | Service Center |
| 7    | **Republish all applications**.<ol><li>Access Service Center.</li><li>Login with a Service Center administration account.</li><li>Access **Factory** > **Solutions**.</li><li>Locate an all-content Solution, ensure it carries all the modules of the environment and publish the current running version. If none exists, skip to the next step.</li><li>Create a new Solution and add all the eSpaces and Extensions to it. Publish the current running version. (execute this step only if you skipped step 4).</li></ol> | Service Center |

## More information

Check the [OutSystems Platform installation guide](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems#Install_OutSystems_Platform_Server) to learn more about the steps to follow for your specific stack.

