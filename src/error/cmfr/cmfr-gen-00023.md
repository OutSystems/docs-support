---
summary: We couldn't find <record> with the Id <identifier-value>.
tags:
locale: en-us
guid: 4a75fcf7-e46b-4bae-8ecb-74d0a1e4883c
---

# OS-CMFR-GEN-00023

## Error message

`We couldn't find <record> with the Id <identifier-value>.`

## Cause

While executing a create or update action, the Case Management framework wasn't able to find the record that the identifier passed as the input reference.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
