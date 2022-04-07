---
summary: The expected rule output type does not match this rule type.
tags:
locale: en-us
guid: 2229f515-fe18-40a9-a982-092610638934
---

# OS-CMFR-GEN-00030

## Error message

`The expected rule output type does not match this rule type.`

## Cause

While trying to execute a rule, the Case Management framework detected that the rule output type passed as input doesn't match the output type that's configured.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Make sure that the **RuleTypeId** input value matches the configured rule type. Use the **Rule_CreateOrUpdate** action from the **CaseConfigurations_API** module if you need to change the type.
