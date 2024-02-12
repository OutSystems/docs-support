---
summary: Restricted path for the resource declared in the extensibility configurations.
tags:
guid: 1fba16c8-f7ca-400c-8824-9bc0a167f51c
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-CNF-40011

## Error message

`Couldn't generate your app because the {0} property of a resource declared in your extensibility configurations points to a restricted path. Check the resources in your extensibility configurations and retry.`

## Cause

This error occurs when a resource defined in extensibility configurations' `resources` has its `src` or `target` properties pointing to a restricted path.

The values of `src` and `target` properties are paths relative to Cordova's project root folder and platform project root folder, respectively. The resolved path must always be within them.

## Impact

The application package can't be generated.

## Recommended action

Check the extensibility configurations of your app and its dependencies to ensure that each of the resources declared in the extensibility configurations meets the requirements.

Find more information about the extensibility configurations resources:

* [OutSystems 11 - Extensibility configurations JSON schema](https://success.outsystems.com/documentation/11/delivering_mobile_apps/customize_your_mobile_app/extensibility_configurations_json_schema/#resources)
* [ODC - Extensibility configurations JSON schema](https://success.outsystems.com/documentation/outsystems_developer_cloud/building_apps/mobile_apps/extensibility_configurations_json_schema/#resources)

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-CNF-40011).
