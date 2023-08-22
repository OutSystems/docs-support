---
summary: "Cannot change the type of an existing attribute: <Name> (<Id>)."
tags:
locale: en-us
guid: a1b0c984-7839-4f47-bf99-ee63d2d2ae1f
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# OS-WFBL-CONF-00003

## Error message

`Cannot change the type of an existing attribute: <Name> (<Id>).`

## Cause

This error occurs when you try to change the data type of a field (attribute) that is already published.
The &lt;Name&gt; and &lt;Id&gt; includes information about the cause of the error.

## Impact

Workflow Builder can't save the application field because you can't change the data type. 

## Recommended action

To change the data type of a field, create a new field with the desired data type.
