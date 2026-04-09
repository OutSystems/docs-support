---
summary: Url to binary for <resource-type> '<resource-name>' cannot be empty
tags:
guid: dd18367c-ed40-4224-b761-2ad6a333744b
locale: en-us
app_type: mobile apps
platform-version: odc
figma:
isautopublish: true
---

# OS-NAOS-40009

## Error message

`Binary file for <resource-type> '<resource-name>' cannot be empty`

## Cause

An attempt was made to save an empty file as the value to a secret and mandatory extensibility setting.

In this context, an empty file is a file that has no contents.

## Impact

The value of the extensibility setting cannot be updated.

## Recommended action

Replace the empty file with a file that contains data.

If the problem persists, create a case with [OutSystems Support](https://www.outsystems.com/support/portal/open-support-case?ErrorCode=OS-MABS-NAOS-40009).
