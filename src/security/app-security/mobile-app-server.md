---
summary: Mobile apps communicate with the OutSystems Platform Server using secure REST endpoints. In this document, we explain how those endpoints are generated and secured.
---

# Mobile app to server communication and security

In an OutSystems Mobile application, all the communication between the app and the Platform Server is done through REST calls. All the calls to Aggregates/Data Actions and Server Actions in Mobile modules will have REST endpoints generated automatically by the platform.

![Client to server REST calls](images/mobile-app-server-communication.png)

Whenever data is fetched from the server or a Server action needs to run, JavaScript code from the app’s Controller files performs HTTP calls to the generated REST endpoints.

In the case of data fetching, the controller, upon receiving the answer from the contacted REST endpoint, sends the data received to the Model. If this data is being in use by the UI, the View gets alerted and updates it on the screen.

## Security of the endpoints

Security of these REST endpoints is automatically ensured by OutSystems through the use of two approaches:

* All accesses are encrypted
* All accesses are subject to server-side access control

### Encryption 

All communication to OutSystems generated REST endpoints is done over HTTPS and is therefore encrypted. Any attempt to use one of these APIs over HTTP will issue an error on the server side

### Server-side access control 

Access control is done on the server side to make sure no unauthorized accesses are made to the generated REST endpoints. This access control is done using a secure user token that is sent whenever there’s a call to one of these endpoints. For more information about the authorization mechanism for OutSystems mobile apps, check [Configure Mobile App Authentication](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Secure_the_Applications/Configure_App_Authentication).

![Access control](images/mobile-app-server-access-control.png)

OutSystems automatically computes access control for each endpoint based on usage and the security definitions made by the developer.

**Screens** that access the server create endpoints that have the same security permissions as the screen:

* Anonymous screens generate public endpoints.
* Screens that have permissions generate endpoints that validate those same permissions.

**Blocks** that access the server create endpoints that have the minimum set of permissions of the screens that use them:

* If an anonymous screen uses the block it generates a public endpoint.
* If a screen that requires "Manager" permissions uses the block it generates an endpoint that requires "Manager" permission.
* If a screen that requires "Manager" permission and a screen that requires "Employee" use the block it generates an endpoint that requires either "Manager" or "Employee" permission.
* If a screen that requires "Manager" permission and an anonymous screen use the block it generates a public endpoint.

**Global client actions** that access the server create endpoints that have the minimum set of permissions of the screens or blocks that use them.

**Exception handlers defined on UI flows** that access the server create public endpoints. This ensures any user of your application will see the correct information about any error that might occur, even if the user hasn’t logged yet.


**Application Events** (for example, *OnApplicationReady*, *OnApplicationResume*) that access the server create public endpoints. Public endpoints are the best solution since these events often occur before the user has had a chance to log in.


You can customize access control of a particular endpoint. Developers have access to OutSystems built-in functions that can be used to check roles and permissions whenever there's an access to the server. A security exception can then be raised if an unauthorized access is detected.