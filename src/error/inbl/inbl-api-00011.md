---
summary: Environment <Hostname> isn't authorized to access the Integration Builder. Contact OutSystems Support to confirm its authorization.
tags:
locale: en-us
guid: 5bda389f-0bd2-414f-a770-895181227675
---

# OS-INBL-API-00011

## Error message

`Environment <Hostname> isn't authorized to access the Integration Builder. Contact OutSystems Support to confirm its authorization.`

## Cause

The &lt;Hostname&gt; environment isn't registered in Integration Builder.
For security reasons, the Integration Builder APIs only accept requests from registered environments.
    
## Impact

Integration Manager can't create connections for integrations, and it can't redirect you to Integration Builder.

## Recommended action

In Integration Builder, go to **Settings** > **Environment setup**, and add the &lt;Hostname&gt; environment.
