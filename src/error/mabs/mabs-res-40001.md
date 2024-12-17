---
summary: The configuration file for SSLPinning must not contain OutSystems domains. Review the JSON file and delete any OutSystems domains.
tags: ssl pinning, mobile app security, error handling, application building, outsystems mabs
guid: 30dec9fe-2fc7-4f3b-8572-6baf5c73958d
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
audience:
  - mobile developers
  - platform administrators
outsystems-tools:
  - mobile plugins
coverage-type:
  - unblock
---

# OS-MABS-RES-40001

## Error message

`The configuration file for SSLPinning must not contain OutSystems domains. Review the JSON file and delete any OutSystems domains.`

## Cause

This error occurs when MABS detects an OutSystems domain on your SSLPinning configuration file.

## Impact

Users can't generate the application package.

## Recommended action

OutSystems no longer supports the usage of OutSystems domains for your SSL Pinning configuration. Learn more about the SSL Pinning configuration [here](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Mobile_Plugins/SSL_Pinning_Plugin#important-note-about-certificates).

Change your SSL Pinning configuration and retry building the application.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-RES-40001).
