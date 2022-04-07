---
summary:
locale: en-us
guid: 4f250e9c-6197-4fc6-8ee2-d6070619a935
---

# Installing the Platform on a FIPS compliant system

## Problem

You are getting the following error when running OutSystems:

"This implementation is not part of the Windows Platform FIPS validated cryptographic algorithms"

This will happen on systems which have been set to enforce FIPS policy.

## Cause

OutSystems internally uses MD5 and other hashing algorithms which may not be FIPS-validated.

We consider this use to not be against FIPS 140 policies as it is not used for cryptography purposes.

## Resolution

Since this may violate your company's policies, you should get in touch with your IT and request to disable the machine's local policy regarding FIPS compliant algorithms. This can be done by setting Local Security Policy > Local Policies > Security Options > System Cryptography: Use FIPS compliant algorithms for encryption, hashing and signing to "Disable" .

Alternatively it's possible to override this configuration in .NET by following [these instructions](https://msdn.microsoft.com/en-us/library/hh202806(v=vs.110).aspx).

