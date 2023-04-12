---
summary: Your app wasn't generated because we couldn't fetch its dependencies due to a CocoaPods server error. Please try again.
tags: mabs plf error_codes
locale: en-us
app_type: mobile apps
guid: 6b5393fd-96f3-471b-b715-a7a563ef91f7
platform-version: o11, odc
---
# OS-MABS-PLF-50002

## Error message

`Your app wasn't generated because we couldn't fetch its dependencies due to a CocoaPods server error. Please try again.`

## Cause

This error occurs when something unexpected happened while MABS is bootstrapping the base cordova project with OutSystems native shell on iOS applications while trying to download some dependencies from CocoaPods. This might be caused by issues on the CocoaPods CDN.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center for more details about the error and fix them. Then, try to generate your application again.

If the problem persists, create a case with [OutSystems
support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLF-50002).
