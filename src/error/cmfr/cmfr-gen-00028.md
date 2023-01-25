---
summary: There was an error processing this rule expression. <data-type> can't be compared with <data-type>.
tags:
locale: en-us
guid: 4acd4a8a-495d-4293-a460-592fc35e4cee
app_type: traditional web apps, mobile apps, reactive web apps
---

# OS-CMFR-GEN-00028

## Error message

`There was an error processing this rule expression. <data-type> can't be compared with <data-type>.`

## Cause

While trying to execute a rule, the Case Management framework detected that the rule expression was trying to compare two data types that can't be compared.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Rewrite the rule and make sure the rule's left and right attribute data types are comparable.
