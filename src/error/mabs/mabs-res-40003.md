---
summary: The configuration file has an invalid format. Add a file with a valid format for SSLPinning. Learn more about configuration files in our documentation.
tags:
guid: 304aa7a9-1cef-4535-b1ed-9b3c0b1b1b84
locale: en-us
app_type: mobile apps
platform-version: o11, odc
---

# OS-MABS-RES-40003

## Error message

`The configuration file has an invalid format. Add a file with a valid format for SSLPinning. Learn more about configuration files in our documentation.`

## Cause

This error occurs when MABS detects an SSLPinning configuration file with an invalid format or information.

## Impact

Users can't generate the application package.

## Recommended action

When using the SSL Pinning plugin, you need to upload a configuration file that will contain information for the SSL Pinning feature in your application.

This configuration file must follow a specific format. Find more about this configuration file [here](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Mobile_Plugins/SSL_Pinning_Plugin#create-the-configuration-file).

Validate the SSL Pinning configuration file to find and fix the inconsistency and retry the building the application.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-RES-40003).
