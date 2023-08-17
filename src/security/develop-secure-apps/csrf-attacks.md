---
summary: Prevent attackers from executing malicious instructions on your OutSystems apps from an external site. Cross Site Request Forgery (CSRF) attack protection.
tags: outsystems-security; outsystems-secure-applications
locale: en-us
guid: 888ae7de-2001-459d-894a-e0001aeba86f
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/vTtFn5nl44ZLjUBYo2anCO/Security?node-id=910:240
---

# Protecting OutSystems apps from Cross Site Request Forgery attacks

Cross-site request forgery (CSRF) is a web security vulnerability used to induce users to perform unintended actions. The following example illustrates how a CSRF attack can trick a user, that hasn't logged out from a vulnerable website, into clicking a trap link that executes a script or sends a fake POST request with the user's session ID:

![Example of a CSRF attack](images/csrf-attack-example.png)

With the CSRF method, attackers are able to make requests to your application from another site using, for example:

  * Hidden image performing a GET request
  * Link performing a GET request
  * Malicious form performing a POST request
  * On load actions that perform a POST request

## OutSystems built-in protection

The most robust and generic form of CSRF protection is to perform server-side validation. It consists in including an anti-CSRF token, known as [Token Based Mitigation](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html#token-based-mitigation), within every or relevant requests:

* For traditional web applications the view state is signed with the osVisitor cookie. When performing requests (submit or ajax), the view state signature is matched against the osVisitor. Find the osVisitor definition in [this article](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Cookie_Usage_in_Web_Applications). 
* For reactive web applications the X-CSRFToken is extracted from the nr2<user\> cookie, and sent as a header on following requests. Find detailed information about nr2<user\> in [this article](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Secure_the_Applications/Configure_App_Authentication#Authentication_Cookies).

## How to prevent CSRF attacks when developing APIs

With OutSystems, the development of APIs is entirely in the responsibility of the developer. APIs don't include anti-CSRF tokens by default. To secure your OutSystems APIs against CSRF attacks, we recommend the following actions:

|**Use case** |**Actions** |
|-------------|------------|
|Perform GET requests |<ul><li>**Don't** run actions in the **Preparation**.</li><li>When designing your REST API, **don't** use cookies.</li></ul>|
|Perform POST requests |<ul><li>Make sure there is a [unique token in your request](https://www.outsystems.com/forums/discussion/13556/cross-site-request-forger-token).</li><li>Validate against the expected value in the session.</li></ul>||

## More information 

To learn how to protect your OutSystems apps against other common types of attacks, check [how OutSystems helps you develop secure applications](intro.md).
