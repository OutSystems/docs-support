---
summary: Missing property {0} on {1} in your extensibility configurations. Review it and try again.
summary: Invalid {0} type in your extensibility configurations. Review it and try again.
tags:
guid: 53eb9fbf-6dc5-43ad-ab70-69a709bfc9b4
locale: en-us
app_type: mobile apps
---

# OS-MABS-CNF-40005

## Error message

`Missing property {0} on {1} in your extensibility configurations. Review it and try again.`
or
`Invalid {0} type in your extensibility configurations. Review it and try again.`

## Cause

This error occurs when some required property in the extensibility configuration is missing.
or
This error occurs when some property in the extensibility configuration is invalid.

## Impact

The application package can't be generated.

## Recommended action

Check the extensibility configurations of your app and ensure the required property is declared.
or
Check the extensibility configurations of your app and ensure that there are no invalid properties.

Find more information about the extensibility configuration [here](https://success.outsystems.com/Documentation/11/Delivering_Mobile_Apps/Customize_Your_Mobile_App/Extensibility_Configurations_JSON_Schema).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-CNF-40005).
