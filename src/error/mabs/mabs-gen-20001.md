---
summary: Your app wasn’t generated because the required dependency for the {0} node module in a plugin hook was missing. Check the product documentation on how to ensure your plugins node dependencies.
tags:
guid: acc20652-0581-4457-83fd-992a8dbd43d6
locale: en-us
app_type: mobile apps
platform-version: o11
---

# OS-MABS-GEN-20001

## Error Message

`Your app wasn’t generated because the required dependency for the {0} node module in a plugin hook was missing. Check the product documentation on how to ensure your plugins node dependencies.`

## Cause

Generating the application package failed due to a missing node dependency in a plugin hook.

## Impact

The application package can't be generated.

## Recommended action

Check the build logs on Service Center and confirm which custom plugin hook has a missing node dependency.

Learn more about generating mobile apps and how to get the build logs [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-20001).
