---
summary: Binary for <resource-type> '<resource-name>' cannot be null or empty
tags:
guid: fad0b7cc-8bf9-45e6-83e1-e0ecbc152620
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-NAOS-40008

## Error message

`Binary file for <resource-type> '<resource-name>' cannot be null or empty`

## Cause

An attempt was made to save an empty file as the value to a mandatory extensibility setting or a mandatory mobile configuration during new package creation.

In this context, an empty file is a file that either has no contents or has contents consisting only of zero bytes.

## Impact

### While updating an extensibility setting

The extensibility setting cannot be updated.

### While defining mobile configuration for new package creation

Package creation cannot begin.

## Recommended action

Replace the empty file with a file that contains data.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-NAOS-40008).
