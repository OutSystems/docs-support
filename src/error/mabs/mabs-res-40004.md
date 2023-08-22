---
summary: Couldn't generate your app because the connection timed out. If the problem persists, check our documentation for more information.
tags:
guid: 6837f7d5-defe-42c9-b1e9-19253bf2fc7c
locale: en-us
app_type: mobile apps
platform-version: o11, odc
figma:
---

# OS-MABS-RES-40004

## Error message

`Couldn't generate your app because the connection timed out. If the problem persists, check our documentation for more information.`

## Cause

This error occurs when MABS timed out while waiting for the needed resources to build the application.

This might be cause by the platform not sending the necessary resources to MABS or MABS not being able to access the resources.

## Impact

Users can't generate the application package.

## Recommended action

Check the build logs on Service Center for more details about the error. Then, try to generate your application again.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-RES-40004).
