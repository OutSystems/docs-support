---
summary: We're sorry, but this database isn't supported.
tags: database compatibility, error handling, case management framework, system requirements, platform version
locale: en-us
guid: d22ff22b-2cf5-43e8-baf9-26a28ea489dd
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - platform administrators
  - backend developers
  - full stack developers
outsystems-tools:
  - case management framework
coverage-type:
  - unblock
---

# OS-CMFR-GEN-00011

## Error message

`We're sorry, but this database isn't supported.`

## Cause

While trying to execute an action that requires an advance query, the Case Management framework detected that the database of the environment isn't supported.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

The platform databases supported by the Case Management framework are:

* Microsoft SQL Server
* Oracle Database

## More info

For information on supported databases, see [OutSystems system requirements](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems/OutSystems_system_requirements).
