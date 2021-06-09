---
summary:
tags:
en_title: OS-INBL-API-00008
---

# OS-INBL-API-00008 - No integration was found for the "Key" with 'value'.

## Error message

`No integration was found for the "Key" with <value>.`

## Cause

The key of the integration doesn't exist in Integration Builder
This usually means that the integration was deleted. Otherwise, it means that the key used in the API call is incorrect.

## Impact

You can't assign a connection to this integration in Integration Manager.

## Recommended action

In Integration Builder, refresh the integration list and check if the integration still exists.
If the integration still exists, create a case with [OutSystems support](https://success.outsystems.com/Support).
Otherwise, recreate the integration before assigning a connection.
