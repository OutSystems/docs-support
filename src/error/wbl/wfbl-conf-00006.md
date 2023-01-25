---
summary: Cannot create new dropdown entry. Id is invalid for dropdown: <Name> (<Id>).
tags:
locale: en-us
guid: e9af2193-372d-4ef0-be22-85d20a7cb626
app_type: traditional web apps, mobile apps, reactive web apps
---

# OS-WFBL-CONF-00006

## Error message

`Cannot create new dropdown entry. Id is invalid for dropdown: <Name> (<Id>).`

## Cause

This error occurs when you try to create or update a field of Dropdown type that has inconsistent data.
The &lt;Name&gt; and &lt;Id&gt; indicates which field has the error. 

## Impact

Workflow Builder can't save the field of type Dropdown because of inconsistencies.

## Recommended action

If the field hasn't been published, try to delete it and create a new one of the same type. Otherwise, create a case with [OutSystems support](https://success.outsystems.com/Support).
