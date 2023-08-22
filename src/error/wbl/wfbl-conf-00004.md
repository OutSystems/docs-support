---
summary: "Cannot decrease the Length of an existing attribute: <Name> (<Id>)."
tags:
locale: en-us
guid: 2f1e24e8-0a0e-4d2f-b45f-8f3db0bb127d
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# OS-WFBL-CONF-00004

## Error message

`Cannot decrease the Length of an existing attribute: <Name> (<Id>).`

## Cause

This error occurs when you try to decrease the Length of a Text field (attribute) that is already published.
The &lt;Name&gt; and &lt;Id&gt; indicates the field with the error.

## Impact

Workflow Builder can't save the application field because you can't change the length of the field. 

## Recommended action

Since you can't change the Length of the field, create a new field with the desired text Length.
