---
summary: Please enter the right password for the alias.
tags: mabs sig error_code
guid: 751b3c1c-a3d6-43d3-a5fe-16f72b90e027
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-SIG-40014

## Error message

`Please enter the right password for the alias.`

## Cause

This error occurs when generating an Android app and the password for the alias inside the keystore file is incorrect.

## Impact

Users can't generate the application package.

## Recommended action

Check if the password for the alias inside the keystore file is correct. Otherwise, replace it and retry.

Find more information about generating Android mobile applications [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/Generate_and_Publish_Your_Mobile_App_to_the_Mobile_App_Stores/Publish_Your_Mobile_Android_Application_to_the_Google_Play_Store).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SIG-40014).
