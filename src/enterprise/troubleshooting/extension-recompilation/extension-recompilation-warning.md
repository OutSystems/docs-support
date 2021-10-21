---
summary: Identify and resolve the publishing warning "Continuing with extension recompilation enabled may result in security flaws".
tags: 
---

# Publish warning: Continuing with extension recompilation enabled may result in security flaws

## Symptoms

You are executing a publishing operation and you get the following warning:

`Continuing with extension recompilation enabled may result in security flaws. You can disable it in the environment configuration.`

![extension recompilation enabled warning](images/ext-recompilation-enabled-warning-sc.png)

This warning can occur in environments running **Platform Server 11.14.0 or later**.

## Cause

Starting from **Platform Server 11.14.0**, the automatic upgrade and recompilation of extensions is blocked on the server-side by default to prevent unattended and unwanted modifications of code.

This warning indicates that the automatic upgrade and recompilation of extensions **is enabled** in your environment. Therefore, your environment is exposed to unattended and unwanted modifications of code whenever the Platform Server automatically upgrades and recompiles extensions in the following scenarios:

* Publishing an application or solution that includes an extension created in an earlier OutSystems major version (for example, publishing an OutSystems 10 extension in an environment running OutSystems 11).

* Installing from Forge an extension created in an earlier OutSystems major version.

* Publishing an extension after upgrading the Platform Server to a later major version (for example, from OutSystems 10 to OutSystems 11).

See more details [here](../../upgrade/extension-recompilation/extension-recompilation.md).

## Recommendation

To prevent unattended and unwanted modifications of code in extension upgrade scenarios, keep the automatic upgrade and recompilation of extensions **disabled** and execute the upgrade and recompilation of extensions in a secure way.

Do the following:

1. [Disable the automatic upgrade and recompilation of extensions](../../upgrade/extension-recompilation/extension-recompilation.md#enable-disable) in the environment. This operation must be performed by a Service Center administrator.

1. In the described scenarios, [upgrade and recompile extensions in a secure way](../../upgrade/extension-recompilation/extension-recompilation.md#secure-upgrade).

If you get the error `Extension recompilation on upgrade is disabled` during the publishing process, execute the upgrade and recompilation of that extension in a secure way. See the details [here](extension-upgrade-disabled-error.md).

## Accepting the risk

If you trust the origin of the extensions that need to be upgraded, you can choose to [accept the risk](../../upgrade/extension-recompilation/extension-recompilation.md#accept-risk) of unattended and unwanted modifications of code for that specific upgrade operation and keep the automatic upgrade and recompilation of extensions enabled. However, OutSystems recommends that you [disable the option](../../upgrade/extension-recompilation/extension-recompilation.md#enable-disable) afterward.
