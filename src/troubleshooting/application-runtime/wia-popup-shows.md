---
summary:
tags:
locale: en-us
guid: 221907f5-bdfa-4767-916d-6c2fb1769489
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# Windows Integrated Authentication login popup keeps showing for end users

## Symptoms  
You have an application:
- built with the OutSystems Platform
- running on the .NET stack
- using Windows Integrated Authentication (WIA) to authenticate users
- using a browser (Internet Explorer or other) that requires explicit authentication with credentials (rather than sending them silently to the server)

Your users report that, during regular use of the application, the login popup “pops back again”. Your users are using the application normally, without long pause periods between interactions

## Cause 
The cause of this behavior is complex, and is explained by a number of things:

A. The pages being accessed are configured to request WIA - even if the user is also being authenticated by other mechanisms (specifically via OutSystems Platform login)
B. The web-server is regularly requesting re-authentication (at WIA level) to confirm the user is still allowed
C. The browser is configured to require explicit authentication (rather than silently authenticating), meaning that the end-user sees the popup.

The below paragraphs go into details in the above bullets:

### A. The pages being accessed are configured to request WIA 
OutSystems Platform provides an authentication mechanism [1] that allows for access control. This mechanism is session based and means that, after successful authentication, the user continues logged in until either explicitly logging out, or until a timeout occurs (by default 20 minutes of inactivity).
When using WIA with OutSystems applications, WIA should be the mechanism through which people authenticate using the Platform’s mechanism. This means that you should not set all pages in an application to use WIA - instead, all pages must be correctly protected by using Roles [3] to segment access levels, and WIA should be reserved only for the login page.

The problem described in this article happens only if the application is set to use WIA throughout its pages. If only the login pages are set to use WIA, the problem does not manifest.

Note that, in specific cases, it may make sense to have individual pages / web screens set as WIA (e.g. if the app is very small) but it’s not a good practice if it's widespread - for the same reason apps don’t require logging in to each individual page.

As a final note - if someone decided to configure WIA directly in IIS instead of doing it in the eSpace, you may still have pages that require WIA even if they have the Integrated Authentication option turned off in the eSpace.

### B. The web-server is regularly requesting re-authentication (at WIA level) 
In webpages configured to use WIA, IIS [Internet Information Services] requires the browser to authenticate (using NTLM or Negotiate). When accessing pages that require WIA, IIS may request WIA authentication from time to time to ensure the client is still allowed to access - at limit, it may require authentication in each different connection or request.

This is by design in IIS, and can be considered a security feature - to avoid people getting access in shared environments or computers.
Microsoft explains some of these conditions in [2].

So this is not the problem - this is a symptom as well. Proceed to the next section.

### C. The browser is requiring explicit authentication 
Browsers can be configured not to show the credentials popup (and instead send them implicitly). This was the default a while ago (Internet Explorer 3 and 4) but soon turned the other way around for security reasons (e.g. a malicious server could request a client to authenticate and with that process get information on the user’s credentials). It can still be turned on for trusted sites, but it’s something that needs to be done on the client side (the browser) - nothing you can do from the server side. [2] gives some hints at this; most modern browsers (non-IE) also have mechanisms for activating implicit authentication if needed.

## Resolution 
From the Cause section it can be guessed that the resolution to this problem is either:
- Change the app not to request WIA throughout the app (restricting such request to the login pages)
OR
- Change the browser configuration to trust a given server and stop annoying the user.

Change the app not to request WIA throughout the app 
Refer to More Information on how to edit your eSpace to set all screens not to require Integrated Authentication, make proper use of Roles to prevent non-authenticated users to access screens, and ensuring the Security handler correctly sends users to the login page where they can authenticate using WIA.

Change the browser configuration to trust a given server and stop annoying the user 
Refer to [2] on how to do it for Internet Explorer. Other browsers have similar functionality - either thru configuration or extensions / plug-ins.

## More information 
[1] (www.outsystems.com/help/ServiceStudio/9.1/#t=Handling_security%2FAuthenticating_End_Users.htm)
[2] (https://support.microsoft.com/en-us/kb/258063)
[3] (www.outsystems.com/help/ServiceStudio/9.1/#t=Handling_security%2FAbout_Roles.htm)
[4] (www.outsystems.com/help/ServiceStudio/9.1/#t=Handling_security%2FAbout_Integrated_Authentication.htm)
[5] (www.outsystems.com/help/ServiceStudio/9.1/#t=Web_User_Interface%2FWeb_Screen_Properties.htm)
