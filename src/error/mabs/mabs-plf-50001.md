---
summary: There was an issue in the connection to a server. This might be caused by a server downtime.
tags: mabs plf error_codes
locale: en-us
app_type: mobile apps
guid: 3852bcd4-12bf-4bef-9a72-55d31e3750ce
platform-version: o11, odc
---
# OS-MABS-PLF-50001

## Error message

`There was an issue in the connection to a server. This might be caused by a server downtime.`

## Cause

The application package generation failed due to an issue when trying to download some external dependencies, while MABS was bootstrapping the base cordova project with OutSystems native shell.

## Impact

Users can't generate the application package.

## Recommended action

Try to repeat the operation and check the build logs on Service Center.

Learn more about generating mobile apps and how to get the build logs [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLF-50001).
