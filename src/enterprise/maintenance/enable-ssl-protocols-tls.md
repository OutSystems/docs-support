---
summary:
---

# (.NET) Enable SSL Protocols for your Integrations - TLS 1.1 and TLS 1.2

## Introduction

When developing integrations with external services (REST, SOAP), there is often the need to use specific SSL protocols, namely:

* TLS 1.1

* TLS 1.2.

While trying to use those API's in OutSystems applications, such attempts to integrate may not work, and produce errors like:

* The request was aborted: Could not create SSL/TLS secure channel.

* Unsupported procotol. You need to enable TLS X.X to use this API

(other types of errors may occur, related to the required SSL protocols)

## Why do you see those errors

.NET Framework 4.5 (and older) uses, by default, two SSL Protocols: SSL v3 and TLS 1.0.

OutSystems Platform doesn't change those default values, so your request will only include (by default) SSLv3 and TLS 1.0. If the API requires a different protocol, which is not available, such errors will occur.

For more information on this, refer to the topics in the **References** section.

## Solution

It is possible for you to enable the protocol you need and include it in the request. That can be achieved through two steps:

* A. Enable the TLS protocols on the server, as "Client";

and one of the following:

* B1. Enable the SchUseStrongCrypto property in the Windows registry to use as the default protocols: TLS 1.0, TLS 1.1 and TLS 1.2

* B2. Include the TLS 1.1 and/or TLS 1.2 protocols in your application code, before the request to the API.

Note that, for cloud customers, option B2 is the only one available.

### A. Enable the TLS protocols on the server, as "Client"

To enable the TLS protocols, you need to add new registry entries for the Schannel [1]

For that, please follow this steps:

1. Start the registry editor by clicking on **Start** and **Run**. Type in "regedit" into the **Run** field (without quotations).

2. Highlight **Computer** at the top of the registry tree.  Backup the registry first by clicking on **File** and then on **Export**.  Select a file location to save the registry file.
    *Note: You will be editing the registry.  This could have detrimental effects on your computer if done incorrectly, so it is strongly advised to make a backup.*

3. Browse to the following registry key:
    `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols`

4. Right click on the **Protocols** folder and select **New** and then **Key** from the drop-down menu. This will create new folder.  Rename this folder to **TLS 1.1** or **TLS 1.2** (depending on the protocol you want to enable)

5. Right click on the **TLS 1.1 **or** TLS 1.2** key and add a new key underneath it.

6. Rename the new key as:

    * Client

7. Right click on the **Client** key and select **New** and then **DWORD (32-bit) Value** from the drop-down list.

8. Rename the **DWORD** to **DisabledByDefault**.

9. Right-click the name **DisabledByDefault** and select **Modify**... from the drop-down menu.

10. Ensure that the **Value** data field is set to **0** and the **Base** is **Hexadecimal**.  Click on OK.

11. Create another **DWORD** for the **Client** key as you did in **Step 7**.

12. Rename this second **DWORD** to **Enabled**.

13. Right-click the name **Enabled** and select **Modify**... from the drop-down menu.

14. Ensure that the **Value** data field is set to **1** and the **Base** is **Hexadecimal**. Click on OK.

15. **Reboot the server**

After the reboot, the server will be able to communicate through the SSL protocol you enabled. However, you need now to add it to your applications requests.

### B1. Enable the SchUseStrongCrypto property in the Windows registry to use as the default protocols: TLS 1.0, TLS 1.1 and TLS 1.2

If you want to make sure strong cryptography is enabled and the SSL protocols for your requests to be TLS 1.0, TLS 1.1 and TLS 1.2, please follow this steps:

1. Start the registry editor by clicking on **Start** and **Run**. Type in "regedit" into the **Run** field (without quotations).

2. Highlight **Computer** at the top of the registry tree.  Backup the registry first by clicking on **File** and then on **Export**.  Select a file location to save the registry file.
    *Note: You will be editing the registry.  This could have detrimental effects on your computer if done incorrectly, so it is strongly advised to make a backup.*

3. Browse to the following registry key:
    `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\.NetFramework\v4.0.30319`

4. Right-click on the right pane and create a new DWORD (32-bit) Value with Name **SchUseStrongCrypto**.

5. Ensure that the **Value** data field is set to **1** and the **Base** is **Hexadecimal**. Click on OK.

6. Repeat steps 4 and 5 for the registry key: HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\.NetFramework\v4.0.30319

7. **Reboot the server** 

### B2. Include the TLS 1.1 and/or TLS 1.2 protocols in your application code, before the request to the API.

Should you need higher control on the used protocols, there's a custom Extension that will allow you to:

* Get the current Security Protocols available for the request

* Add the TLS 1.1 protocol to the following requests

* Add the TLS 1.2 protocol to the following requests

You can get it from Forge: [ManageSecurityProtocols](https://www.outsystems.com/forge/Component_Overview.aspx?ProjectId=1413)

**_Note_***: please note that the Forge module is built by our community and it's not officially supported by the OutSystems Support.*

Should you notice any issues with the extension, please report them through **[Forge (tab Support)](https://www.outsystems.com/forge/component-discussions/1413/ManageSecurityProtocols)*.*

To allow you to use those protocols, you need to use one of the "AddTLS" actions (depending on which protocol you need) before you send a request to the API that requires that specific protocol.

## Applies to

OutSystems Platform on-premise on .NET, all database stacks.

Applies to Platform 9.0.x.y and 9.1.x.y (last reviewed under 9.1.600.0).

## References

[1] [https://technet.microsoft.com/en-us/...(v=ws.11).aspx](https://technet.microsoft.com/en-us/library/dn786418(v=ws.11).aspx)

[2] [https://support.microsoft.com/en-us/kb/3069494](https://support.microsoft.com/en-us/kb/3069494)

[3] [https://msdn.microsoft.com/en-us/lib...v=vs.110).aspx](https://msdn.microsoft.com/en-us/library/system.net.securityprotocoltype(v=vs.110).aspx)

[4] [http://blogs.perficient.com/microsof...d-net-support/](http://blogs.perficient.com/microsoft/2016/04/tsl-1-2-and-net-support/)

