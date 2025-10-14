---
summary: Explore timeout management and settings in OutSystems 11 (O11) for efficient application performance.
locale: en-us
guid: 6663ad0f-9ee9-4a61-8d03-e8fa4e21b052
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
tags: performance optimization, error handling, database management
audience:
  - mobile developers
  - frontend developers
  - full stack developers
outsystems-tools:
  - service studio
coverage-type:
  - unblock
---

# Timeouts under the hood

This article describes the different types of timeouts that can occur during the runtime or development of an OutSystems application (Reactive Web, Mobile and Traditional Web). Understand how different timeouts are triggered, how to identify them in the Error Logs, and all configurations that can be made to fine-tune them.

## About timeouts

The OutSystems platform is composed of interconnected web application servers, databases, external integrations, and others. These components communicate with each others and the connections should have their own timeouts.

For example, if a query exceeds the execution timeout in the database, the server request waiting for its result will receive a timeout error. Another example is when a request executing on the server is waiting for the response of an external integration for more than a specified timeout limit.

Reactive Web apps and Mobile apps behave in an asynchronous way, where the client-side running on the browser or native operating system performs several different asynchronous requests to the server. To protect the apps from slow server performance or other events that may make the responses slower, these contain a definition for the maximum time the client side can wait for a response from the server before aborting the request.

Regarding development level timeouts you can experience timeouts during the deployment of a module, such as when uploading or downloading modules.

The following sections describe the most common timeouts that can occur while using or developing OutSystems applications.

<div class="info" markdown="1">

See [Sessions in Traditional Web apps](https://www.outsystems.com/tk/redirect?g=a6784b12-4617-437f-b5e5-ec8c8b579006) and [Configure App Authentication](https://www.outsystems.com/tk/redirect?g=74fffe9e-d6fa-4ea9-a8ae-aa7a34a37511) for more details about sessions and session timeouts.  

</div>

## SQL query timeout

Being supported by a database backbone (either Microsoft SQL, Oracle or MySQL) in nature, this is the most common timeout event that can occur in the OutSystems Platform and their applications, specially in low performance database servers or large data volume environments.

The SQL Query timeout defines the maximum amount of time that an SQL statement can take to be fully executed by the database engine, and the resulting dataset be returned to the calling application. It influences OutSystems applications Aggregates and Advanced SQL, as well as the entity actions (CRUD). It also influences the OutSystems Platform system queries, that exist in LifeTime, System Components, and other OutSystems Services.

### Timeout symptoms

When this timeout value is reached you usually get a runtime error either in the applications or during deployment procedures, and a logged Error entry in Service Center. The log entry, shows for the most part the following:

```
Message: 
Error executing query. Error in advanced query MyAdvancedSQL in Preparation in WebScreen1 in MainFlow in MyApp (SELECT ...): Execution Timeout Expired.  The timeout period elapsed prior to completion of the operation or the server is not responding.

Stack:
Error executing query.
   at ssMyApp.Flows.FlowMainFlow.ScrnWebScreen1.FuncssPreparation.QueryMyAdvancedSQL(...)
   at ssMyApp.Flows.FlowMainFlow.ScrnWebScreen1.Preparation(...)
   at ssMyApp.Flows.FlowMainFlow.ScrnWebScreen1.Page_Load(...)
   at System.Web.UI.Control.OnLoad(...)
   at System.Web.UI.Control.LoadRecursive()
   at System.Web.UI.Page.ProcessRequestMain(...)

```

In this case, an Advanced SQL called MyAdvancedSQL timed out in the preparation of a Traditional Web screen.

### Timeout setting

For the application Aggregates and Advanced SQL, it is possible to specify a timeout value in seconds individually. When these queries do not have a timeout value specified, they take into account the platform wide Default Query Timeout instead. Additionally, any system query from LifeTime, System Components, or even low level underlying components such as OutSystems Services, also takes this default value as the timeout. The entity actions (CRUD) and the OutSystems Platform system queries do not have a timeout value definition that can be changed individually and follow a platform-wide Default Query Timeout.

This Default Query Timeout can be specified on the [Configuration Tool](https://www.outsystems.com/tk/redirect?g=3ccedde9-7f7c-4d04-8992-703b00953c15), by going to the Advanced Settings of the Platform tab. By default it is defined with 30 seconds. Note that changing this value will influence the timeout value for all non-application queries and the change must be sustained by a clear reason. There is also one last setting called Database Update Query Timeout that will only affect the default time for database updates to run when 1-Click publishing and is set to 600 seconds by default.

<div class="info" markdown="1">

The default query timeout setting mentioned above does not apply to OutSystems Cloud customers. Cloud customers may observe different timeout values.

</div>

## Application request timeout

Every web request done to an OutSystems application takes its time to process by the application server (IIS) and is ruled by a Request Timeout that prevents the existence of everlasting web requests. So basically, when a web request is taking too long to process and reaches the defined request timeout, the thread that's running it will be abruptly interrupted, generating a runtime error and avoiding waste of resources.

### Timeout symptoms

This error can occur practically anywhere during the execution of the application request. If one is accessing a particular screen and this takes longer that the specified request timeout to execute, the IIS can abort its execution in any of its lifecycle stages. So, you can see an error message associated with a query, an extension, integration, some part of the logic, etc.

These runtime errors are logged in Service Center, under the Error Logs page. In ASP.NET, the message _Thread was being aborted_ is the common way of logging this timeout event. Sometimes one can also idenfify the message _Request timed out_ right after the previous error. For example, the following error stack is caused by a web request timeout event that occurred right when a SQL query was being executed:

```
Message:
Error in advanced query GetOldProducers in Espace_UpdateCache_OldProducersRefs (SELECT ... ): Thread was being aborted.

Stack: 
Thread was being aborted.
   at ssServiceCenter.Flows.FlowOperations_eSpace.ScrneSpace_Publish_Logic_Go.Preparation(...) 
   at ssServiceCenter.Flows.FlowOperations_eSpace.ScrneSpace_Publish_Logic_Go.Page_Load(...) 
   at System.Web.UI.Control.OnLoad(...) 
   at System.Web.UI.Control.LoadRecursive() 
   at System.Web.UI.Page.ProcessRequestMain()
```

Below is another example when the timeout event occured during a extension method invocation:

```
Message: 
Thread was being aborted.

Stack: 
Thread was being aborted.
   at OutSystems.NssOMLProcessor.CssOMLProcessor.MssCompileeSpaceAsync(...) 
   at ssServiceCenter.RssExtensionOMLProcessor.MssCompileeSpaceAsync(...) 
   at ssServiceCenter.Actions.ssCompileFlow3004763(...) 
   at ssServiceCenter.WebServices.ServiceStudio.Compile(...) 
```

### Timeout setting

This timeout event value is defined in the machine.config file under the **httpRuntime** section, with the parameter **executionTimeout**. By default, this value is not set and it will default to 110 seconds. In the [OutSystems installation checklist](https://www.outsystems.com/downloads/search/Platform-Server/), you'll find the instructions for setting the executionTimeout for your application server (notice that this can't be modified in Cloud environments).

But the IIS default timeout value can also be changed during the execution of the requests with [SetRequestTimeout](https://success.outsystems.com/documentation/11/reference/outsystems_apis/httprequesthandler_api/#SetRequestTimeout). This method can be placed in the begining of a Server Action to inform IIS that the request being executed will timeout after the value you've defined.

## Web Service request timeout

When integrating with external APIs (SOAP or REST), the OutSystems applications can invoke methods remotely through web services. The web service itself will also have a invocation timeout event. This timeout event defines the total elapsed amount of time since the web service invocation until the complete reception of its response.

### Timeout symptoms

In an OutSystems application, if calling a Web Service action doesn't produce a response before the specified timeout, it may generate the following timeout error:

```
Message: 
The operation has timed out

Stack: 
The operation has timed out
   at ssMyApp.CcMyRestAPI.ActionMyMethod(...)
   at ssMyApp.Flows.FlowMainFlow.ScrnWebScreen1.CommandOk(...)
   at ssMyApp.Flows.FlowMainFlow.ScrnWebScreen1.wt10_Click(...)
   at System.Web.UI.WebControls.Button.OnClick(...)
   at System.Web.UI.WebControls.Button.RaisePostBackEvent(...)
   at OutSystems.HubEdition.WebWidgets.Button.RaisePostBackEvent(...)
   at System.Web.UI.Page.ProcessRequestMain(...)
```

In this case, one clicked a button that invoked the endpoint MyMethod from the API MyRestAPI and this didn't provide an answer before the Timeout in Seconds defined for the method.

### Timeout setting

Upon adding your Web Reference to the eSpace in the Integrations section, for each method you can define the **Timeout in Seconds_** property. This specifies the maximum time value in seconds that the web service method invocation can take, prior to issue a timeout event.

## Service actions timeout

Communication with Service Actions is similar to a REST Consume. Underneath, it uses REST over HTTP, which means there's a client initiating a request and a server responding to that request. However, unlike typical REST services hosted on IIS, Service Actions do not follow the IIS timeout configuration. Although IIS may have a default timeout of 110 seconds, Service Actions are not governed by this setting.

### Timeout symptoms

After 100 seconds have passed without a response, the connection with the Service Action will abort the connection and log the following entry in the error logs:

```
Message: 
The request was aborted: The operation has timed out.

Stack: 
The request was aborted: The operation has timed out.
   at ssMyApp.RsseSpaceMyApp2.MyApp2ServiceAPIClients.ServiceAction1(...)
   at ssMyApp.RsseSpaceMyApp2.ServiceAction1(...)
   at ssMyApp.Flows.FlowMainFlow.ScrnWebScreen1.CommandOk(...)
   at ssMyApp.Flows.FlowMainFlow.ScrnWebScreen1.wt10_Click(...)
   at System.Web.UI.WebControls.Button.OnClick(EventArgs e)
   at System.Web.UI.WebControls.Button.RaisePostBackEvent(...)
   at OutSystems.HubEdition.WebWidgets.Button.RaisePostBackEvent(...)
   at System.Web.UI.Page.ProcessRequestMain(...)

```

In this case, a screen in the module MyApp invokes a Service Action in a producer module MyApp2 through a click on a button.

### Timeout setting

Contrary to Server Actions, Service Actions execute through internal REST calls between modules, and therefore are not in-process like Server Actions. These internal REST calls do not respect IIS timeout settings, nor are they limited by any server-side timeout.

However, on the client side, the platform has a default timeout of 100 seconds for waiting for a Service Action’s response. This is not configurable and is the actual source of the timeout behavior observed in logs.

Using [SetRequestTimeout](https://success.outsystems.com/documentation/11/reference/outsystems_apis/httprequesthandler_api/#SetRequestTimeout) before invoking a Service Action will not affect the Service Action’s execution time. It only defines how long the caller will wait before timing out. Therefore, if the Service Action does not respond within 100 seconds, the operation will fail regardless of SetRequestTimeout.

In contrast, Server Actions are executed within the same module context, without HTTP communication. This allows SetRequestTimeout to effectively define how long the logic should run before timing out, since it's managing in-process behavior.

In summary, Service Actions have a client-side timeout of 100 seconds, which cannot be extended. To avoid timeouts, consider breaking down the logic or data processing into smaller chunks and invoking them iteratively.

## Server request timeout

On mobile and reactive apps, the client side of the applications perform multiple asynchronous requests to the servers through Data Actions, Server Actions, and Aggregates. To protect the apps from slow server requests, Server Request Timeout is set to 10 seconds by default on the Modules. This means that if a server request does not reply within 10 seconds, the application triggers a Communication Exception.

The requests are aborted by the client but not on the server and will continue executing on IIS.

### Timeout symptoms

The most common symptom is when a Communication Exception is thrown on the apps, sometimes displaying a red error popup to the user saying _The Connection has timed out_. On the logs, an error will be logged for the exact request that caused the timeout (this improvement was introduced in PS 11.21.0):

```
Error Message:
The Connection has timed out

Stack:
Source Name: DataActionDataAction1
Endpoint: screenservices/MyReactiveApp/MainFlow/Screen1/DataActionDataAction1
 CommunicationException: The connection has timed out
    at request.onTimeout (...)
    at https://mydomain/MyReactiveApp/scripts/OutSystems.js
```

In this case, a Data Action from Screen1 did not reply within the defined Server Request Timeout value.

### Timeout setting

Server Request Timeout can be configured on the module Default properties, which will make all Data Actions, Server Actions, and Aggregates inherit the value. But this value can also be defined for each of these components individually, overriding the global value.

## Timers timeout

Timers are OutSystems applications' synchronous jobs that execute a specified application logic on scheduled instants, invoked by the OutSystems Scheduler Service. The timer's timeout event occurs when the elapsed time since the timer's invocation and its completion surpasses the specified value.

### Timeout symptoms

When a timer reaches its timeout settings, an error log will be registered in the Error Logs page of Service Center with an error message and error stack similar to:

```
Message: 
Error executing request http://127.0.0.1/TesteSpace/timerhandler.asmx for Timer Send_Messages. Request duration = 1439 secs. [Marked as 'not running'. Computed next run.]

Stack: 
System.Net.WebException: The operation has timed-out.
   at System.Web.Services.Protocols.WebClientProtocol.GetWebResponse(...)
   at System.Web.Services.Protocols.HttpWebClientProtocol.GetWebResponse(...)
   at System.Web.Services.Protocols.SoapHttpClientProtocol.Invoke(...)
   at OutSystems.HubEdition.RuntimePlatform.TimerHandler.ExecuteTimer(...)
   at OutSystems.HubEdition.Scheduler.Scheduler.ExecuteJob(...)
```

Since it's the OutSystems Scheduler Service that invokes the timer of the application to run, it will also catch the error exception associated with the timeout event occurrence, which will abort the timer's execution. In this case, the timer execution took 1439 seconds, before being aborted.

### Timeout setting

For each one of timers, its possible to specify the _Timeout in Minutes_ property. This value is the maximum elapsed period of time that the OutSystems Platform has to completely execute the action associated with the timer. For more information on how timers are handled by the OutSystems platform please check [Timers documentation](https://www.outsystems.com/tk/redirect?g=7b104f5a-3077-4eab-9dd0-90c28ade4b67).

## Email sending timeout

The OutSystems platform allows to send emails directly form your OutSystems applications. The email sending process is done in two steps:

1. In the first step, the email is rendered and added to a queue. Rendering involves a special web request to a specific endpoint that renders the "web page" with the email content. This content is then stored to the database. This request is made synchronously in the logic that sends the email.
For example, if you send an email with the click of a button in a page, the email is rendered and queued before the page returns.

1. In the second step, Scheduler service picks emails from the queue and sends them to the server using the SMTP configurations in the server.

The first step is managed by a timeout while rendering the page to send by email, and when the page takes too long to render, it may affect the ability of your application to send that email.

### Timeout symptoms

When the timeout value is reached, you get an error message like this:

```
Error creating Email. The operation has timed out
   at System.Net.HttpWebRequest.GetResponse()
   at OutSystems.HubEdition.RuntimePlatform.Email.EmailHelper.HttpGetContent(...)
   at OutSystems.HubEdition.RuntimePlatform.Email.EmailHelper.HttpPost(...)
   at OutSystems.HubEdition.RuntimePlatform.Email.EmailProcessor.SendEmailRequest(...)
   at OutSystems.HubEdition.RuntimePlatform.Email.EmailProcessor.SendEmailRequest(...)
   at ssUserManagement.Flows.FlowMain.ScrnListUsers.CommandResetPassword(...)
```

### Timeout setting

When the email being sent is taking too long to render, you need to reduce the time it takes to render the email because there's no timeout setting that you can configure to overcome the limitation of the page rendering process of the email engine.

Note that resorting to HTTPRequestHander.SetRequestTimeout to extend the duration of email processing won't have any effect. The timeout is not related to the length of the request to render the email. Instead, the limit is in the method that calls the email (_OutSystems.HubEdition.RuntimePlatform.Email.EmailHelper.HttpGetContent_) is limited in time to ensure best practices.

In a simplified way, it's the caller that is not waiting long enough for the request to be ready. The solution, is to reduce the time it takes to render the page.
