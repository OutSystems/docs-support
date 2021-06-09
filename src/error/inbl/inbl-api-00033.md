---
summary:
tags:
en_title: OS-INBL-API-00030
---

# OS-INBL-API-00030 - The connection was deleted locally, but we could not delete the connection on the Microsoft's servers.

## Error message

`The connection was deleted locally, but we could not delete the connection on the Microsoft's servers. You'll need to access Microsoft Azure Active Diretory if you want to delete it manually. Error details: "<"Message">".`

## Cause

While deleting a connection, Integration Manager failed to delete the matching Application in Microsoft Azure Active Directory (AAD). 
Typically, this means the Application has already been deleted in AAD.

## Impact

Integration Manager can't delete the connection.

## Recommended action

Access Microsoft Azure Active Directory to delete the Application manually if it still exists.

## More info

[What is application management in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/what-is-application-management)

