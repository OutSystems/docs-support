---
summary: There was an issue loading your resources. Please try again.
tags: mobile app build process, error handling, resource management, application packaging
guid: c26c0ff1-4228-4fb0-af5c-ba4c8f2757b5
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
audience:
  - mobile developers
  - full stack developers
  - platform administrators
outsystems-tools:
  - service studio
  - service center
coverage-type:
  - unblock
---

# OS-MABS-RES-50000

## Error message

`There was an issue loading your resources. Please try again.`

## Cause

This error occurs when MABS encounters an issue when processing the OutSystems resources to build the application package.

## Impact

Users can't generate the application package.

## Recommended action

Validate the correctness of any resource file added in your application and try to repeat the operation and check the build logs on Service Center.

Resource usage range from adding custom [icons](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Modify_the_App_Icon) or [splashscreens](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Use_Custom_Splash_Screens), to using [custom mobile plugins](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Mobile_Plugins/Using_Cordova_Plugins) in a zip file, amongst other scenarios.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-RES-50000).
