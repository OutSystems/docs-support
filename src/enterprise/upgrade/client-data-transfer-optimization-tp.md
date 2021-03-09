---
summary: Use the server-to-client data transfer optimization technical preview to reduce the data client apps receive.
tags:
---

# Technical Preview - Server-to-client data transfer optimization

Server-to-client data transfer optimization uses a sophisticated data flow algorithm that analyses how the data flows and then optimizes the transfer from the server to the client. 

## Prerequisites

To have your apps use server-to-client data transfer optimization, as part of a technical preview, you need to meet the following requirements:

* Platform Server 11.10.0 or later.
* LifeTime 11.6.0 or later.
* You activated the [technical preview](https://success.outsystems.com/Support/Enterprise_Customers/Upgrading/Technical_Preview_features) **Client-side optimizations for Reactive Web Apps** or **Client-side optimizations for Mobile Apps** in LifeTime. After you activate or deactivate  the feature, **publish your app** to apply the optimization changes.

With the optimization the apps receive only the information that users of the app really need. You can activate this optimization as a technical preview, to try out the following benefits:

* Performance improvements, due to the reduced amount of data transfer. The improvement is noticeable in data-demanding apps that use complex database joins.
* Improved security, as less data coming to the client reduces the possibility of an accidental data leak.

The optimization works for Screen Aggregates, Data Actions, and for the Server Actions in the logic flows of the Screen Client Actions. You can turn on the optimization for Mobile Apps or Reactive Web Apps, or for both.

## Send feedback

If you experience issues with this technical preview, let us know by posting [a new question with the **technical preview** tag](https://www.outsystems.com/forums/tag/6875/technical-preview/) in Forums.
