---
summary: Identify and resolve the "Extension recompilation on upgrade is disabled" publishing error.
tags: 
locale: en-us
guid: c37d5792-0a07-4eda-a3a2-a1e6be408968
---

# Publish error - Extension recompilation on upgrade is disabled

## Symptoms

You are executing a publishing operation that requires the Platform Server to automatically upgrade and recompile an extension, and you get the following error:

`Upgrade Disabled: Extension recompilation on upgrade is disabled.`

![upgrade disabled error](images/ext-recompilation-upgrade-disabled-error-sc.png)

This error can occur in environments running **Platform Server 11.14.0 or later**, in one of the following scenarios:

* Publishing an application or solution that includes an extension created in an earlier major version of OutSystems (for example, publishing an OutSystems 10 extension in an environment running OutSystems 11).

* Installing a Forge extension already created in an earlier major version of OutSystems.

* Publishing an extension after upgrading the Platform Server to a later major version (for example, from OutSystems 10 to OutSystems 11).

## Cause

When running **Platform Server 11.14.0** or later, the automatic upgrade and recompilation of extensions on the server-side is blocked by default. This prevents unattended and unwanted code modifications.

See more details [here](./extension-recompilation.md).

## Solution

To prevent unattended and unwanted code modifications when publishing the extension, do the following:

1. [Upgrade and recompile the extension in a secure way](./extension-recompilation.md#secure-upgrade).

1. Repeat the publishing operation.

### Accepting the risk

If you trust the origin of the extension that needs to be upgraded, you can choose to [accept the risk](./extension-recompilation.md#accept-risk) of unattended and unwanted code modifications for that specific upgrade operation.

If you choose to accept the risk, do the following:

1. **Temporarily** [enable automatic upgrade and recompilation of extensions](./extension-recompilation.md#enable-disable) in your environment. This operation must be performed by a Service Center administrator.

2. Repeat the publishing operation.

3. [Disable the option](./extension-recompilation.md#enable-disable). This operation must be performed by a Service Center administrator.
