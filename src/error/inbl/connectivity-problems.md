---
summary: Connectivity problems with Integration Builder or Workflow Builder
tags: connectivity issues, environment configuration, network requirements, error handling, access troubleshooting
helpids: 30403
locale: en-us
guid: 2d4d101e-fdac-4eab-a7a1-b1fbe4a4b742
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - platform administrators
  - full stack developers
  - infrastructure managers
outsystems-tools:
  - experience builder
  - workflow builder
  - integration builder
coverage-type:
  - unblock
---

# Integration - Workflow Builder cannot connect to your environment


## Error message

`We were unable to reach your environment and we couldn't sign you into <Integration/Workflow> Builder. Check here for the solutions.`

## Cause

* There is an error in the environment name
* Integration Builder cannot connect to the environments where you deploy integrations
* Workflow Builder cannot connect to the environment where you want it to publish apps 


## Recommended action

Verify with your IT department that your Integration/Workflow Builder has access to the correct source and destination on your network.

## More info
* [OutSystems network requirements](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems/OutSystems_network_requirements)

