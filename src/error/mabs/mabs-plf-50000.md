---
summary: Something happened on our side. Please try again.
tags: mobile app building, outsystems, error handling, troubleshooting, app deployment
locale: en-us
app_type: mobile apps
guid: 816b011f-8034-4550-b68e-9130cc80234a
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

# OS-MABS-PLF-50000

## Error message

`Something happened on our side. Please try again.`

## Cause

The application package generation failed due to an issue while MABS was bootstrapping the base cordova project with OutSystems native shell.

## Impact

Users can't generate the application package.

## Recommended action

Try to repeat the operation and check the build logs on Service Center.

Learn more about generating mobile apps and how to get the build logs [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLF-50000).
