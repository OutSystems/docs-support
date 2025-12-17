---
summary: Something went wrong while executing your Capacitor Build Actions. Check your build action JSON configurations.
tags: capacitor, build actions, mobile app generation, extensibility, error handling, troubleshooting
guid: a1b2c3d4-e5f6-7890-abcd-ef1234567890
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
audience:
  - mobile developers
  - full stack developers
outsystems-tools:
  - service center
coverage-type:
  - unblock
---

# OS-MABS-ACT-40000

## Error message

`Something went wrong while executing your Capacitor Build Actions. <error_details>`

## Cause

This error occurs when a build action fails to execute during the Capacitor mobile app build process. Build actions use JSON-based configuration files to perform native project modifications such as updating the Android Manifest, Info.plist, or Gradle files. They execute after the `cap sync` command during the build.

Common causes include:

* Invalid JSON syntax in the build action configuration file
* Malformed build action definitions (missing required properties, incorrect structure)
* Invalid file paths or target selectors in the configuration
* Attempting to modify files or nodes that don't exist
* Incorrect variable references or unresolved parameters
* Invalid conditional expressions in conditional build actions
* Merge or inject operations with malformed XML/JSON content
* Invalid Gradle syntax in gradle build actions
* File permission issues when copying or creating files
* Network errors when copying resources from URLs

## Impact

Users can't generate the mobile application package. The build process stops when the build action fails, preventing the app from being compiled and packaged.

## Recommended action

1. Check the build logs on Service Center for detailed error information. The error message contains specific details about what went wrong during the build action execution.

1. Review your build action JSON configuration file:
   * Verify the JSON syntax is valid
   * Ensure all required properties are present for each action
   * Check that file paths are correct and relative to the project root
   * Validate that target selectors (XPath, Gradle targets) correctly identify the elements you want to modify
   * Confirm all variable references match the defined variables

1. Learn more about [Build Actions](https://www.outsystems.com/tk/redirect?g=35892a80-96be-43bf-a89f-8d535b5b6f09).

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-ACT-40000).
