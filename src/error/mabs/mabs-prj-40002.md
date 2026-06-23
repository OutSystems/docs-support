---
summary: "OS-MABS-PRJ-40002 in OutSystems Developer Cloud (ODC) occurs when a splash screen branding image is corrupted or in an unsupported format."
tags:
  - Mobile app
  - Native App
  - Troubleshooting
guid: 22cdb0b4-c0f9-4803-b5ac-95cf38db05b4
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

# OS-MABS-PRJ-40002

## Error message

`Branding image for <Screen> couldn't be read. The file may be corrupted or in an unsupported format.`

## Cause

This error occurs when a branding image configured for the splash screen can't be correctly read. Common causes are:

* The file is corrupted or incomplete.
* The file is in an unsupported format. Use a standard PNG image to avoid format compatibility issues.
* The file has an image extension but doesn't contain valid image data.

## Impact

The app package can't be generated.

## Recommended action

Open the branding image in an image editor to confirm it's valid, then export it again as a 1024x1024 PNG. Update your app's splash screen configuration in app properties to point to the corrected image. Regenerate your app again.

For more information about customizing splash screens, refer to [Customize the splash screen](https://success.outsystems.com/documentation/outsystems_developer_cloud/building_apps/mobile_apps/customize_the_splash_screen/).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PRJ-40002).
