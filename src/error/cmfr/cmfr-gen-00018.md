---
summary: You can only have one initial case status.
tags:
locale: en-us
guid: 0f042f7b-b512-4083-abad-80b2fa865680
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# OS-CMFR-GEN-00018

## Error message

`You can only have one initial case status.`

## Cause

While executing one of the **Bootstrap/Setup** actions, the Case Management framework detected that more than one case status record had its **IsInitial** attribute set as **True**. There can only be one case status set as initial for each case definition.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure that only one of the case status records has its **IsInitial** attribute set as **True**.
