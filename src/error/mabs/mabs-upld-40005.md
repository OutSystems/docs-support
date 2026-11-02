---
summary: The App Store Connect API key isn't a valid .p8 private key. Upload the key file you downloaded from App Store Connect and try again.
tags:
  - iOS
  - Mobile app
  - Native App
  - Troubleshooting
guid: 629cf229-21ea-4650-9305-9e6f4a61f56b
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
audience:
  - Developer
outsystems-tools:
  - odc portal
coverage-type:
  - unblock
topic:
---

# OS-MABS-UPLD-40005

## Error message

`The App Store Connect API key isn't a valid .p8 private key. Upload the key file you downloaded from App Store Connect and try again.`

## Cause

ODC checks the API key before it contacts App Store Connect, and the key isn't a PEM-encoded elliptic curve private key. The key file holds a different type of key, such as an RSA key, or its contents are incomplete.

## Impact

The upload to App Store Connect doesn't start.

## Recommended action

Add the .p8 file you downloaded from App Store Connect to the App Store Connect configuration, and then upload again. Don't change the contents of the file.

If you no longer have the .p8 file, create an API key in App Store Connect and update the configuration with the key file you download.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40005).
