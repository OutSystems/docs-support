---
summary: Your app wasn’t generated because we couldn’t fetch its dependencies from the repository server {0} due to a server error. Please try again.
tags:
guid: be168032-545a-43eb-814c-b599b0b58547
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-GEN-50001

## Error message

`Your app wasn’t generated because we couldn’t fetch its dependencies from the repository server {0} due to a server error. Please try again.`

## Cause

Generating the Android application package failed due to downtime on some maven repository server.

## Impact

The Android application package can't be generated.

## Recommended action

Check the build logs on Service Center and repeat the operation. If possible, you could also change the used maven repository.

Learn more about generating mobile apps and how to get the build logs [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-50001).
