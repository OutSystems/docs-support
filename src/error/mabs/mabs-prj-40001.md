---
summary: "OS-MABS-PRJ-40001 in OutSystems Developer Cloud (ODC) occurs when the splash screen branding image isn't 1024x1024 pixels."
tags:
  - Mobile app
  - Native App
  - Troubleshooting
guid: 669e2b75-049d-4b7f-8e47-dcd0ec55f0e5
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
audience:
  - Developer
outsystems-tools:
  - odc studio
coverage-type:
  - unblock
isautopublish: true
---

# OS-MABS-PRJ-40001

## Error message

`Branding image for <Screen> must be 1024x1024 pixels, but is <Actual>.`

## Cause

This error occurs when a branding image configured for the splash screen doesn't have the required 1024x1024 pixel dimensions.

## Impact

The app package can't be generated.

## Recommended action

Resize the branding image to exactly 1024x1024 pixels and update your app's splash screen configuration in app properties to point to the corrected image. Regenerate your app again.

For more information about customizing splash screens, refer to [Customize the splash screen](https://success.outsystems.com/documentation/outsystems_developer_cloud/building_apps/mobile_apps/customize_the_splash_screen/).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PRJ-40001).
