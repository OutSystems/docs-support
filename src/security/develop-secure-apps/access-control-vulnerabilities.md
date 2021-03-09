---
summary: Ensure the users of your OutSystems apps only see and do what they are allowed to.
tags: protecting-outsystems-applications; outsystems-security; outsystems-secure-applications; outsystems-access-control; outsystems-permissions-vulnerabilities
en_title: 03 Protecting OutSystems apps from Access Control Permissions vulnerabilities
---

# Protecting OutSystems apps from access control / permissions vulnerabilities

Access Control is about making sure that only the people who are supposed to do/see something are able to.

You can grant user/role permissions to:

* Perform actions. For example, adding a user or deleting an asset.
* See information. For example, payroll data or health records.

## How to do it with OutSystems Platform 

The following sections describe the recommended actions to deal with common access control use cases with OutSystems Platform:

### Protecting Actions

|Use case    |Actions    |
|------------|-----------|
|Disable action from UI |**Avoid disabling actions from the UI**. Disabling a widget in the UI doesn't prevent the sensitive action code to be run by forcing or forging the POST request. |
|Hide action from UI    |**Avoid hiding actions from the UI**. Action is still available on the page. Hiding a widget in the UI doesn't prevent the sensitive action code to be run by forcing or forging the POST request. |
|Validate based on **Preparation** check    |**Avoid performing validations only in Preparation**.  If using old page or screen values (for example, having a second tab open, or in case the user clicks the back button on the browser), the server must validate if the actions can still apply instead of relying on information calculated in the Preparation |
|Implement a page for a role    |Tailor a page with actions available for that role.    |
|Check permissions in action    |Before executing any code, check if the current session has permissions to do it. |
|Set IDs    |Use non-guessable IDs.  |

### Protecting Information

|Use case    |Actions    |
|------------|-----------|
|Display information on screens |Check in **Preparation** if current user is allowed to view this information.  |


## More information 

To learn how to protect your OutSystems apps against other common types of attacks, check [how the OutSystems Platform helps you develop secure applications](intro.md).