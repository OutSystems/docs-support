---
summary:
tags:
en_title: OS-INBL-API-00028
---

# OS-INBL-API-00028 - The connection was updated locally, but we could not update the connection on the Microsoft's servers. You'll need to access Microsoft Azure Active Diretory if you want to update it manually. Error details: &lt;Message&gt;

## Error message

`The connection was updated locally, but we could not update the connection on the Microsoft's servers. You'll need to access Microsoft Azure Active Diretory if you want to update it manually. Error details: <Message>`

## Cause

While trying to edit a connection, Integration Manager failed to edit the matching Application in Microsoft Azure Active Directory (AAD). 
The most common cause for this error is that the Application that matches the Connection on AAD has been deleted.

## Impact

Integration Manager can't edit the connection.

## Recommended action

Access Microsoft Azure Active Diretory to update the connection manually if it still exists.<br/>
Alternatively you can delete the connection in Integration Builder and create a new one, if the current connection isn't working.

## More info

[What is application management in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/what-is-application-management)
