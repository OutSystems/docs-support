---
summary: Check what type of product releases does OutSystems have and what you can expect from each one. Details about how OutSystems versions are numbered.
tags: 
locale: en-us
guid: d18db4ef-572c-4961-a7aa-097259242aca
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# OutSystems product lifecycle and support calendar

At OutSystems we strive to ensure that our customers can continuously benefit from our latest innovations and features that truly help to speed up the digital transformation processes. With this goal in mind, we've devised a product lifecycle that allows OutSystems to keep our product innovative and up to date with current market trends.

![OutSystems release lifecycle](images/product-lifecycle-diag.png)

Our product may be updated through several types of releases:

* **Major release** - a new major version of the product is announced through extensive marketing campaigns including, press releases, [Product Releases and Updates pages](https://www.outsystems.com/product-updates/), keynote announcements on NextStep and other OutSystems events.

* **Release** -  within for each product major version, we will periodically release new features. OutSystems will inform customers and developers through community digests and social media posts. All customers’ registered users in OutSystems Community are informed of these changes. Additionally, depending on what's being launched, there might be a specific landing page to support the release, release videos and/or blog posts related to the subject. This type of release occurs when new features are added.

* **Cumulative patch** - these are mainly focused on bug fixing but may include minor features. This type of release is usually communicated through release notes published on our website.

## OutSystems version numbers

OutSystems version numbers are a sequence of three numbers, separated by a period, and assigned in ascending order.

The version numbering schema is as follows:

**Major release**.**Release**.**Cumulative patch** **Build**

The several components of the version number are the following:

Major
:   This number identifies the major product version. A new major version is defined in your Subscription Agreement as an "**Upgrade**" or a “**New Software Version**”.

Release
:   This number increases when OutSystems adds functionality to a release in a backward-compatible manner (for example, from Platform Server 11 **.7**.*n*, where *n* is a number, to Platform Server 11 **.8**.0).

Cumulative patch
:   This number increases when OutSystems makes backward-compatible bug fixes or minor improvements in a release (for example, from Development Environment 11.7 **.1** to Development Environment 11.7 **.2**).

Build ID
:   This number identifies a specific build and is unique for each OutSystems component: Development Environment, Platform Server, LifeTime. For example, "Development Environment 11.7.1 **(Build 91)**".

In most situations, the complete version is properly identified by the three first numbers: **Major.Release.Cumulative patch**. However, sometimes, you need to identify a very specific build and, in this case, you should use the three numbers and the build ID.

### Example

The following table illustrates the usage of version numbers in 3 different types of releases:

| Stage | Version number change |
|---|---|
| A Major containing new features and possibly breaking changes. The first number (major product version) increases and the other two numbers are reset to 0. | from **10**.n.nto **11**.0.0 |
| A Release containing new functionality, and possibly breaking changes. The second number increases and the third number is reset to 0. | from 11.**0**.nto 11.**1**.0 |
| A Cumulative patch containing only defect fixes and minor improvements, but with no breaking changes. The third number (patch) increases. | from 11.1.0to 11.1.**1**  |


*n* = an integer number


## Early access programs

Major launches typically include an Early Access Program (EAP). The program duration will depend on the scope of the launch and the specific program objectives. Customers are invited to participate in an EAP, depending on pre-defined eligibility criteria. During the EAP, OutSystems has dedicated resources (Support, Engineering, Training) to enable and support the customer. OutSystems may provide additional infrastructure resources while the program is in place (for example, to run in parallel with the existing infrastructure).


## Installing new releases

### Upgrades to a new major release

Upgrading to a new major release is optional (but recommended) for self-managed customers. For OutSystems Cloud, upgrades can be scheduled and are then performed by the OutSystems Support team. Upgrades in OutSystems Cloud installations will be mandatory once the installed version reaches the end of the support window. In extreme cases, the upgrades may require very small downtimes. Pragmatic instructions for this process are provided in our [documentation](https://success.outsystems.com/Support/Enterprise_Customers/Upgrading/01_Upgrade_OutSystems_Platform). OutSystems can provide [services to assist with the upgrade](https://www.outsystems.com/evaluation-guide/professional-services).

Personal environments and enterprise trials will be upgraded to the latest major release as soon as possible.


### Upgrades to a new release or cumulative patch

Upgrading to a new release or cumulative patch are optional (but recommended) for self-managed customers. OutSystems Cloud installations are handled by our operations with no downtime. Update instructions are available in the [installation checklist](https://www.outsystems.com/Downloads/search/). OutSystems can provide [services to assist with the upgrade](https://www.outsystems.com/evaluation-guide/professional-services).

For Development Environment upgrades, developers are free to update to the latest release as soon as it becomes available.

The OutSystems free offers will be updated to the latest release as soon as possible.


## End of mainstream support

### How is it announced?

At OutSystems we are committed to supporting our customers and minimizing the impact of upgrades to new releases. We support each version of our product for a minimum of 2 years from the date of commercial release.

End of support for specific product versions is managed directly with customers. Customers using a product version approaching the end of support are notified at least 1 year before the targeted end of support date, and periodically from there until the final date. If the customer is using OutSystems Cloud, our teams will engage the customer and prepare a migration plan. Please read more about our end of mainstream support [here](https://www.outsystems.com/legal/success/support-terms-and-service-level-agreements-sla-of-the-outsystems-software/#end-of-support-for-older-software-versions).

For discontinued versions, it might be necessary to have some downtime; therefore we advise continuously upgrading to the latest release as soon as possible, which heavily reduces the risk for potential downtime. In any instance, OutSystems may provide specialized migration services.

### What is the support calendar for OutSystems releases? 

The below calendar shows the past, current, and planned dates for OutSystems product mainstream support.

![OutSystems support calendar](images/product-lifecycle-cal-diag.png)


## Documentation and training updates

The following table shows the different types of documentation and the moments when they're updated:


| | Major release | Release | Cumulative patch |
|---|---|---|---|
| [Training](https://www.outsystems.com/learn) | Updated | Updated | Not updated |
| [Product documentation](https://success.outsystems.com/Documentation) | Updated | Updated | Not updated |
| [Breaking changes](https://success.outsystems.com/Support/Archive/11/OutSystems_Platform_side_effects_and_breaking_changes) | Updated | Updated | Not updated |
| [System requirements](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems/OutSystems_system_requirements) | Updated | Updated | Not updated |
| [Installation checklist](https://www.outsystems.com/Downloads/search/) | Updated | Updated | Not updated |
| [Release notes](https://success.outsystems.com/Support/Release_Notes) | Updated | Updated | Updated |
| [Product updates](https://www.outsystems.com/product-updates/) | Updated | Updated | Updated |

## Product release model

OutSystems ecosystem is divided into components with different release cycles. To find out more about each component check [OutSystems tools and components](https://www.outsystems.com/evaluation-guide/development-and-management-tools) and for release cycles check [OutSystems Product Releases](https://success.outsystems.com/Support/Enterprise_Customers/Upgrading/OutSystems_Release_Cycle).
