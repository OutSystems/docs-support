---
summary: We couldn't retrieve the record <case-identifier> of object <entity-name>.
tags:
---

# OS-CMFR-GEN-00015

## Error message

`We couldn't retrieve the record <case-identifier> of object <entity-name>.`

## Cause

While trying to execute the **Email_ProcessPlaceholders** or the **Email_Send** actions, the Case Management framework wasn't able to find the record inside the &lt;entity-name&gt; entity that matched the &lt;case-identifier&gt;.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the values that are being passed as input to the Case Management framework action are correct. Use Service Studio's Debugger to check the input parameter's value at the time of execution.
