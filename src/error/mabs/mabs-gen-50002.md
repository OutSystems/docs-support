---
summary: OS-MABS-GEN-50002 occurs when a network timeout interrupts npm install on the OutSystems platform, blocking MABS app package generation.
tags:
  - Mobile app
  - Plugins
  - Troubleshooting
guid: 482e34ad-101e-47df-90ca-8234f43d2a47
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
audience:
  - Developer
outsystems-tools:
  - service center
coverage-type:
  - unblock
isautopublish: true
---

# OS-MABS-GEN-50002

## Error message

`There was a network connectivity issue during npm install. This may be a transient error. Please try again.`

## Cause

There was a network timeout or interruption while installing the required dependency packages.

## Impact

The app package can't be generated.

## Recommended action

This is an internal issue. Rebuild the package by going to the ODC Portal and opening your app’s detail page. Click **Mobile distribution** and trigger a new build.

For detailed information, refer to [Create mobile app package](https://success.outsystems.com/documentation/outsystems_developer_cloud/building_apps/mobile_apps/create_mobile_app_package/).
