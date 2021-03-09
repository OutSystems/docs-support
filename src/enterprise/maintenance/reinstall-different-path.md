---
summary: This article guides through the necessary steps to move the OutSystems Platform installation to a different path
---

# Re-Install the OutSystems Platform on a different path

Follow the steps in this article when moving the Platform Server installation from one path to another, for example from C:\Program Files\OutSystems\Platform Server to D:\Program Files\OutSystems\Platform Server. 

<div class="info" markdown="1">

These steps are not applicable when moving the Platform Server installation to a different server.

</div>

This operation applies only to **on-premises installations**.

## In the deployment controller server

In the server with the Deployment Controller role do the following:

1. Stop IIS: open IIS Manager and click **Stop** on the right pane under **Manage Server > Actions**.

1. Stop all OutSystems Services. You can do this in the **Services** application in Windows to all services that start with 'OutSystems'.

1. Backup the `private.key` and `server.hsconf`files present in the installation folder (by default C:\Program files\OutSystems\Platform Server).

1. Uninstall the current OutSystems platform. This should be done by using the operating system's features to manage installed programs (for example, in Windows Server  **Control Panel > Programs and Features**).

1. Re-install the OutSystems platform on the new path (ex: D:\Program files\OutSystems\Platform Server). To do this you'll need to run `PlaformServer.exe` of the same version.

1. Restore the `private.key` file and `server.hsconf` files backed up on step 2 on the new installation path overwriting any files that may be present.

1. Start IIS: open IIS Manager and click **Start** on the right pane under **Manage Server > Actions**.

1. Open the Configuration Tool and click **Apply and Exit**.

1. A popup will be shown asking you to run the Service Center installation. Accept by clicking **Yes**.

1. Publish System Components.

1. Re-publish all apps.


## In any additional front-end server

If your OutSystems environment has additional front-end servers, after executing the above steps on the deployment controller server, execute steps 1 through 9 on each of the front-end servers.
