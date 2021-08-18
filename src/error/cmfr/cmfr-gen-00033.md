---
summary: Case Definition with the Id <case-definition-identifier-value> can't be purged. Change the PurgeTypeId to allow it.
tags:
---

# OS-CMFR-GEN-00033

## Error message

`Case Definition with the Id <case-definition-identifier-value> can't be purged. Change the PurgeTypeId to allow it.`

## Cause

While trying to execute the **CaseDefinition_Purge** action, the Case Management framework detected that the case definition passed as input doesn't have a purge type defined.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Update the case definition record with the selected purge type. You can do this by calling the **CaseDefinition_Update** action from the **CaseConfigurations_API** or by filling in the missing attributes in your **Bootstrap/Setup** input structures. You can change these attributes:

* PurgeTypeId
* DaysToPurgeCase
* DaysToPurgeProcess
