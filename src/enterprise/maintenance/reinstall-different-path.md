---
summary: This article guides through the necessary steps to move the OutSystems Platform installation to a different path
locale: en-us
guid: 6b46a4ee-85c8-482d-96dd-e555863e7935
---

# Re-Install the OutSystems Platform on a different path

Follow the steps in this article when moving the Platform Server installation **from one path to another**, for example from "C:\Program Files\OutSystems\Platform Server" to "D:\Program Files\OutSystems\Platform Server". 

<div class="info" markdown="1">

These steps are not applicable when moving the Platform Server installation to a different server.

</div>

This operation applies only to **on-premises installations**.

## In the deployment controller server

In the server with the Deployment Controller role, do the following:

1. Stop IIS: open IIS Manager and click **Stop** on the right pane under **Manage Server > Actions**.

1. Stop all OutSystems Services. You can do this in the **Services** application in Windows to all services that start with "OutSystems".

1. Backup the `private.key` and `server.hsconf` files present in the installation folder (by default, "C:\Program files\OutSystems\Platform Server").

1. Remove RabbitMQ Service. To do this, open the installation folder, navigate to "\thirdparty\RabbitMQ Server\rabbitmq_server-%version%\sbin", and open the command prompt in this folder. Execute the following command: `rabbitmq-service.bat remove`

1. Uninstall RabbitMQ using the operating system's features to manage installed programs (for example, in Windows Server use **Control Panel > Programs and Features**).

1. Uninstall Erlang OTP using the operating system's features to manage installed programs.

1. Uninstall the current OutSystems platform using the operating system's features to manage installed programs.

1. Delete all entries in the `ossys_parameter` database table that contain the older installation folder path (depending on the platform version these entries may not exist).

1. In the .NET configuration files, delete all settings related to the previous installation folder. We can find these configuration settings in the machine.config file, in each of the following folders: "C:\Windows\Microsoft.NET\Framework64\v4.0.30319\Config" and "C:\Windows\Microsoft.NET\Framework\v4.0.30319\Config"

1. Delete all environment variables related to Erlang and RabbitMQ (such as ERLANG_HOME, OUTSYSTEMS_RABBITMQ, RABBITMQ_BASE, RABBITMQ_NODENAME). To do this, open the **Advanced System Settings** option and click **Environment variables**. Then, select the system variable and click **Delete**.

1. Re-install the OutSystems platform on the new path (for example, "D:\Program files\OutSystems\Platform Server"). To do this, you need to run the OutSystems Platform Server installation package (`PlaformServer-<version>.exe`) of the same version.

1. Restore the `private.key` file and `server.hsconf` files backed up on step 3 on the new installation path overwriting any files that may be present.

1. Start IIS: open IIS Manager and click **Start** on the right pane under **Manage Server > Actions**.

1. Open the Configuration Tool and navigate to the Cache tab. Then click on **Create/Upgrade Service**.

1. Click **Apply and Exit**.

1. A popup will be shown asking you to run the Service Center installation. Accept by clicking **Yes**.

1. Publish the System Components.

1. Re-publish all applications.

## In any additional front-end server

If your OutSystems environment has additional front-end servers, after executing the above steps on the deployment controller server, execute steps 1 through 16 on each of the front-end servers.
