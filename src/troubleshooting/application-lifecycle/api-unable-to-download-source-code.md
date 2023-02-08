---
summary: Learn how to troubleshoot if you are unable to download source code from on application.
locale: en-us
guid: 8DD3FD53-11F9-4CE4-9251-BACDA78F7D1C
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# Unable to Download Source Code from one application

## Symptoms
Error downloading the source code package of an application requested for on a specific environment.

## Troubleshooting
When downloading the source code of an application is failing, follow the validations below to troubleshoot a potential issue.

### Check the user has full-control over the application
To validate this requirement

1. In the LifeTime management console of your infrastructure, open the User Management tab and select the Service Accounts sub-menu.
1. Select the service account used on the source code access API by clicking on the service account name
1. Check if the level of permission of the user is Full-Control on the environment you are requesting the source code.

The wrong permissions level returns a message like You need permission to access the environment `{EnvironmentKey}` or the app `{ApplicationKey}`.

### Check the environment has Non-Production purpose
Call the API method that returns the details of the environment

Request `GET /environments/{EnvironmentKey}/`

Response body:

```
{
  "Key": "849515f2-b4ff-4aca-a9d6-9407bea655f4",
  "Name": "Testing",
  "OSVersion": "11.0.110.0",
  "Order": 1,
  "HostName": "prd-env-1.company.com",
  "UseHTTPS": true,
  "EnvironmentType": "NonProduction",
  "NumberOfFrontEnds": 1,
  "ApplicationServerType": ".NET",
  "ApplicationServer": "IIS",
  "DatabaseProvider": "SQLServer",
  "IsCloudEnvironment": false
}
```

Confirm that the Environment you on which you are requesting the source code has the EnvironmentType as NonProduction.

A request to the wrong purpose environment returns the message `Couldn't request the app source code. You can only do it in a non-production environment.`

### Check the environment key exists

Call the API method that returns all the environments registered on your infrastructure

Request: `GET /lifetimeapi/rest/v2/environments/`

Response body:
```
[
  {...},
  {
    "Key": "849515f2-b4ff-4aca-a9d6-9407bea655f4",
    "Name": "Testing",
    "OSVersion": "11.0.110.0",
    "Order": 1,
    "HostName": "prd-env-1.company.com",
    "UseHTTPS": true,
    "EnvironmentType": "Production",
    "NumberOfFrontEnds": 1,
    "ApplicationServerType": ".NET",
    "ApplicationServer": "IIS",
    "DatabaseProvider": "SQLServer",
    "IsCloudEnvironment": false
  },
  {...}
]
```

Check that the Environment Key (**Key**) is the correctly passed to the API call.

If the environment key does not exist the API will return a message like The environment `{EnvironmentKey}` or the app `{ApplicationKey}` doesn't exist.

### Check the application key exists

Call the API method that returns all the applications available on your infrastructure

Request: `GET /lifetimeapi/rest/v2/applications/`

Response body:
```
[
  {...},
  {
    "Key": "c9a7a82e-0eee-4a3d-8e22-2a19c69c766f",
    "Name": "EmployeeBackoffice",
    "Kind": "WebResponsive",
    "Team": "",
    "Description": "",
    "URLPath": "/EmployeeBackoffice",
    "IconHash": "IconHash6a79e71e-c8e5-9e18-115c-cab789517672",
    "IconURL": "/LifeTimeSDK/ApplicationIcon.aspx?ApplicationKey=c9a7a82e-0eee-4a3d-8e22-2a19c69c766f",
    "IsSystem": false,
    "AppStatusInEnvs": []
  },
  {...}
]
```

Check that the Application Key (**Key**) is the correctly passed to the API call.

If the application key does not exist the API will return a message like The environment `{EnvironmentKey}` or the app `{ApplicationKey}` doesn't exist.

## Still having problems?

If the above validations didn't help you to solve the issue and you need further assistance, open a support case to get help from OutSystems Support.
