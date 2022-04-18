---
summary: <record> Id is not a valid GUID: <input-parameter-value>
tags:
locale: en-us
guid: 8bb2689d-1198-4f5f-b04d-ae962aee277c
app_type: traditional web apps, mobile apps, reactive web apps
---

# OS-CMFR-GEN-00003

## Error message

`<record> Id is not a valid GUID: <input-parameter-value>`

## Cause

While trying to execute an action, the Case Management framework detected an invalid GUID format.

## Impact

The Case Management framework wasn't able to successfully execute the action.

## Recommended action

Verify if the value that is being passed as input to the Case Management framework action is GUID and has the correct format. Use Service Studio's Debugger to check the input parameter's value at the time of execution.

If necessary, you can use an online generator to easly generate a GUID. For example:

* e2f3c612-3cd4-4536-a0b4-d03df29afcf6
 
## More info

A GUID is a 128-bit integer (16 bytes) that can be used across all computers and networks wherever a unique identifier is required. In its canonical textual representation, the 16 octets of a GUID are represented as 32 hexadecimal (base-16) digits, displayed in five groups separated by hyphens, in the form 8-4-4-4-12 for a total of 36 characters (32 hexadecimal characters and 4 hyphens).    
