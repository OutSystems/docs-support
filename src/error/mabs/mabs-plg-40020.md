---
summary: Couldn't install the Cordova plugin {0} because it's using a framework tag with type podspec, which is not supported from MABS 10 onwards. The podspec tag must be used instead.
tags:
guid: c659ed6c-8079-4e55-8517-0f2e626af3ca
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-PLG-40020

## Error message  

`Couldn't install the Cordova plugin {0} because it's using a framework tag with type podspec, which is not supported from MABS 10 onwards. The podspec tag must be used instead.`

## Cause

Generating the iOS application package failed because a `framework` tag with type `podspec` was used. This isn't possible in MABS 10 onwards because this feature was removed in [Cordova-iOS 7](https://cordova.apache.org/announcements/2023/07/10/cordova-ios-7.0.0.html).

## Impact

The iOS application package can't be generated.

## Recommended action

Update the plugin that is causing the error to the latest version.

If you're already using the latest version or updating is not feasible, modify the `plugin.xml` of the plugin. In that file, update the `framework` tags that have type `podspec` to [`podspec` tags](https://cordova.apache.org/docs/en/dev/plugin_ref/spec.html#podspec-).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40020).
