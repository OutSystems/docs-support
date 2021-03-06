---
summary: Cannot decrease the Length of an existing attribute: <Name> (<Id>).
tags:
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
