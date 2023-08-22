---
summary: There's a splash screen missing in your extensibility configurations with {0}.
tags:
guid: 8fce2d5f-62b5-41fa-b865-61ce9d8ead3f
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-CNF-40001

## Error message

`There's a splash screen missing in your extensibility configurations with {0}.`

## Cause

The density and/or size of the splash screen is missing in the specific configuration.

## Impact

The application package can't be generated.

## Recommended action

Check the extensibility configurations of your app to ensure that the splash screen with the required density and/or size exists and fix it, as needed.

Find more information about how to modify the application splash screen [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Use_Custom_Splash_Screens).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-CNF-40001).
