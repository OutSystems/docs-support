---
summary: Couldn't generate your app. For "<type>" type elements with defined intent filters, you must declare the value for the attribute "android:exported" in all AndroidManifest.xml files.
tags:
guid: c780d4d5-d779-434a-8a34-391faf16cd79
locale: en-us
app_type: mobile apps
---

# OS-MABS-GEN-40016

## Error message

`Couldn't generate your app. For "<type>" type elements with defined intent filters, you must declare the value for the attribute "android:exported" in all AndroidManifest.xml files.`

## Cause

This error occurs when you are generating an Android package. When you are using custom plugins (with MABS 8.0 or higher), you must declare the `"android:exported"` attribute and it’s value (`"true"` or `"false"`) for specific type elements with defined intent filters, inside the **AndroidManifest.xml** files. **&lt;type&gt;** refers to the type elements (activity, service, or broadcast receiver) in which you must set the attribute.

## Impact

Users can't generate the application package.

## Recommended action

For custom plugins, declare in the **AndroidManifest.xml** files the attribute for `"android:exported"` and it’s value (`"true"` or `"false"`) on type elements with defined intent filters.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-GEN-40016).
