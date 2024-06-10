---
summary: Removing unsafe-inline
locale: en-us
guid: 773cfac2-eed6-44ae-a2c6-f63d68e6c8a7
app_type: reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?type=design&node-id=3431%3A270&mode=design&t=n3OfSI1cyFvKAAiH-1
---

# Removing unsafe-inline 

<div class="info" markdown="1">

Applies to Reactive web apps only

</div>

The following are the breaking changes that may occur when you disable the **Enforce Unsafe Inline Reactive** setting in Factory Configuration.

## Browser's console error

``Refused to execute inline script because it violates the following Content Security Policy directive: "script-src 'self'".`

Browser errors include a stack that allows you to track the source of the error.

## Service Center error logs

``Content Security Policy blocked 'inline'.``

### Example

This is an example of a JavaScript file (resource loaded when opening the App) that can't be found.

![Screenshot displaying an error because the JavaScript file can't be found.](images/javascript-not-found.png "JavaScript File Not Found Error")

This scenario may have a small or critical impact on the app, depending on the resource that is not loaded and executed.

If you can’t resolve the error, open a support case with the OutSystems Support team. You’ll need the following information:
* Service Center Error Logs (that occur when the error is observed). If the issue is related to a missing resource, no errors will appear in the Service Center, reflecting this specific scenario.
* OutSystems Solution that contains all dependencies in order to replicate the issue
* Exact steps to reproduce the Error
* The HAR file, from a timeframe reproducing the error.
* The running folder of the affected app.
