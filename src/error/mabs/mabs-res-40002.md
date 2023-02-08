---
summary: The configuration file is missing. Add a valid configuration file for SSLPinning. Learn more about configuration files in our documentation.
tags:
guid: 27ccb435-2ddc-4006-8eef-6982959107b3
locale: en-us
app_type: mobile apps
platform-version: o11
---

# OS-MABS-RES-40002

## Error message

`The configuration file is missing. Add a valid configuration file for SSLPinning. Learn more about configuration files in our documentation.`

## Cause

This error occurs when MABS detects the usage of the SSLPinning Plugin but it is missing its mandatory configuration file.

## Impact

Users can't generate the application package.

## Recommended action

When using the SSL Pinning plugin, you need to upload a configuration file that will contain information for the SSL Pinning feature in your application. Find more about this configuration file [here](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Mobile_Plugins/SSL_Pinning_Plugin#create-the-configuration-file).

Add the SSL Pinning configuration file to your application and retry the building operation.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-RES-40002).
