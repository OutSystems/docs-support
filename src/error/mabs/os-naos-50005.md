---
summary: An error occurred while fetching the extensibility configurations
tags: 
guid: 9592decf-8fae-4e63-8867-3a9c60ff334e
locale: en-us
app_type: mobile apps
platform-version: odc, o11
figma: 
---

# OS-NAOS-50005

## Error Message

`An error occurred while fetching the extensibility configurations.`

## Cause

The system couldn't retrieve the configuration data required for extensibility features. This is often caused by one or more of the following issues:

1. **Malformed Extensibility Configuration JSON**: Missing or invalid properties, such as `key`, `name`, `type`, or `url`.

1. **Missing Extensibility Resources**: Resources specified in the JSON are not accessible or have invalid URLs.

## Impact

The build process depends on the extensibility configurations for key functionality and fails without valid configurations.

## Recommended action

Ensure that the necessary extensibility configurations are available and correctly set up.

If the problem persists, create a case with [OutSystems support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-NAOS-50005).
