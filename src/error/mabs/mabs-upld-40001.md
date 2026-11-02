---
summary: The App Store Connect private key isn't valid. Use the .p8 file you downloaded from App Store Connect and try again.
tags:
  - iOS
  - Mobile app
  - Native App
  - Settings
  - Troubleshooting
guid: 7e7b5889-9a45-4a0c-ae3a-5eacd4be933c
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
audience:
  - Developer
  - Platform administrator
outsystems-tools:
  - odc portal
coverage-type:
  - unblock
topic:
---

# OS-MABS-UPLD-40001

## Error message

`The App Store Connect private key isn't valid. Use the .p8 file you downloaded from App Store Connect and try again.`

## Cause

The value saved as the App Store Connect private key isn't a usable .p8 private key. The value holds a different type of key, such as an RSA key, or its contents are incomplete.

How you send the key determines whether encoding is part of the cause:

* In the ODC Portal, you upload the .p8 file and the Portal encodes it for you. Encoding isn't a cause here.
* Through the public API, you send the key as a Base64-encoded string. A value that isn't Base64-encoded produces this error even when the underlying .p8 file is valid.

## Impact

ODC doesn't save the App Store Connect configuration, and the previous configuration stays in place.

## Recommended action

Download the API key from App Store Connect as a .p8 file, and then save it the way that matches how you configure ODC:

* In the ODC Portal, upload the .p8 file without changing its contents.
* Through the public API, encode the contents of the .p8 file in Base64 and send the encoded value.

If you no longer have the .p8 file, create an API key in App Store Connect and save the key file you download.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40001).
