---
summary: 
---

# Previous version number format

This document refers to a previous version number format used in OutSystems 10 releases and in older versions of OutSystems 11.

For the current version number format, check [How are OutSystems Platform versions numbered?](https://success.outsystems.com/Support/Enterprise_Customers/Upgrading/How_are_OutSystems_Platform_versions_numbered%3F)

The previous version number format consisted of a sequence of four numbers, separated by a period, and assigned in ascending order.

This version numbering schema was as follows:

**Major first digit**.**Major second digit**. **[Feature set][Patch set]**.**[Hotfix or Alpha/Beta]**

(M.n.ffpp.xyy)

**[Major first digit].[Major second digit]**

M.n

These two digits identify the Major version. A new Major version is defined in your Subscription Agreement as an "**Upgrade**" or a “**New Software Version**”.

**[Feature set][Patch set]**

[ff][pp]

ff [01-99]  - it signals that a new feature set has been delivered. It is incremented when a new feature set is delivered along with defect fixes.

pp [00-99]  - it is reserved for patch sets. It is incremented when a new patch set includes only defect fixes, and no changes to the feature set.

**[Hotfix or Alpha/Beta]**

M.n.ffpp.xyy

xyy = 0 - Generally Available version

xyy [1-99] - Hot fix over a Generally Available version

xyy [100-999] - Alpha or Beta release 

## Examples

 9.1.100.0	    reads as     Major version 9.1, feature set 1, patch set 0

 9.1.101.4	    reads as	 Major version 9.1, feature set 1, patch set 1, hotfix 4

 9.1.101.302    reads as     Major version 9.1, feature set 1, patch set 1, beta 302


The following table illustrates the usage of version numbers during the life cycle of a Major version:

| Stage                                                               | Version number | Version type                           |
|---------------------------------------------------------------------|----------------|----------------------------------------|
| Beta 1                                                              | 9.1.0.100      | Development version                    |
| Defect fixes                                                        | 9.1.0.1**01**  | Development version                    |
| Beta 2                                                              | 9.1.0.1**02**  | Development version                    |
| General Availability of Major version                               | 9.1.**100**.0  | Generally Available version            |
| Hotflix                                                             | 9.1.100.**1**  | Hotfix delivered to selected customers |
| Maintenance update, including only defect fixes                     | 9.1.1**01**.0  | Generally Available version            |
| Maintenance update, including only defect fixes                     | 9.1.1**02**.0  | Generally Available version            |
| Alpha/Beta for a new feature                                        | 9.1.102.**100**| Development version                    |
| Maintenance update, including both the new feature and defect fixes | 9.1. **2**00.0 | Generally Available version            |


