---
summary: One or more <record> Ids aren't valid GUIDs.
tags:
---

# OS-CMFR-GEN-00019

## Error message

`One or more <record> Ids aren't valid GUIDs.`

## Cause

While executing one of the **Bootstrap/Setup** actions, the Case Management framework detected that one or more records don't have a valid GUID set as the Identifier attribute.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the Identifier attribute of the records all match to a valid GUID.

You can use an online generator to easly generate a GUID. For example:

* e2f3c612-3cd4-4536-a0b4-d03df29afcf6

## More info

A GUID is a 128-bit integer (16 bytes) that can be used across all computers and networks wherever a unique identifier is required. In its canonical textual representation, the 16 octets of a GUID are represented as 32 hexadecimal (base-16) digits, displayed in five groups separated by hyphens, in the form 8-4-4-4-12 for a total of 36 characters (32 hexadecimal characters and 4 hyphens).
