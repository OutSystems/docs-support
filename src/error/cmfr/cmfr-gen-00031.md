---
summary: This rule isn't configured or doesn't exist.
tags:
---

# OS-CMFR-GEN-00031

## Error message

`This rule isn't configured or doesn't exist.`

## Cause

While trying to execute a rule, the Case Management framework detected that the rule isn't configured or doesn't exist.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure that the rule is configured before executing the action. Use the **RuleGroup_CreateOrUpdate** action from the **CaseConfigurations_API** module to configure the rule.
