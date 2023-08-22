---
summary: The application build type (<requestBuildType>) must match the provisioning profile (<provisioningBuildType>).
tags: mabs sig error_code
guid: 723b286b-06ff-494c-8160-bc6307e0b1e7
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-SIG-40002

## Error message

`The application build type (<requestBuildType>) must match the provisioning profile (<provisioningBuildType>).`

## Cause

This error occurs when generating an iOS app of the build type &lt;requestBuildType&gt; but using a provisioning profile that's not valid for that build type (&lt;provisioningBuildType&gt;).

## Impact

Users can't generate the application package.

## Recommended action

Check if your provisioning profile matches the build type. Otherwise, change the build type or the provisioning profile.

Find more information about generating iOS mobile applications [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App/Generate_and_Publish_Your_Mobile_App_to_the_Mobile_App_Stores/Publish_Your_Mobile_iOS_Application_to_the_Apple_App_Store).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-SIG-40002).
