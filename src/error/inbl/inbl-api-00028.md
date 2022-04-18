---
summary: The connection was updated locally, but we could not update the connection on the Microsoft's servers. You'll need to access Microsoft Azure Active Diretory if you want to update it manually. Error details <Message>
tags:
locale: en-us
guid: 6d91e880-d57f-4e9d-ae72-ba3d0181f4f1
app_type: traditional web apps, mobile apps, reactive web apps
---

# OS-INBL-API-00028

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
