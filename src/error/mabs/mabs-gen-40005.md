---
summary: There was an issue generating the app because {0} ‘{1}’ wasn’t found. Check if your plugins are up to date and compatible with the MABS version you’re using.
tags:
guid: 630be946-bfad-4fc2-b194-2544bbf72ed3
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-GEN-40005

## Error message

`There was an issue generating the app because {0} ‘{1}’ wasn’t found. Check if your plugins are up to date and compatible with the MABS version you’re using.`

## Cause

Generating the Android application package failed because a custom plugin points to a file that doesn’t exist.

## Impact

The Android application package can't be generated.

## Recommended action

Check the build logs on Service Center to confirm which custom plugin is affecting the package generation and update it.

Learn more about generating mobile apps and how to get the build logs [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40005).
