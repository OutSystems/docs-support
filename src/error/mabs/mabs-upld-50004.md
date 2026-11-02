---
summary: OS-MABS-UPLD-50004 error occurs when ODC can't deliver your app to Google Play because of an issue on Google's side.
tags:
  - Android
  - Deploy
  - Mobile app
  - Troubleshooting
coverage-type:
  - unblock
topic:
  - google-play-console-upload-errors
audience:
  - Developer
guid: 4ea3a1ff-375f-4aff-9f3f-5de392e1c866
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-MABS-UPLD-50004

## Error message

`The Google Play Developer API encountered an internal error. Try again.`

## Cause

ODC uses the Google Play Developer API associated with your Google Cloud service account to upload app bundle builds to the Google Play Console. This error occurs when that API returns a server error, times out, rate-limits the request, or when the upload fails without a specific reason from Google.

## Impact

ODC can't upload your app bundle build to the Google Play Console.

## Recommended action

Upload your app again. If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-UPLD-50004).
