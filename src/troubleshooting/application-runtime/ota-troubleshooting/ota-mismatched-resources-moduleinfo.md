---
summary: Downloaded resources do not match the resources listed in the moduleinfo
locale: en-us
guid: B34D4527-D30A-4149-8982-8C031DDCCE26
app_type: mobile apps
platform-version: o11
---

# Downloaded resources do not match the resources listed in the moduleinfo

## What are the errors?

* ``Checksum failed for file <Resource_Path>?<Resource_Hash> Received hash: <Resource_Hash> | Calculated hash: <Another_Hash>``

* ``Failed to store download resource <Resource_Path>?<Resource_Hash> with error: File is corrupt or invalid.``

* ``Upgrade failed - rolling back to the previous application version.``

## Where is this occurring and what does it mean?

As described in step 9 ([see OTA upgrade process diagram](https://success.outsystems.com/documentation/11/delivering_mobile_apps/mobile_app_update_scenarios/over_the_air_upgrades/#ota-upgrade-process-diagram)),after downloading each resource from the server, the mobile application validates whether or not the downloaded file matches the one in the **moduleinfo** list. To do that, it calculates the hash of the file, based on its content and compares it with the hash associated with that file in the **moduleinfo**.

This error means that the content of the ``<Resource_Path>?<Resource_Hash>`` downloaded doesn’t have the expected hash and is considered corrupt.

The following are the reasons this validation fails:

* If there are any network elements caching resources. In this scenario, the app expects to download a specific resource version (from the server), but if a different version of that same resource is cached in the network interface (for example, a Load Balancer, a CDN or a Proxy), the validation fails.
    
* If there’s any third-party component manipulating the resource (for example, a Load Balancer, a CDN or a Proxy) before it reaches the client (for example, a mobile device), changing its content and consequently changing the value of the hash calculated by the application. 

* If for some reason (for example, failed or inconsistent deployment) the resources’ content deployed in the **running** folder does not match their hashes in the **moduleinfo**.

* If during the OTA upgrade, a new deployment of the application is made in the server. This causes the app to download resources that are from a newer version of the app and not from the **moduleinfo** that was fetched at the beginning of the OTA upgrade process.

## What is the impact of this error on the mobile application?

In most cases, the mobile app is rolled back to the previous version cached in the device. Runtime issues may occur depending on the changes introduced in the new version. The impact on the end users may vary depending on the frequency and delta size of the upgrade OTA. 

The most critical impact of this error is when **index.html** is affected. This file is the application’s main file and, if it fails to load on the WebView, the application stops working. Reinstalling the app usually fixes this error.

## How to overcome this issue?

### On-premises Environments

If the validation fails, you need to check the following: 

* What resource and resource version failed to be stored by checking the error message.

* What version of the resource is listed in the **moduleinfo**.

* What version of the resource was deployed in the frontend at the moment of validation failure. You can get this information in the **Running** folder of the affected Modules.

* What is the content of the resource if you download it directly from the browser.

**Troubleshoot tools**

Use the Hash Calculator tool to compare the 2 files - the version from the frontend versus the version received in the browser. You can request this calculator from OutSystems Support.  The Hash Calculator tool is effective as you can compare the hash of the files in the frontend versions of what was received and calculated. If any of the hashes are not consistent, it gives you a hint of where the problem is. Note that these hash values must be fetched at the same time, that is, without any new deployment on the server.

**Troubleshoot paths**

* If the Hash of a resource on a particular frontend doesn’t match the calculated Hash in the Error log, this means that this frontend doesn’t have the most up-to-date resources:

    * Double-check that the deployment was performed as expected in all the frontends that are serving the application. For example, if the OutSystems Deployment Service was disabled in one of the frontends (when the deployment was performed), the respective frontend will be serving outdated resources and will cause this error until the correct version is deployed in all frontends.

* If the Hash of a resource on all frontends match the calculated Hash, but the received Hash is not the same on the device, this indicates an issue on the network.

    * If there is any network component caching the resources, ensure that this cache is completely purged before reloading the app on the mobile device.

    * If you have any network element or software that is tampering with the requests (for example, injecting content for monitoring purposes) disable the functionality, at least temporarily, to mitigate the situation.

### OutSystems Cloud Environments

To troubleshoot this issue on an OutSystems Cloud Environment, you must open a support case with the OutSystems Support team. Keep in mind that, in the vast majority of situations reported on the OutSystems Cloud Environment, the cause tends to be a network issue (outside of OutSystems control).

* If there is any network component caching the resources, ensure that this cache is completely purged before reloading the app on the mobile device.

* If you have any network element or software that is tampering with the requests (for example, injecting content for monitoring purposes) disable the functionality, at least temporarily, to mitigate the situation.


