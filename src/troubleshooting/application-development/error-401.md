---
summary: This document lists two common reasons that can help you troubleshoot the issue. A 401 error when authentication fails after client request. Message "Install the new app template to start creating Reactive Web apps".
Tags:
locale: en-us
guid: 292ae0af-338c-48d8-be72-b23cc3d84380
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# Unable to create a new app due to 401 error or missing templates

This document provides more information about a network issue that can prevent developers from creating a new app in Service Studio. Platform Server provides available app types to Service Studio through the Template Manager service. In this process, Service Studio needs to provide valid authentication. If that authentication fails, you won't see any app templates and you won't be able to create new apps.

When creating a new app, one of the following happens:

* There are no app templates to create a new app. Instead, there's a message: **Install the new app template to start creating Reactive Web apps.**.
* An error shows, with the text: **The remote server returned error (401) Unauthorized**.

These errors are rare in cloud environments and a typical network configuration on the client side, or in on-premises installations where the installation process followed the installation checklist.

## Network component interfering with the token authorization

A common issue when the developer has a proxy between their computer and the Platform Server **and** the proxy is tampering with the authorization tokens. 

**How to fix**

If a proxy mediates the network communication between the computer and the Platform Server, ensure with your IT department that the proxy doesn't manipulate the authentications headers.

## Basic Authentication configured in the module at the IIS level

Having **Basic Authentication** on the module at the IIS level isn't a supported configuration. IIS has several authentication modes and OutSystems requires that you enable **Anonymous Authentication**. This lets the platform handle the authentication process. Platform Server checks this setting as part of the installation, to ensure it sets up the authentication correctly.

**How to fix**

Check if the IIS settings are correct and ensure **Anonymous Authentication** is on.