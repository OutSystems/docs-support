---
summary: Android - keystore file read issue. iOS - no certificates available
tags: mabs sig error_code
guid: da69e5ea-5f5a-4015-8491-7373f60ab6d8
locale: en-us
app_type: mobile apps
platform-version: o11, odc
---

# OS-MABS-SIG-40019

## Error message

Android - `There was an issue reading the alias from keystore file. Please review both the keystore file and alias.`

iOS - `There are no certificates available. Check your .p12 file or create a new one by checking our documentation.`

## Cause

This error can occur for both platforms: Android and iOS. On Android when the provided keystore file is invalid or corrupt. On iOS when the .p12 file does not contain a valid certificate.

## Impact

Users can't generate the application package.

## Recommended action

Check the application identifier and ensure that it follows the required format. Otherwise, replace it and retry.

Find more information about generating Android mobile applications [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/Generate_and_Publish_Your_Mobile_App_to_the_Mobile_App_Stores/Publish_Your_Mobile_Android_Application_to_the_Google_Play_Store).

Find more information about generating your certificate file for iOS [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/More_Information_on_Generating_and_Distributing_Mobile_Apps#create-a-certificate).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SIG-40019).
