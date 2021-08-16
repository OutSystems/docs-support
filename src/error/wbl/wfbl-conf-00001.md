---
summary: Field label cannot be higher than <Max_Length>.
tags:
---

# OS-WFBL-CONF-00001

## Error message

`Field label cannot be higher than <Max_Length>.`

## Cause

This error occurs when trying to create or modify a field label that is longer than allowed.
The &lt;Max_Length&gt; indicates the max length allowed for the label.

## Impact

Workflow Builder can't save the application field because the label is too long.

## Recommended action

Set a label length that's less than or equal to the &gt;Max_Length&lt;.
