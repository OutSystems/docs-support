---
summary: "OS-MABS-PRJ-40003 in OutSystems Developer Cloud (ODC) occurs when Capacitor plugins aren't compatible with the iOS package manager (SPM or CocoaPods)."
tags:
  - Capacitor
  - iOS
  - Libraries
  - Mobile app
  - Native App
  - Plugins
  - Troubleshooting
guid: 13ae5b4e-bf7b-48d1-b047-4515e843fa18
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
audience:
  - Developer
outsystems-tools:
  - odc portal
  - odc studio
coverage-type:
  - understand
  - unblock
isautopublish: true
---

# OS-MABS-PRJ-40003

## Error message

`One or more Capacitor plugins aren't compatible with <PackageManager>. Review build logs for details.`

## Cause

This error occurs when the package manager selected for the code project, `SPM` or `CocoaPods`, doesn't support one or more of the Capacitor plugins required by your app or its libraries. The build logs identify the incompatible plugins.

The **spmPreview** configuration in the [app universal extensibility schema](https://success.outsystems.com/documentation/outsystems_developer_cloud/building_apps/mobile_apps/configure_mobile_apps/universal_extensibility_configurations_json_schema/app_extensibility_configuration_json_schema/) determines which package manager the code project uses:

* When **spmPreview** is enabled, the code project uses Swift Package Manager (SPM). Plugins that only ship a `.podspec` (CocoaPods) and not `Package.swift` (SPM) aren't compatible.
* When **SPM Preview** is disabled, the code project uses CocoaPods. Plugins that only ship `Package.swift` and not `.podspec` aren't compatible.

For example, to enable **spmPreview** in the universal extensibility schema:

```json
{
  "buildConfigurations": {
    "spmPreview": true
  }
}
```

## Impact

The iOS app package can't be generated.

## Recommended action

Check the build logs to identify the incompatible plugins. Then choose one of the following options:

* Update all mobile libraries to their latest versions.
* Toggle the **spmPreview** configuration to use a package manager that the incompatible plugins support.
* Look for alternative mobile libraries (Forge components) that all support the same package manager.
* Contact the plugin maintainers to add support for the missing package manager.
* If you own the plugins, add support for the missing package manager. Otherwise, fork the plugins and modify them.
* If they aren't required, remove the affected mobile libraries from your app, or remove the incompatible plugins from the mobile libraries that declare them.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PRJ-40003).
