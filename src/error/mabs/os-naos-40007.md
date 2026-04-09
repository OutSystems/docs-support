---
summary: Secret for <resource-type> '<resource-name>' cannot be empty
tags:
guid: fdc5bbb9-327b-4390-b903-752dfce7f560
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-NAOS-40007

## Error message

`Secret for <resource-type> '<resource-name>' cannot be empty`

## Cause

An attempt was made to save an empty string as the value to a secret and mandatory extensibility setting or a secret and mandatory mobile configuration during new package creation.

## Impact

### While updating an extensibility setting

The extensibility setting cannot be updated.

### While defining mobile configuration for new package creation

Package creation cannot begin.

## Recommended action

Provide a valid value for the extensibility setting or mobile configuration.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-NAOS-40007).
