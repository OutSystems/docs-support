---
summary: The Keystore operation requires user interaction, but the app is currently running in a context where it is not allowed.
tags:
  - iOS
  - Mobile app
  - Plugins
  - Troubleshooting
locale: en-us
guid: 13d98420-d373-4f5d-a53d-d8b86dc60b19
app_type: mobile apps
platform-version: odc,o11
figma:
audience:
  - Developer
  - Front-end developer
outsystems-tools:
  - service studio
  - odc studio
coverage-type:
  - unblock
topic:
  - using-cordova-plugins
  - wrap-cordova-plugin
isautopublish: true
---

# OS-PLUG-KSTR-0008

## Error message

User interaction is currently not allowed.

## Platform

iOS

## Cause

The iOS Keychain API returned an `errSecInteractionNotAllowed` status. The Keychain item being accessed requires user authentication (for example, a biometric prompt or a passcode entry), but the app is currently running in a context where user interaction is not permitted, such as in the background or during device startup before the first unlock.

## Impact

The requested Keystore operation cannot be completed because the required authentication prompt cannot be displayed.

## Recommended action

Ensure the Keystore operation is triggered only when the app is in the foreground and the device is fully unlocked. Avoid calling the plugin in background tasks, push notification handlers, or other non-interactive execution contexts.

If the problem persists, open a support case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-PLUG-KSTR-0008).
