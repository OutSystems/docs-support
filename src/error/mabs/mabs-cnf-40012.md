---
summary: Missing resource declared in the extensibility configurations.
tags: mobile app development, extensibility configurations, json schema, error handling, application packaging
guid: f671b509-847d-4535-b224-6665ce2986b7
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
audience:
  - mobile developers
outsystems-tools:
  - service studio
coverage-type:
  - unblock
---

# OS-MABS-CNF-40012

## Error message

`Couldn't generate your app because the resource {0} declared in your extensibility configurations can't be found. Check the resources in your extensibility configurations and retry.`

## Cause

This error occurs when a resource defined in extensibility configurations' `resources` has its `src` pointing to a missing file.


## Impact

The application package can't be generated.

## Recommended action

Check the extensibility configurations of your app and its dependencies to ensure that each of the resources declared in the extensibility configurations meets the requirements.

Find more information about the extensibility configurations resources:

* [OutSystems 11 - Extensibility configurations JSON schema](https://success.outsystems.com/documentation/11/delivering_mobile_apps/customize_your_mobile_app/extensibility_configurations_json_schema/#resources)
* [ODC - Extensibility configurations JSON schema](https://success.outsystems.com/documentation/outsystems_developer_cloud/building_apps/mobile_apps/extensibility_configurations_json_schema/#resources)

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-CNF-40012).
