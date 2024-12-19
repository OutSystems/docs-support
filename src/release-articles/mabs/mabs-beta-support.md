---
summary: The OutSystems policy for supporting new versions of mobile operating systems, and the new SDK versions from Android and iOS.
locale: en-us
guid: 6201ced2-dd45-4d61-96af-714f4f170512
app_type: mobile apps
platform-version: o11, odc
---

# Support for new mobile operating system versions

## What OutSystems does for you

OutSystems supports new operating system versions as soon as they're released, which usually happens around September for Android and iOS.

To take advantage of new functionalities released with new operating system versions, OutSystems releases a new **major version** of the Mobile Application Build Service (MABS). From then on, the new SDKs from Google and Apple are available on the latest Major MABS version.

This generally means that customers may need to generate their mobile apps with the new MABS version. In some cases, using a different MABS version may also require an upgrade of the Platform Server (O11). For more information about the MABS versions, refer to [Mobile Apps Build Service Versions](mabs-versions.md).


With a new major versions of MABS OutSystems supports:

* Runtime primitives of the platform i.e., widgets, with the goal of finding and correcting misbehaving primitives.

* Supported Forge components, with the goal of testing and fixing misbehaving components

OutSystems releases the required updates for both runtime primitives and Forge components ahead of the new operating system release. New SDKs become mandatory for publishing mobile apps on the iOS AppStore and Google Play.

## What OutSystems needs from you

Customers play a part in supporting upcoming versions of mobile operating systems and new SDKs. Mobile apps have the following aspects that require customer attention:

* **Interaction with custom plugins (non-supported)**. Each plugin behaves in a way that can interfere with other plugins, and those interferences may change with the mobile operating system version and the new SDKs. OutSystems guarantees that Supported Plugins are fully compatible with the latest SDKs, but it's the customer's responsibility to test their app and identify misbehaving interactions for non-supported Plugins/Assets.

* **Customer-owned plugins**. While OutSystems makes an effort to facilitate all types of integrations, OutSystems can't test non-supported plugins extensively. However, OutSystems user forums provide a good resource for information about the required changes.

OutSystems strongly recommends that customers begin testing their apps with the first official public previews of upcoming versions of mobile operating systems. After the release of the first public previews OutSystems begins accepting support requests from customers. However, due to the instability of Beta version operating systems, OutSystems can't guarantee a stable mobile offer over those Beta versions.

OutSystems also strongly recommends that customers begin testing their apps with the new SDKs as soon as OutSystems releases a new MABS major version. OutSystems begins accepting customer support requests from that moment. OutSystems assigns the severity levels of those requests according to the MABS version (Beta or stable).

