---
summary: OutSystems 11 (O11) debugger fails to start in Chrome version 111.0.5563.64/.65, requiring an upgrade to resolve the issue.
locale: en-us
guid: A46FC291-7A1D-4D99-852A-972FA5E4F8E8
tags: ide usage, chrome browser issue, debugger, technical support, troubleshooting
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?node-id=3327:550
audience:
  - mobile developers
  - frontend developers
  - full stack developers
outsystems-tools:
  - service studio
coverage-type:
  - unblock
---

# Debugger does not start in Chrome

With the Chrome version 111.0.5563.64/.65 released on March 7, 2023, the debugger at Service Studio does not start. 
The following section will help you understand and resolve the error you may encounter while using the Service Studio debugger. 

## Symptom

The Service Studio may display a message similar to the following when launching the debugger:

![Error dialog box in Service Studio indicating that the browser used for debugging is unresponsive.](images/debugger-error-ss.png "Service Studio Debugger Error Message")

Please check the Chrome version under Settings if you receive this message. 

![Google Chrome's 'About' section showing the browser is up to date with version 111.0.5563.65.](images/debugger-chrome-update-ss.png "Chrome Version Check for Debugger Issue")

## Cause

The Chrome version **111.0.5563.64/.65** released on March 7, 2023 is associated with a detected issue on Service Studio usage.
Hence, all Service Studio users that are using Chrome 111.0.5563.64/.65 will not be able to start debugger.

## Recommended action

To restore the debugger feature back to service, upgrade Service Studio to the latest version 11.53.43.62091. 

If the problem still persists, [open a ticket](https://success.outsystems.com/support/home/) with OutSystems Support. 
