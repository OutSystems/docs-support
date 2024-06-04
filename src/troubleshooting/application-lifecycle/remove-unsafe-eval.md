---
summary: Removing unsafe-eval
locale: en-us
guid: 413298b7-54dc-47cd-bbcd-2c87611980fa
app_type: reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?type=design&node-id=3431%3A267&mode=design&t=n3OfSI1cyFvKAAiH-1
---

# Removing unsafe-eval

<div class="info" markdown="1">

Applies to Reactive web apps only

</div>

## Browers console error

* ``Refused to evaluate a string as JavaScript because 'unsafe-eval' is not an allowed source of script in the following Content Security Policy directive: "script-src 'self'".``

## Service Center error logs

* ``Content Security Policy blocked 'eval'.``
* ``EvalError: Refused to evaluate a string as JavaScript because 'unsafe-eval' is not an allowed source of script in the following Content Security Policy directive: "script-src 'self'".``

Service Center and browser errors include a stack that allows you to track the source of the error and correct it. 

### Example 1

In this example, the error is caused by using a component (from OutSystems Charts) that uses the eval().

![Screenshot of a browser console error caused by using a component from OutSystems Charts that uses the eval() function.](images/linechart-error.png "Screenshot showing error caused by using a component that uses the eval")

### Example 2

In this example, the error is caused by a JavaScript Widget that is performing an eval().

![Screenshot of a JavaScript Widget performing an eval() function, causing a browser console error.](images/javascript-error-ss.png "Screenshot showing error caused by JavaScript Widget that is performing an eval")

Reading the stack trace allows you to track the exact location of this pattern in order to correct it.

![Screenshot of a browser console error caused by a JavaScript Widget performing an eval() function.](images/javascript-error.png "Screenshot showing error caused by JavaScript Widget that is performing an eval")

If you can’t resolve the error, open a support case with the OutSystems Support team. You’ll need the following information:
* Service Center Error Logs (that occur when the error is observed)
* OutSystems Solution that contains all dependencies in order to replicate the issue
* Exact steps to reproduce the Error
