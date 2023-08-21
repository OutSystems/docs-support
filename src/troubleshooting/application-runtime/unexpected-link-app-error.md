---
summary: 
locale: en-us
guid: 19528074-d51e-434c-bbce-ccfde080c48e
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=3327:408
---

# Unexpected link in application - changes from HTTPS to HTTP or shows an internal server name

## Symptoms

In an application built with the OutSystems Platform, links don't behave consistently. Most links work as expected, and you are able to navigate the application through those.

However, some of the links in the application misbehave. Some of the possible misbehaviors observed:

* protocol changes from HTTPS to HTTP (no longer secure)

* the hostname of the URL changes (e.g. you were accessing with [http://www.mycompany.local](http://www.mycompany.local/) and you find a link that sends you to [http://srv09123.mycompanydomain.local](http://srv09123.mycompanydomain.local/)

Typically, this type of problem happens in the production environment but not in other (earlier) staging environments (development, test, etc).

Additionally, in the affected environment(s), the problem will typically not happen if accessing the application in a browser running locally in the server, by accessing with [http://127.0.0.1/](http://127.0.0.1/) . 

## Cause

This type of problems typically happens when the environment has a network layer (a load balancer or a reverse proxy) between the end-user and the OutSystems Platform. In this scenario, if these layers are not properly configured, it may be sending wrong information to the platform.

OutSystems Platform usually generates "relative" links: links to other pages are inserted in the code relative to the current path. Examples:

* ./NextScreen.aspx

* ./img/logo.png

* /MyWidgets/SomeFancyJavascript.js

In some situations, however, the platform needs to generate absolute URL. In those situations, URL are generated based on the information received in the front-end. Particularly, the following are inferred from the request that arrives at the application server:

* The protocol (HTTP or HTTPS)

* The hostname (via the Host header in the HTTP request).

If a network layer is not properly configured to pass this information correctly to the target server, the misbehaviors indicated under Symptoms may occur.

## Resolution

Solving this problem is done as indicated below.

**a) HTTPS/HTTP issue**

Either one of the following:

* doing a full pass-through of protocol (meaning: requests initiated by the end-user as HTTPS need to be delivered to the OutSystems application server as HTTPS; same thing for HTTP)

* Configuring the platform for properly setting up the [HTTPS to HTTP offload](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Using_OutSystems_in_Reverse_Proxy_Scenarios/03_OutSystems_configurations_in_reverse_proxy_scenarios#C_-_End-to-end_SSL_and_SSL_Offloading).

**b) wrong hostname**

Configure the network layer to pass the original host header all the way through until the application server.

## More information

Refer to the following contents for more information on the subject:

* [https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/OutSystems_Platform_in_Reverse_Proxy_scenarios](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Using_OutSystems_in_Reverse_Proxy_Scenarios)

* [https://www.outsystems.com/forums/discussion/5684/configuring-a-microsoft-isa-server-to-serve-agile-platform-web-applications/](https://www.outsystems.com/forums/discussion/5684/configuring-a-microsoft-isa-server-to-serve-agile-platform-web-applications/)

## Properties

Applies to OutSystems Platform, all stacks.

Applies to version 8.0.x.x and above (last reviewed under 9.1.600.0).

