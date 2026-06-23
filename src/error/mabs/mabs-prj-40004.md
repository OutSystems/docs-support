---
summary: "OS-MABS-PRJ-40004 in OutSystems Developer Cloud (ODC) occurs when a resource declared in extensibility configurations can't be found."
tags:
  - Cordova
  - Extensions
  - iOS
  - Libraries
  - Mobile app
  - Native App
  - Troubleshooting
guid: d729cb4d-e734-4e5f-974c-74c51db42e1d
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

# OS-MABS-PRJ-40004

## Error message

`Resource file <SourcePath> declared in extensibility configurations of <Owner> can't be found.`

## Cause

This error occurs when a resource declared in the extensibility configurations of your app or one of its libraries points to a file that doesn't exist. It typically happens when the source is set to a literal file path. The recommended pattern is to use a placeholder instead.

For example, using Universal Extensibility:

```json
{
  "buildConfigurations": {
    "resources": {
      "ios": [
        { "source": "missing-file.txt", "target": "target/dir/file.txt" }
      ]
    }
  }
}
```

Another example, using Cordova-based Extensibility:

```json
{
  "resources": {
    "ios": {
      "some-id": { "src": "missing-file.txt", "target": "target/dir/file.txt" }
    }
  }
}
```

## Impact

The app package can't be generated.

## Recommended action

Open the extensibility configurations of the **&lt;Owner&gt;** app or library and find the resource entry that references **&lt;SourcePath&gt;**. Then take one of the following actions:

* Update the source to use a placeholder, such as `$images.MyImageName` or `$resources.MyResourceName`.
* If you can't use a placeholder, make sure the literal path points to an existing file.

After fixing the resource declaration, regenerate your app again.

For more information about declaring resources in extensibility configurations, refer to [Extensibility configurations JSON schema](https://success.outsystems.com/documentation/outsystems_developer_cloud/building_apps/mobile_apps/extensibility_configurations_json_schema/).

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-PRJ-40004).
