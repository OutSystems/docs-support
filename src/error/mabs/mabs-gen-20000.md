---
summary: Your app wasn’t generated because an action was blocked due to security concerns. Contact the support team if this problem persists.
tags:
guid: 9807a6d6-d714-4390-b24c-0240e2c0058a
locale: en-us
app_type: mobile apps
---

# OS-MABS-GEN-20000

## Error Message

`Your app wasn’t generated because an action was blocked due to security concerns. Contact the support team if this problem persists.`

## Cause

Generating the application package failed due to a custom plugin trying to execute non-permitted actions.

## Impact

The application package can't be generated.

## Recommended action

Check the build logs on Service Center and confirm which custom plugin is trying to execute non-permitted actions.

Learn more about generating mobile apps and how to get the build logs [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Generate_and_Distribute_Your_Mobile_App#download-mobile-app-build-logs).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-20000).
