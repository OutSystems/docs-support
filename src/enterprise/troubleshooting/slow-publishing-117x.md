---
summary: Known issue that causes slow publishing in Platform Server versions 11.7.x. Check the causes, the mitigation, and the resolution.
locale: en-us
guid: e4883c46-2022-4c8e-9ecf-f09d524329a1
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---


# Slow publishing in OutSystems 11.7.x

There's a known issue in Platform Server versions 11.7.x that causes publishing to be slower in some circunstances. The issue was solved in Platform Server 11.8.0 and above. If you're upgrading the Platform Server, we advise using the latest version available.

## Symptoms

One of the following becomes slower after an upgrade to OutSystems version 11.7.x

* Solution publishing in ServiceCenter

* Application publishing in ServiceCenter

* LifeTime staging (via UI or API) to a target environment running 11.7.x or higher

When compared to publishing prior to the upgrade, the duration increased by 20% or more; this is especially felt in the deployment phase of the publishing operation.

### Affected configurations

The problem manifests if the following combination of factors occurs in the target environment (all conditions must apply):

1. Self-managed installations;

2. Running Platform Server 11.7.x;

3. Farm installations (with 2 or more front-ends);

4. The [deployment zone address](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Deploy_Applications/Selective_Deployment_Using_Deployment_Zones/Deployment_Zones_Reference) is the load balancer's hostname

**OutSystems Cloud customers are not affected**

### Confirm that you're affected

1. **Confirm the bottleneck on the Deployment phase**

Analyze the detailed publishing log (in Service Center or LifeTime) to confirm that each individual step of the Deployment phase takes longer than before (consult a prior deployment log if needed). Moreover, for each module (not extensions) the deployment takes approximately 1 minute and 30 seconds, as depicted below, instead of a few seconds as previously.
```
Updating tenant views of module ‘AdminLead_cs’.
Updating tenant views of module ‘AutomatedEmails_cs’.
Deploying module ‘RichWidgets’. (Last Step took 315).
Deploying module ‘Users’. (Last Step took 1m 27s).
Deploying module ‘W_Theme_UI’. (Last Step took 1m 285).
Deploying module ‘Countries’. (Last Step took 1m 28s).
Deploying module ‘WorldTimezone’. (Last Step took 1m 28s).
Deploying module ‘DiffEntityDataToText’. (Last Step took Im 28s).
```
 

1. **Identify the slow RefreshISAPIFilters action calls**

Once you confirm the previous pattern, filter the Service Center's General logs for SLOWEXTENSION and identify multiple entries like the below, during the deployment period for each module deployed, with durations of approximately 90.000 ms:

* *OMLProcessor.RefreshISAPIFilters took 88765 ms [actual value may vary]*

1. **Identify the errors connecting to Deployment Service**

After confirming the pattern above, locate errors like the below in Service Center's Error log - approximately one for each slow RefreshISAPIFilters in the same time period. Note the entry referring to **_RefreshPathRules_** - this is the important part. If you don’t see this, it’s not the relevant error:
```
A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond 10.0.21.8:12001
(...)
Exception rethrown at [0]:
   at System.Runtime.Remoting.Proxies.RealProxy.HandleReturnMessage(...)
   at System.Runtime.Remoting.Proxies.RealProxy.PrivateInvoke(...)
   at OutSystems.HubEdition.IBroadcastListener.MessageTransmission(...)
   at OutSystems.HubEdition.DeploymentController.Compiler.RefreshPathRules(...)
   at cs#pbxmkwit.InnerExecute()
   at OutSystems.HubEdition.ServerCommon.Tasks.AbstractTask.Execute()
   
```
 

## Cause

The problem occurs because the deployment controller service is trying to communicate with the deployment service through the IP address of the deployment zone address, instead of the front-end server address. 

In situations where that communication is not possible and the network connection is not explicitly rejected, the deployment controller will wait until a timeout is attained. This wait occurs for each module being deployed.

## Recovery

A workaround is already available for this problem in the most frequent farm configuration (farms in which the deployment controller is also a front-end), in the form of a reconfiguration of the platform. Environments with pure deployment controllers may opt to promote their deployment controller to also be a front-end, and then apply the workaround.

### Workaround

<div class="info" markdown="1">

**This workaround can only be applied when the controller server is also a front-end,** and it has the deployment service running. 
</div>

To overcome this situation, reconfigure the platform so that the deployment controller communicates with its own deployment service on IP 127.0.0.1.

To do that, the required steps are: 

1. Execute the following query in the environment's database:
```
insert into ossys_parameter (name, VAL) VALUES ('Compiler.UseFrontEndAddressRefreshPaths', 'False')
```
2. Restart the deployment controller service in the controller server.

#### Resolution

Platform Server version 11.8.0 includes the fix for this problem. The fix is identified with the reference RPD-4770 on our [Release Notes](https://success.outsystems.com/Support/Release_Notes/11/Platform_Server).

