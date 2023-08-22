---
summary: The Forge <plugin_name> isn't compatible with MABS version <MABS_version>. Update it to <plugin_min_version> or higher.
tags:
guid: de2ad3fc-1ff1-4ed9-810a-f90e1ad7cea0
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-PLG-40019

## Error message

`The Forge <plugin_name> isn't compatible with MABS version <MABS_version>. Update it to <plugin_min_version> or higher.`

## Cause

This error occurs when a Forge plugin isn't compatible with a specific MABS version (MABS 8.0 or higher). The **&lt;plugin_name&gt;** refers to the plugin name on Forge. The **&lt;MABS_version&gt;** refers to the MABS version that you are using to generate your application. The **&lt;plugin_min_version&gt;** refers to the minimum plugin version that is compatible with the MABS version that you are trying to use. 

## Impact

Users can't generate the application package.

## Recommended action

Update your Forge plugin version to **&lt;plugin_min_version&gt;** or higher. Check the [plugin’s documentation](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/Mobile_Plugins) for more information.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PLG-40019).
