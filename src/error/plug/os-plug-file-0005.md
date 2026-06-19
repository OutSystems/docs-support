---
summary: OS-PLUG-FILE-0005 OutSystems File Plugin error occurs when method input parameters like Path or Directory are invalid, missing, or wrong type.
tags:
  - Android
  - Cordova
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 7308dd6d-9be3-43dc-987a-21024621c74e
app_type: mobile apps
platform-version: odc,o11
figma:
audience:
  - Developer
  - Front-end developer
outsystems-tools:
  - service studio
  - odc studio
coverage-type:
  - unblock
topic:
  - using-cordova-plugins
  - wrap-cordova-plugin
isautopublish: true
---

# OS-PLUG-FILE-0005

## Error message

"The `<method-name>` input parameters aren't valid."

## Platform

iOS and Android

## Cause

One or more of the parameters passed to the specified method are invalid, missing, or of an unexpected type. Each plugin method expects specific parameters (for example, `Path` and `Directory`), and this error is thrown when those expectations are not met.

## Impact

The requested filesystem operation won't be executed.

## Recommended action

Review the documentation for the method referenced in the error message and verify that all required parameters are provided with valid values. In particular:

* Ensure that text parameters such as `Path` are not empty when required.
* Ensure that the `Directory` parameter uses one of the accepted values from its static entity, rather than providing a string directly.
* Check that no required parameter is missing or has an empty value.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-FILE-0005).
