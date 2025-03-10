---
summary: This rule isn't configured or doesn't exist.
tags: error handling, case management framework, system rules, configuration, action execution
locale: en-us
guid: ca40e6e0-aca2-4171-9691-ddbf5a4db552
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - backend developers
  - full stack developers
  - architects
  - platform administrators
outsystems-tools:
  - service studio
coverage-type:
  - unblock
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
