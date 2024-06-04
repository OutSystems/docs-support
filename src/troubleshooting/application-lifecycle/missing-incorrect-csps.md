---
summary: Troubleshooting missing or incorrect CSPs
locale: en-us
guid: 14893878-ab23-4afd-8935-c901853a5ebe
app_type: reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?type=design&node-id=3431%3A273&mode=design&t=klPGgLnFhGS1wmJs-1
---

## Troubleshooting missing or incorrect CSPs

To confirm if the CSP headers are being applied, you can use the browser's developer tools to check the headers sent by the OutSystems appl. To accomplish that, navigate to the application URL with the Developer Tools opened on the Network tab and check the response headers of the request (document type).

Example below:

![Browser developer tools network tab displaying the Content Security Policy headers sent by an OutSystems application](images/csp-header-dev-tools.png "Checking CSP Headers in Browser Developer Tools")

If the headers are either not present or are different from what you expected, we recommend checking the following:

* Confirm that the app and its dependencies were published after the configuration of the Content Security Policies. Otherwise, the settings are not effective.
* Validate whether the CSP configurations set at the application level are the same as the ones set for the whole environment. CSP headers at the application level overwrite the environment-level configurations.
* Confirm that no Shared Configuration is manipulating the CSP headers. If there's an existing Shared Configuration adding custom headers associated with existing modules, it will overwrite the CSP configurations defined in LifeTime. OutSystems recommends managing CSP headers in Lifetime only.
