---
summary:
en_title: How are OutSystems Platform versions numbered?
---

# How are OutSystems versions numbered?

**Starting with Development Environment version 11.5.39, Platform Server 11.7.0, and LifeTime version 11.4.0**, OutSystems version numbers are a sequence of three numbers, separated by a period, and assigned in ascending order.

The version numbering schema is as follows:

**_[Major]_****.****_[Feature]_****.****_[Patch]_** (Build ****_[Build ID]_****)

The several components of the version number are the following:

**[Major]**

This number identifies the major product version. A new major version is defined in your Subscription Agreement as an "**Upgrade**" or a “**New Software Version**”.

**[Feature]**

This number increases when OutSystems adds functionality to a release in a backward-compatible manner (e.g. from Platform Server 11 **.7**.*n*, where *n* is a number, to Platform Server 11 **.8**.0).

**[Patch]**

This number increases when OutSystems makes backward-compatible bug fixes or minor improvements in a release (e.g. from Development Environment 11.7 **.1** to Development Environment 11.7 **.2**).

**[Build ID]**

This number identifies a specific build and is unique for each OutSystems component: Development Environment, Platform Server, LifeTime, e.g. "Development Environment 11.7.1 **(Build 91)**".

In most scenarios, the version is identified by the three first numbers: **[Major].[Feature].[Patch]**. However, in some cases, you need to identify a very specific build and, in this case, you should use the three numbers and the build ID.

### Example

The following table illustrates the usage of version numbers in 3 different types of releases:

| Stage | Version number change |
|-------|-----------------------|
| A major release containing new features and possibly breaking changes.The first number (major product version) increases and the other two numbers are reset to 0. | from **10**.n.nto **11**.0.0 |
| A release containing new functionality, but with no breaking changes.The second number (feature) increases and the third number is reset to 0.                     | from 11.**0**.nto 11.**1**.0 |
| A release containing only defect fixes and minor improvements.The third number (patch) increases.                                                                  | from 11.1.0to 11.1.**1**  |


*n* = an integer number

