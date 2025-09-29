---
summary: Explore how to install OutSystems 11 (O11) on FIPS-compliant systems and resolve cryptographic algorithm errors.
locale: en-us
guid: 4f250e9c-6197-4fc6-8ee2-d6070619a935
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
tags: fips compliance, cryptographic algorithms, system configuration, error resolution, .net framework
audience:
  - platform administrators
  - full stack developers
  - backend developers
outsystems-tools:
  - none
coverage-type:
  - apply
---

# Installing the OutSystems on a FIPS compliant system

## Problem

You are getting the following error when running OutSystems:

"This implementation is not part of the Windows Platform FIPS validated cryptographic algorithms"

This will happen on systems that have been set to enforce FIPS policy, when running Platform Server versions earlier than 11.38.0.

## Cause

OutSystems internally uses MD5 and other hashing algorithms which may not be FIPS-validated.

We consider this use to not be against FIPS 140 policies as it is not used for cryptography purposes.

## Resolution

Since this may violate your company's policies, you should get in touch with your IT and request to disable the machine's local policy regarding FIPS compliant algorithms. This can be done by setting Local Security Policy > Local Policies > Security Options > System Cryptography: Use FIPS compliant algorithms for encryption, hashing and signing to "Disable" .

Alternatively it's possible to override this configuration in .NET by following [these instructions](https://msdn.microsoft.com/en-us/library/hh202806(v=vs.110).aspx).

<div class="info" markdown="1">

Starting from Platform Server 11.38.0, you can install the platform in FIPS-compliant environments. Please check the [system requirements](https://success.outsystems.com/documentation/11/setup_outsystems_infrastructure_and_platform/setting_up_outsystems/outsystems_system_requirements/#fips-compliance).

</div>
