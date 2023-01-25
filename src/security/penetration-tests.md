---
summary: Support for penetration tests and vulnerability scans, explore the false positives findings.
tags:
locale: en-us
guid: 43176740-324f-4592-a993-5d4f9fa660fb
app_type: traditional web apps, mobile apps, reactive web apps
---

# Penetration testing

## Overview

As a subscription customer, you may wish to perform penetration tests or vulnerability scans. This is possible as long as they're limited to your own OutSystems Cloud, hybrid, or self-managed infrastructure.
For OutSystems Cloud, the tests are limited to the assets under the responsability of the **Customer** as described under the [OutSystems shared responsability model](../enterprise/maintenance/cloud-shared-responsibility.md).

## Before you start

To avoid generating false positive findings, make sure you consult the [OutSystems Platform Hardening](platform-server-hardening.md) documentation. 

To find all the procedure details necessary to perform penetration tests and vulnerability scans in your OutSystems Cloud environments, refer to [Load and penetration tests on OutSystems Cloud](penetration-test-cloud.md).

## Reviewing the results { #review-results }

When reviewing penetration test results, it's important to keep in mind that each penetration test framework reports on findings without a proper context. To detect false positives, these findings must be reviewed. For more information on understanding the findings in their proper context, you can contact OutSystems support [here](https://www.outsystems.com/goto/submit-support-case).

### False positives

The following are some examples of false positive findings. In each one, there's a description of why they're considered as such.

#### jQuery 1.8.3 flagged as a potentially vulnerable library

OutSystems uses jQuery version 1.8.3 which has the following known vulnerabilities:

* Issue - Selector interpreted as HTML.
[CVE-2012-6708](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2012-6708) relates to a potential Cross-Site Scripting vulnerability in jQuery's selector operator ( $ ). While the jQuery version we ship with OutSystems is based on version 1.8.3, it contains some changes made by OutSystems. In particular, as of OutSystems version 9.1.401.0, the fix was backported and the $ operator is no longer vulnerable to this attack.

* Issue - Prototype pollution.
The jQuery version 1.8.3 is vulnerable to Prototype Pollution, [CVE-2019-11358](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-11358). The extend function can be tricked into modifying the prototype of Object when the attacker controls part of the structure passed to this function. This can let an attacker add or modify an existing property that will then exist on all objects. You can find more information on the vulnerability [here](https://snyk.io/vuln/SNYK-JS-JQUERY-174006). While the jQuery version we ship with OutSystems is based on 1.8.3, it doesn't contain any of the patterns described in the vulnerability description, for which this is considered a false positive.

* Issue - Passing HTML from untrusted sources to one of jQuery's DOM manipulation methods.
The jQuery versions 1.0.3 to 3.5.0 are vulnerable to the possible execution of untrusted code ([CVE-2020-11022](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-11022) and [CVE-2020-11023](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-11023)). While the jQuery version we ship with OutSystems is based on 1.8.3, the Platform Server doesn't generate code that passes HTML from untrusted sources to the JQuery DOM manipulation methods, for which this is considered a false positive.

#### jQuery-ui-dialog flagged as a potentially vulnerable library

Some penetration testing tools may flag OutSystems as having a vulnerable jQuery-ui-dialog library.

OutSystems uses jQuery-ui-dialog version 1.8.24 which has a vulnerability known to this version - [CVE-2010-5312](https://www.cvedetails.com/cve/CVE-2010-5312/). This vulnerability relates to the title() function, potentially allowing for unescaped content to be inserted in the title and causing a cross site scripting problem.

All uses of the affected function by OutSystems properly encode the input parameter. As such, OutSystems isn't vulnerable despite this vulnerability still being present in jquery-ui-dialog.

As for applications developed by your users which make use of this library, you should ensure that you encode the input to the title() function correctly. Alternatively, you can import your own version of jquery-ui-dialog into a different namespace and use that version instead.

#### jQuery-ui-tooltip flagged as a potentially vulnerable library

Some penetration testing tools may flag OutSystems as having a vulnerable jQuery-ui-tooltip library - [CVE-2012-6662](https://nvd.nist.gov/vuln/detail/cve-2012-6662). 

OutSystems doesn't use jQuery-ui-tooltip widget. It's not present on our code.

## Support from OutSystems

OutSystems support and security teams are ready to discuss the findings of the penetration tests with you under the following conditions:

* We expect that you do a preliminary analysis of the report, and report  the issues that are caused by the platform and/or cloud infrastructure to OutSystems support.
* The list of issues reported to OutSystems support should exclude issues that can be fixed by the developers or OutSystems admins by enforcing configurations.

Support's reply may include the following:

* A reasoned identification of false positives.
* A reasoned adjustment of severity based on the specifics of the technical environment.
* An escalation of eventual product defects to R&D.

Furthermore, the following tables can help you understand the responsibilities and expectations by deployment model:

**OutSystems Cloud & hybrid**

|            | Responsibilities |Expectations  |
|------------|------------------|--------------|
| Customer   | <ul><li>Deploy and manage OutSystems on self managed servers</li><li>Execute the penetration tests</li></ul>|<ul><li>The customer has knowledge of how to configure and manage OutSystems and underlying technologies</li><li>The customer has knowledge of the tool(s) used to perform penetration tests</li><li>The customer is responsible for executing the tests, collecting the results, reviewing the results, performing the necessary correction and re-checking</li></ul>|
| OutSystems | <ul><li>Maintain and manage OutSystems Cloud</li><li>Help customers set up the hybrid infrastructure</li><li>Provide support to customers on issues related to the product and deployment</li></ul>|<ul><li>Has expert knowledge on OutSystems cloud</li><li>Has expert knowledge on OutSystems</li><li>Is able to help customers with OutSystems related issues [(support terms)](https://www.outsystems.com/legal/success/support-terms-and-service-level-agreements-sla-of-the-outsystems-software/)</li><li>Is able to reply to Customer questions</li></ul>|

**Self-managed**

|            | Responsibilities| Expectations |
|------------|-----------------|--------------|
| Customer   | <ul><li>Deploy and manage OutSystems on self managed servers</li><li>Execute the penetration tests</li></ul>|<ul><li>The customer has knowledge of how to configure and manage OutSystems and  underlying technologies</li><li>The customer has knowledge of the tool(s) used to perform penetration tests</li><li>The customer is responsible for executing the tests, collecting the results, reviewing the results, performing the necessary correction and re-checking</li></ul>| 
| OutSystems | <ul><li>Provide support to customers on issues related to the product</li></ul>|<ul><li>Has expert knowledge on OutSystems</li><li>Is able to help Customers with OutSystems related issues [(support terms)](https://www.outsystems.com/legal/success/support-terms-and-service-level-agreements-sla-of-the-outsystems-software/)</li><li>Is able to reply to customer questions</li></ul>|


