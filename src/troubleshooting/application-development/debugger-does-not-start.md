---
summary: This article explains how to troubleshoot if the debugger does not start in a particular version of chrome. 
locale: en-us
guid: A46FC291-7A1D-4D99-852A-972FA5E4F8E8
tags: 
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=3327:550
---

# Debugger does not start in Chrome

With the Chrome version 111.0.5563.64/.65 released on March 7, 2023, the debugger at Service Studio does not start. 
The following section will help you understand and resolve the error you may encounter while using the Service Studio debugger. 

## Symptom

The Service Studio may display a message similar to the following when launching the debugger:

![Chrome error](images/debugger-error-ss.png)

Please check the Chrome version under Settings if you receive this message. 

![Chrome error](images/debugger-chrome-update-ss.png)

## Cause

The Chrome version **111.0.5563.64/.65** released on March 7, 2023 is associated with a detected issue on Service Studio usage.
Hence, all Service Studio users that are using Chrome 111.0.5563.64/.65 will not be able to start debugger.

## Recommended action

To restore the debugger feature back to service, upgrade Service Studio to the latest version 11.53.43.62091. 

If the problem still persists, [open a ticket](https://success.outsystems.com/support/home/) with OutSystems Support. 
