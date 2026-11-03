---
summary: OS-MABS-UPLD-40013 error occurs when Google Play Console rejected the service account key. Check that the key is still active in the Google Cloud project and its service account has not been deleted.
tags:
  - Android
  - Authentication
  - Mobile app
  - Security
  - Troubleshooting
coverage-type:
  - unblock
topic:
  - fix-service-key-rejection
audience:
  - Developer
  - Platform administrator
guid: 5a1a2b12-3fca-4062-be52-5fa9e84fabbc
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-MABS-UPLD-40013

## Error message

`Google Play Console rejected the service account key. Check that the key is still active in the Google Cloud project and its service account has not been deleted`

## Cause

ODC signs an authentication token with your service account key before it uploads your app bundle build to the Google Play Console. This error occurs when Google rejects that token because the service account key was revoked, rotated, or modified in place, or the service account itself was deleted.

## Impact

ODC can't upload your app bundle build to the Google Play Console.

## Recommended action

* Check the service account in the Google Cloud console. If it was deleted, create a service account, create a JSON key for this service account, then upload the new key as the new Service Account JSON in ODC.
* Confirm that the values of the `client_email` and `private_key` keys in the json file have not been modified.
* If the key was revoked, rotated, or modified in place, generate a new JSON key and upload it as the new Service Account JSON in ODC.

For more information, refer to the official Google Cloud documentation on how to [Create and list service account keys](https://docs.cloud.google.com/iam/docs/keys-create-delete).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-40013).
